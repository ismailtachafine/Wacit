# Symfony Application Documentation

## 1. Overview

This application is built using the **Symfony 6.4** framework and adheres to the **Model-View-Controller (MVC)** architecture. It offers a suite of modules to manage various organizational functions, including:

- User management  
- Project tracking  
- On-call duty (Astreinte) management  
- Bonus (Prime) allocation  
- Performance evaluations (EVP)  
- IT cost tracking (ITICS)  
- Overtime management  
- Public holiday administration  
- Collaborator data  
- Security and access control  

---

## 2. Core Modules

Each module serves a distinct purpose within the system:

- **User Management:** Authentication, authorization, roles, and permission handling.  
- **Project Management:** Project creation, monitoring, and reporting features.  
- **Astreinte Management:** Assignment and scheduling of on-call duties.  
- **Prime Management:** Handling bonuses and incentives, including calculation and distribution.  
- **EVP (Performance Evaluation):** Goal setting, feedback, and employee performance reviews.  
- **ITICS (IT Costs):** Management of expenses related to hardware, software, and IT services.  
- **Overtime Management:** Tracking and managing extra working hours.  
- **Public Holiday Management:** Configuration and handling of official holidays.  
- **Collaborator Management:** Storing collaborator details like personal data, skills, and roles.  
- **Security:** Access policies and resource protection enforcement.

---

## 3. Diagrams

### 3.1 Class Diagrams (Mermaid)

- **User Management:**  
  ![User Diagram](docs/diagrams/ev_stations_ny.png)

- **Project Management:**  
  ![Project Diagram](docs/diagrams/diagram_1.png)

- **Astreinte Management:**  
  ![Astreinte Diagram](docs/diagrams/diagram_2.png)

- **Prime Management:**  
  ![Prime Diagram](docs/diagrams/diagram_3.png)

- **ITICS:**  
  ![IT Costs Diagram](docs/diagrams/diagram_4.png)

### 3.2 Sequence Diagrams

- **User Authentication:**  
  ![Authentication](docs/diagrams/diagram_5.png)

- **Project Creation Workflow:**  
  ![Project Creation](docs/diagrams/diagram_6.png)

- **Astreinte Creation Workflow:**  
  ![Astreinte Creation](docs/diagrams/diagram_7.png)

---

## 4. Installation & Usage

### 4.1 Prerequisites

- PHP 8.1 or later  
- Composer  
- MySQL or compatible database

### 4.2 Installation Steps

1. **Clone the Repository**
   ```bash
   git clone <repository_url>
   cd <project_directory>
   ```

2. **Install Dependencies**
   ```bash
   composer install
   ```

3. **Configure the Environment**

   - Create a new MySQL database.
   - Update the `.env` file:
     ```
     DATABASE_URL="mysql://db_user:db_password@127.0.0.1:3306/db_name?serverVersion=8.0&charset=utf8mb4"
     ```

4. **Run Migrations**
   ```bash
   php bin/console doctrine:migrations:migrate
   ```

5. **Create an Initial User**
   ```bash
   php bin/console app:create-user
   ```

6. **Start the Server**
   ```bash
   symfony server:start
   ```

### 4.3 Running the Application

1. Open your browser and go to `http://127.0.0.1:8000`.  
2. Log in with the credentials you created.  
3. Use the sidebar navigation to access different modules.

---

## 5. Code Samples

### 5.1 Creating a User (Controller)

```php
#[Route('/new', name: 'app_user_new', methods: ['GET', 'POST'])]
public function new(Request $request, EntityManagerInterface $entityManager, UserPasswordHasherInterface $passwordHasher): Response
{
    $user = new User();
    $form = $this->createForm(UserType::class, $user);
    $form->handleRequest($request);

    if ($form->isSubmitted() && $form->isValid()) {
        $hashedPassword = $passwordHasher->hashPassword($user, $form->get('plainPassword')->getData());
        $user->setPassword($hashedPassword);

        $entityManager->persist($user);
        $entityManager->flush();

        return $this->redirectToRoute('app_user_index', [], Response::HTTP_SEE_OTHER);
    }

    return $this->render('user/new.html.twig', [
        'user' => $user,
        'form' => $form->createView(),
    ]);
}
```

### 5.2 Retrieving Projects (Repository)

```php
public function add(Project $entity, bool $flush = false): void
{
    $this->getEntityManager()->persist($entity);
    if ($flush) {
        $this->getEntityManager()->flush();
    }
}

public function remove(Project $entity, bool $flush = false): void
{
    $this->getEntityManager()->remove($entity);
    if ($flush) {
        $this->getEntityManager()->flush();
    }
}
```

### 5.3 Displaying Astreintes (Twig)

```twig
{% extends 'base.html.twig' %}

{% block title %}Astreinte Index{% endblock %}

{% block body %}
<h1>Astreinte Index</h1>

<table class="table">
    <thead>
        <tr>
            <th>Id</th>
            <th>Collaborator</th>
            <th>Start Date</th>
            <th>End Date</th>
            <th>Actions</th>
        </tr>
    </thead>
    <tbody>
    {% for astreinte in astreintes %}
        <tr>
            <td>{{ astreinte.id }}</td>
            <td>{{ astreinte.collaborator.firstName }} {{ astreinte.collaborator.lastName }}</td>
            <td>{{ astreinte.startDate ? astreinte.startDate|date('Y-m-d H:i:s') : '' }}</td>
            <td>{{ astreinte.endDate ? astreinte.endDate|date('Y-m-d H:i:s') : '' }}</td>
            <td>
                <a href="{{ path('app_astreinte_show', {'id': astreinte.id}) }}">Show</a>
                <a href="{{ path('app_astreinte_edit', {'id': astreinte.id}) }}">Edit</a>
            </td>
        </tr>
    {% else %}
        <tr>
            <td colspan="5">No records found.</td>
        </tr>
    {% endfor %}
    </tbody>
</table>

<a href="{{ path('app_astreinte_new') }}">Create New</a>
{% endblock %}
```

---