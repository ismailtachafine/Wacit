```markdown
# Application Documentation

## 1. System Overview

This application is built using the Symfony 6.4 framework and follows the Model-View-Controller (MVC) architectural pattern. It provides a suite of modules for managing various aspects of the organization, including user management, project management, on-call duty (Astreinte) management, bonus (Prime) management, performance evaluations (EVP), IT cost management (ITICS), overtime, public holidays, collaborator data, and security.

## 2. Module Descriptions

The application consists of the following core modules:

*   **User Management:** Provides authentication and authorization services, managing user accounts, roles, and permissions.
*   **Project Management:** Manages project-related information, including project creation, tracking, and reporting.
*   **Astreinte Management:** Handles the scheduling, assignment, and tracking of on-call duties.
*   **Prime Management:** Manages bonus and incentive programs, including calculation and distribution.
*   **EVP (Evaluation of Professional Performance):** Facilitates the performance evaluation process, including goal setting, feedback collection, and performance reviews.
*   **ITICS (IT Costs):** Manages IT-related costs, including hardware, software, and services.
*   **Overtime Management:** Tracks and manages overtime hours worked by employees.
*   **Public Holidays Management:** Defines and manages public holiday calendars.
*   **Collaborator Management:** Manages collaborator data, including personal information, skills, and roles.
*   **Security:** Enforces access control policies and protects application resources.

## 3. Mermaid Class Diagrams

### 3.1. User Management Module

![Diagram 0](diagrams/diagram_0.png)

### 3.2. Project Management Module

![Diagram 1](diagrams/diagram_1.png)

### 3.3. Astreinte Management Module

![Diagram 2](diagrams/diagram_2.png)

### 3.4. Prime Management Module

![Diagram 3](diagrams/diagram_3.png)

### 3.5. ITICS (IT Costs) Module
![Diagram 4](diagrams/diagram_4.png)

## 4. Sequence Diagrams for Key Workflows

### 4.1. User Authentication

![Diagram 5](diagrams/diagram_5.png)

### 4.2. Project Creation

![Diagram 6](diagrams/diagram_6.png)

### 4.3. Astreinte Creation

![Diagram 7](diagrams/diagram_7.png)

## 5. Installation/Usage Instructions

### 5.1. Prerequisites

*   PHP 8.1 or higher
*   Composer
*   MySQL or other supported database

### 5.2. Installation

1.  Clone the repository:

    ```bash
    git clone <repository_url>
    cd <project_directory>
    ```

2.  Install dependencies:

    ```bash
    composer install
    ```

3.  Configure the database:

    *   Create a database in MySQL.
    *   Update the `.env` file with your database credentials:

        ```
        DATABASE_URL=mysql://db_user:db_password@127.0.0.1:3306/db_name?serverVersion=8.0&charset=utf8mb4
        ```

4.  Run database migrations:

    ```bash
    php bin/console doctrine:migrations:migrate
    ```

5.  Create a user:

    ```bash
    php bin/console app:create-user
    ```

6.  Start the Symfony server:

    ```bash
    symfony server:start
    ```

### 5.3. Usage

1.  Open your browser and navigate to the application URL (e.g., `http://127.0.0.1:8000`).
2.  Log in with the credentials created in step 5 of the installation process.
3.  Use the navigation menu to access the different modules.

## 6. Code Examples

### 6.1. Creating a User (Controller)

```php
<?php

namespace App\Controller;

use App\Entity\User;
use App\Form\UserType;
use Doctrine\ORM\EntityManagerInterface;
use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\HttpFoundation\Request;
use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\PasswordHasher\Hasher\UserPasswordHasherInterface;
use Symfony\Component\Routing\Annotation\Route;

#[Route('/user/new', name: 'app_user_new', methods: ['GET', 'POST'])]
class UserController extends AbstractController
{
    #[Route('/new', name: 'app_user_new', methods: ['GET', 'POST'])]
    public function new(Request $request, EntityManagerInterface $entityManager, UserPasswordHasherInterface $passwordHasher): Response
    {
        $user = new User();
        $form = $this->createForm(UserType::class, $user);
        $form->handleRequest($request);

        if ($form->isSubmitted() && $form->isValid()) {
            // Hash the password
            $hashedPassword = $passwordHasher->hashPassword(
                $user,
                $form->get('plainPassword')->getData()
            );
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
}
```

### 6.2. Retrieving Projects (Repository)

```php
<?php

namespace App\Repository;

use App\Entity\Project;
use Doctrine\Bundle\DoctrineBundle\Repository\ServiceEntityRepository;
use Doctrine\Persistence\ManagerRegistry;

/**
 * @extends ServiceEntityRepository<Project>
 *
 * @method Project|null find($id, $lockMode = null, $lockVersion = null)
 * @method Project|null findOneBy(array $criteria, array $orderBy = null)
 * @method Project[]    findAll()
 * @method Project[]    findBy(array $criteria, array $orderBy = null, $limit = null, $offset = null)
 */
class ProjectRepository extends ServiceEntityRepository
{
    public function __construct(ManagerRegistry $registry)
    {
        parent::__construct($registry, Project::class);
    }

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

    //    /**
    //     * @return Project[] Returns an array of Project objects
    //     */
    //    public function findByExampleField($value): array
    //    {
    //        return $this->createQueryBuilder('p')
    //            ->andWhere('p.exampleField = :val')
    //            ->setParameter('val', $value)
    //            ->orderBy('p.id', 'ASC')
    //            ->setMaxResults(10)
    //            ->getQuery()
    //            ->getResult()
    //        ;
    //    }

    //    public function findOneBySomeField($value): ?Project
    //    {
    //        return $this->createQueryBuilder('p')
    //            ->andWhere('p.exampleField = :val')
    //            ->setParameter('val', $value)
    //            ->getQuery()
    //            ->getOneOrNullResult()
    //        ;
    //    }
}
```

### 6.3. Displaying Astreintes (Twig Template)

```twig
{# templates/astreinte/index.html.twig #}

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
                <th>actions</th>
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
                    <a href="{{ path('app_astreinte_show', {'id': astreinte.id}) }}">show</a>
                    <a href="{{ path('app_astreinte_edit', {'id': astreinte.id}) }}">edit</a>
                </td>
            </tr>
        {% else %}
            <tr>
                <td colspan="5">no records found</td>
            </tr>
        {% endfor %}
        </tbody>
    </table>

    <a href="{{ path('app_astreinte_new') }}">Create new</a>
{% endblock %}
```
