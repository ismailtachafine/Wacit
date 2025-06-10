# Application Documentation: Astreinte Platform

## 1. System Overview

The Astreinte Platform is a web application built with the Symfony 6.4 framework, using the MVC architectural pattern. It includes modules for managing organizational operations such as shift scheduling, employee evaluations, bonus allocations, project oversight, and personnel records. Key technologies include Doctrine ORM for database operations, Twig for templating, Symfony Security for authentication/authorization, and attribute routing for streamlined route definition. Encryption plays a vital role in securing data across components.

## 2. Module Descriptions

The application comprises the following key modules:

- **Astreinte Module (Shift Management/On-call Duty):** Manages employee shift schedules and on-call duties, including shift patterns, assignments, availability tracking, and request handling.
- **EVP Module (Evaluation Process):** Supports employee evaluations with features for defining criteria, collecting feedback, generating reports, and monitoring development goals.
- **Prime Module (Bonuses/Incentives):** Administers bonuses and incentives, including defining structures, calculating payouts, and budget tracking.
- **Project Module (Project Management):** Facilitates planning, task delegation, resource allocation, and status tracking.
- **Collaborator Module (Employee Management):** Manages employee records including contact info, job roles, and access rights.

Detailed analysis of controller-entity relationships is required for a complete understanding of inter-module dependencies.

## 3. Mermaid Class Diagrams

These example diagrams illustrate general module architecture. For detailed diagrams, access to the codebase is required.

### General Module Structure

![Diagram 0](docs/diagrams/diagram_0.png)

### Astreinte Module (Sample Diagram)

![Diagram 1](docs/diagrams/diagram_1.png)

## 4. Sequence Diagrams for Key Workflows

The following are illustrative examples. Refined diagrams should be based on actual code review.

### Creating a New Shift (Astreinte Module)

![Diagram 2](docs/diagrams/diagram_2.png)

### Requesting an Evaluation (EVP Module)

![Diagram 3](docs/diagrams/diagram_3.png)

## 5. Installation and Usage Instructions

### Prerequisites

- PHP 8.1 or higher
- MySQL 8.0
- Composer
- Nginx (or Apache)

### Installation Steps

1. **Clone the repository:**

    ```bash
    git clone <repository_url>
    cd <project_directory>
    ```

2. **Install dependencies:**

    ```bash
    composer install
    ```

3. **Configure database connection:**

    - Create a MySQL database.
    - Update the `.env` file:

      ```env
      DATABASE_URL=mysql://db_user:db_password@127.0.0.1:3306/db_name?serverVersion=8.0&charset=utf8mb4
      ```

4. **Run migrations:**

    ```bash
    php bin/console doctrine:migrations:migrate
    ```

5. **Configure web server (Nginx):**

    ```nginx
    server {
        listen 80;
        server_name yourdomain.com;

        root /path/to/your/project/public;
        index index.php;

        location / {
            try_files $uri $uri/ /index.php?$args;
        }

        location ~ \.php$ {
            include snippets/fastcgi-php.conf;
            fastcgi_pass unix:/run/php/php8.1-fpm.sock;
        }

        location ~ /\.ht {
            deny all;
        }
    }
    ```

    - Enable the site and restart Nginx:

    ```bash
    sudo ln -s /etc/nginx/sites-available/astreinte /etc/nginx/sites-enabled/
    sudo nginx -t
    sudo systemctl restart nginx
    ```

6. **Start Symfony server (development):**

    ```bash
    php bin/console server:start
    ```

### Access and Navigation

- Visit the app via `yourdomain.com`.
- Log in or register a new user.
- Use the navigation menu to access modules.

## 6. Code Examples

### ShiftController (Astreinte Module)

```php
#[Route('/shift')]
class ShiftController extends AbstractController
{
    #[Route('/', name: 'app_shift_index', methods: ['GET'])]
    public function index(ShiftRepository $shiftRepository): Response
    {
        return $this->render('shift/index.html.twig', [
            'shifts' => $shiftRepository->findAll(),
        ]);
    }
    // ... other controller methods ...
}
```

### Shift Entity

```php
#[ORM\Entity(repositoryClass: ShiftRepository::class)]
class Shift
{
    #[ORM\Id]
    #[ORM\GeneratedValue]
    #[ORM\Column]
    private ?int $id = null;

    #[ORM\Column(type: 'datetime')]
    private ?\DateTimeInterface $startTime = null;

    #[ORM\Column(type: 'datetime')]
    private ?\DateTimeInterface $endTime = null;

    #[ORM\ManyToOne(targetEntity: Collaborator::class)]
    #[ORM\JoinColumn(nullable: false)]
    private ?Collaborator $employee = null;

    // Getter and Setter methods ...
}
```

### ShiftType Form

```php
class ShiftType extends AbstractType
{
    public function buildForm(FormBuilderInterface $builder, array $options): void
    {
        $builder
            ->add('startTime', DateTimeType::class, [
                'date_widget' => 'single_text',
                'time_widget' => 'single_text',
            ])
            ->add('endTime', DateTimeType::class, [
                'date_widget' => 'single_text',
                'time_widget' => 'single_text',
            ])
            ->add('employee', EntityType::class, [
                'class' => Collaborator::class,
                'choice_label' => 'name',
            ]);
    }

    public function configureOptions(OptionsResolver $resolver): void
    {
        $resolver->setDefaults([
            'data_class' => Shift::class,
        ]);
    }
}
```

---

> For a full understanding of the system, deeper inspection of each module's code is recommended.
