
# Documentation Technique Complète

*Générée le 2025-09-19 00:54:30*

Cette documentation technique rétroactive complète a été générée par analyse automatisée du code source du projet.


# Présentation Générale

---

```wiki
# Présentation Générale de WacitV2

## 1. Vue d'ensemble du projet

WacitV2 est une application web de gestion complète, conçue pour optimiser la gestion des ressources humaines, des projets, des finances et des activités des collaborateurs. Développée en utilisant une architecture robuste et des technologies web modernes, elle assure une performance élevée, une évolutivité optimale et une facilité d'utilisation pour l'ensemble des utilisateurs. L'application vise à centraliser l'information, automatiser les tâches, améliorer la collaboration et faciliter la prise de décision.

## 2. Objectifs du projet

*   **Centralisation de l'information**: Fournir un point d'accès unique et centralisé pour l'ensemble des données relatives aux collaborateurs, aux projets et aux finances. Cela simplifie l'accès aux informations et facilite leur consultation rapide et efficace.
*   **Automatisation des tâches**: Simplifier et automatiser les processus de gestion, notamment la gestion des astreintes, des primes et des dépenses. L'automatisation réduit les erreurs, optimise les flux de travail et améliore l'efficacité globale.
*   **Amélioration de la collaboration**: Faciliter la collaboration entre les différents acteurs (collaborateurs, managers, administrateurs) grâce à des outils de communication et de partage d'informations intégrés. L'objectif est de promouvoir un environnement de travail collaboratif et transparent.
*   **Prise de décision éclairée**: Offrir des informations précises, fiables et actualisées, ainsi que des rapports personnalisables. Ces outils permettent une prise de décision stratégique, basée sur des données concrètes et pertinentes.

## 3. Fonctionnalités principales

WacitV2 propose un ensemble de fonctionnalités complètes pour répondre aux besoins de gestion des organisations :

*   **Gestion des Astreintes**:
    *   Planification et suivi des périodes d'astreinte, avec gestion des créneaux horaires et des équipes.
    *   Gestion des cas exceptionnels : modifications, remplacements et ajustements des plannings.
    *   Validation des astreintes par les responsables hiérarchiques, avec suivi des approbations.
    *   Export des données d'astreinte vers différents formats (CSV, Excel, PDF) pour l'intégration avec d'autres systèmes ou le reporting.
*   **Gestion des Primes**:
    *   Calcul automatisé et attribution des primes selon des règles définies et paramétrables.
    *   Validation des primes par les gestionnaires, avec un workflow d'approbation.
    *   Gestion des différents types de primes (performance, ancienneté, objectifs, etc.) et personnalisation des règles de calcul.
    *   Export des données de primes pour l'intégration avec les systèmes de paie.
*   **Gestion des Projets**:
    *   Création, modification et suivi de l'avancement des projets, avec gestion des statuts.
    *   Gestion des étapes, des tâches, des jalons et des livrables liés aux projets.
    *   Validation des projets et des livrables, avec des workflows d'approbation.
    *   Export des données des projets pour le reporting et l'analyse de la performance.
*   **Gestion des Dépenses**:
    *   Enregistrement et suivi des dépenses engagées, avec classification par catégories.
    *   Gestion des différents types de dépenses (frais de déplacement, fournitures, etc.), avec pièces justificatives.
    *   Validation des dépenses par les responsables hiérarchiques, avec un système d'approbation.
    *   Export des données de dépenses pour le contrôle budgétaire, la comptabilité et l'analyse financière.
*   **Gestion des Collaborateurs**:
    *   Gestion des informations personnelles et professionnelles des collaborateurs (coordonnées, qualifications, etc.).
    *   Gestion des droits d'accès et des rôles utilisateurs, avec une gestion fine des permissions.
    *   Suivi de l'historique des activités et des modifications, avec audit trail.
    *   Fonctionnalités de sauvegarde et de restauration des données, pour assurer la sécurité et la disponibilité des informations.
*   **Gestion des Utilisateurs et des Permissions**:
    *   Gestion des comptes utilisateurs et des rôles (administrateur, manager, collaborateur, etc.).
    *   Gestion fine des permissions d'accès aux différentes fonctionnalités et données (CRUD : Create, Read, Update, Delete).
    *   Mise en place d'une politique de sécurité robuste pour protéger les données sensibles.
*   **Gestion des Calendriers**:
    *   Intégration d'un calendrier partagé pour la planification des événements, des réunions, des congés et des activités importantes.
    *   Possibilité de synchronisation avec des calendriers externes (Google Calendar, Outlook, etc.).
*   **Gestion des Échanges de Devises**:
    *   Suivi des taux de change en temps réel, grâce à l'intégration d'une API de conversion de devises.
    *   Conversion des devises pour faciliter les transactions internationales et les rapports financiers.
*   **Gestion des Approbations et Validations**:
    *   Mise en place de workflows d'approbation personnalisables pour différents processus (astreintes, primes, projets, dépenses), avec des notifications et des rappels.
    *   Gestion des étapes d'approbation, des responsabilités et des délais.

## 4. Technologies Utilisées

WacitV2 est développé en utilisant les technologies suivantes :

*   **Langage**: PHP (version 8.1 ou supérieure recommandée)
*   **Framework**: Symfony (version 6 ou 7) pour la gestion de l'architecture et du développement.
*   **Base de données**: PostgreSQL (recommandé pour la performance et la robustesse) ou MySQL (compatible) via Doctrine ORM
*   **Frontend**:
    *   HTML, CSS, JavaScript pour l'interface utilisateur.
    *   Frameworks : Bootstrap, AdminLTE pour la conception et l'organisation de l'interface.
    *   Librairies : jQuery, Twig (moteur de template), Select2, DataTables, @hotwired (Turbo, Stimulus), Popper pour l'interactivité et la gestion des données.
*   **Serveur Web**: Nginx (recommandé pour la performance) ou Apache (compatible)
*   **Conteneurisation**: Docker (pour le développement, le déploiement et la gestion des environnements)
*   **Tests**: PHPUnit pour la qualité et la stabilité du code.

## 5. Architecture générale

L'architecture de WacitV2 est basée sur le pattern MVC (Modèle-Vue-Contrôleur) et tire parti des fonctionnalités offertes par le framework Symfony, assurant une structure claire et une maintenabilité accrue :

*   **Modèle**: Les entités Doctrine (classes PHP mappées sur la base de données) représentent les données de l'application et gèrent la logique de persistance (accès, modification, suppression).
*   **Vue**: Les templates Twig sont utilisés pour afficher les données de manière dynamique et personnalisée, facilitant la séparation du code et du contenu.
*   **Contrôleur**: Les contrôleurs gèrent les requêtes HTTP, traitent la logique applicative, interagissent avec le modèle et la vue, et coordonnent les interactions entre les différents composants.
*   **Repositories**: Les repositories Doctrine permettent d'accéder à la base de données de manière structurée, offrant des méthodes pour la recherche, la création, la modification et la suppression des données. Ils encapsulent la logique d'accès aux données et facilitent les requêtes complexes.
*   **Services**: Les services encapsulent la logique métier réutilisable, assurant une séparation des responsabilités, facilitant les tests unitaires et améliorant la maintenabilité du code. Ils regroupent les traitements spécifiques qui ne sont pas directement liés à une entité ou à une requête HTTP.

## 6. Structure des fichiers

La structure des fichiers suit l'organisation standard préconisée par Symfony, ce qui facilite la compréhension, la maintenance et l'évolutivité du projet. Voici quelques répertoires importants :

*   `src/Controller/`: Contient les contrôleurs, qui gèrent les requêtes et définissent la logique métier.
*   `src/Entity/`: Contient les entités Doctrine, qui représentent les modèles de données.
*   `src/Form/`: Contient les classes de formulaires Symfony, permettant de gérer les saisies et la validation des données.
*   `src/Repository/`: Contient les repositories Doctrine, qui permettent d'accéder aux données.
*   `templates/`: Contient les templates Twig, qui définissent la présentation des données.
*   `config/`: Contient les fichiers de configuration de l'application (services, paramètres, routes, etc.).
*   `public/`: Contient les assets publics (CSS, JavaScript, images) et le point d'entrée principal de l'application (`index.php`).

## 7. Points d'entrée

*   `public/index.php`: Point d'entrée principal pour les requêtes web. Ce fichier initialise l'application Symfony, gère le routage des requêtes et est le point d'accès principal à l'application web.
*   `bin/*`: Scripts en ligne de commande pour les tâches d'administration, telles que la sauvegarde de la base de données, la gestion de la console Symfony, l'exécution des tests, etc.

## 8. Installation et configuration du projet

Le projet utilise Docker pour faciliter le développement et le déploiement, permettant de créer des environnements isolés et reproductibles.

*   **Configuration Docker**:
    *   Le fichier `docker-compose.yml` définit la configuration de base des conteneurs Docker (PHP, Nginx, base de données, etc.). Il permet de définir les services, les réseaux et les volumes utilisés par l'application.
    *   Les fichiers `docker-compose.override.*.yml` permettent de spécifier des configurations supplémentaires pour différents environnements (développement, pré-production, production). Ces fichiers permettent de personnaliser la configuration de l'application en fonction de l'environnement.
    *   Le fichier `Dockerfile` définit l'image Docker pour l'application PHP, en spécifiant l'environnement d'exécution, les dépendances et les instructions pour la construction de l'image.
    *   Le répertoire `docker/nginx` contient la configuration de Nginx pour le routage des requêtes et la gestion du serveur web. Il contient les fichiers de configuration du serveur Nginx, tels que les fichiers de configuration des virtual hosts et les règles de réécriture d'URL.

*   **Gestion des dépendances**: Les dépendances PHP sont gérées par Composer (fichiers `composer.json` et `composer.lock`). Composer permet d'installer et de gérer les bibliothèques et les extensions nécessaires au fonctionnement de l'application.

*   **Configuration des variables d'environnement**: Les variables d'environnement sont définies dans le fichier `.env` et peuvent être utilisées pour configurer l'accès à la base de données, les clés API, les paramètres de débogage, etc. L'utilisation de variables d'environnement permet de séparer la configuration de l'application du code source et de faciliter le déploiement dans différents environnements.

    ```bash
    # Exemple de configuration d'une variable d'environnement dans le fichier .env
    DATABASE_URL=postgresql://user:password@host:port/database_name
    APP_ENV=dev
    ```

## 9. Dépendances

*   **Dépendances externes**: Symfony, Doctrine, Twig, et d'autres librairies (voir `composer.json`). Ces librairies sont essentielles pour le bon fonctionnement de l'application et offrent des fonctionnalités prêtes à l'emploi, facilitant le développement et la gestion du projet.
*   **Dépendances internes**: Gérées par l'injection de dépendances Symfony et l'utilisation des espaces de noms PHP. L'architecture du projet repose sur des relations bien définies entre les entités, les contrôleurs, les formulaires, les services et les repositories, facilitant la maintenance et l'évolutivité.
*   **Gestion des dépendances**: Le fichier `composer.json` liste les dépendances du projet et leurs versions. Composer est utilisé pour installer et gérer ces dépendances, garantissant la compatibilité et la stabilité de l'application.

## 10. Scripts de gestion

Le répertoire `bin/` contient des scripts permettant d'exécuter des tâches spécifiques et d'automatiser certaines opérations :

*   `bin/backup.sh`: Script de sauvegarde des données de la base de données (peut nécessiter une configuration spécifique, notamment des paramètres d'accès à la base de données et le chemin de sauvegarde).
*   `bin/console`: Script de la console Symfony, permettant d'exécuter des commandes de gestion et de maintenance. La console Symfony offre des outils pour interagir avec l'application, exécuter des tâches et effectuer des opérations de débogage.
*   `bin/phpunit`: Script d'exécution des tests unitaires. Ce script lance les tests unitaires pour vérifier la qualité et la stabilité du code.

## 11. Tests unitaires

Le projet utilise PHPUnit pour les tests unitaires, afin de garantir la qualité, la fiabilité et la maintenabilité du code. Les tests unitaires permettent de vérifier le comportement de chaque composant de l'application de manière isolée. Le fichier `phpunit.xml.dist` contient la configuration des tests, incluant les paramètres de configuration, les exclusions et les rapports de couverture.

```bash
# Exemple de commande pour lancer les tests unitaires
./bin/phpunit
```

## 12. Documentation additionnelle

*   Une documentation plus détaillée sur les différentes sections de l'application est fournie dans d'autres documents. Ces documents spécifiques traitent des modules, des fonctionnalités et des aspects techniques de l'application.
*   Les guides d'installation, la documentation de l'API et des exemples d'utilisation sont accessibles dans des sections spécifiques, offrant des ressources complètes pour les développeurs et les utilisateurs.
```

APPROVED: [content]
```

---

# Architecture

---

```wiki
# Architecture de WacitV2

## 1. Introduction

Ce document présente l'architecture du système WacitV2. Il est destiné aux développeurs, aux architectes, aux testeurs et aux nouveaux collaborateurs afin de faciliter la compréhension, la maintenance et l'évolution du système. La documentation décrit les composants, leurs interactions, les flux de données et les technologies utilisées. Elle sert de référence pour la conception, la mise en œuvre et le maintien du système.

## 2. Vue d'Ensemble

### 2.1. Type et Objectif du Projet

WacitV2 est une application web de gestion d'entreprise, probablement axée sur les ressources humaines et la gestion de projets. Elle offre une gamme de fonctionnalités, notamment la gestion des astreintes, des primes, des projets, des dépenses, des calendriers et des droits d'accès. L'objectif principal est de fournir une solution intégrée pour optimiser les processus métiers, améliorer l'efficacité opérationnelle et offrir une expérience utilisateur intuitive.

### 2.2. Architecture

*   **Pattern Architectural**: L'application est basée sur le pattern **MVC (Modèle-Vue-Contrôleur)**, inhérent au framework Symfony. Cette approche favorise une séparation claire des responsabilités, facilitant la maintenance, l'évolutivité et les tests unitaires.

*   **Couches Logicielles**: L'architecture est structurée en plusieurs couches distinctes, chacune ayant des responsabilités spécifiques :
    *   **Couche Présentation (Frontend)**: Responsable de l'interface utilisateur et de l'interaction avec l'utilisateur.
    *   **Couche Métier (Backend)**: Contient la logique métier de l'application, les règles métier et l'accès aux données.
    *   **Couche Accès aux Données**: Responsable de la persistance des données et de l'interaction avec la base de données.

*   **Persistance des Données**: L'application utilise une base de données relationnelle pour le stockage persistant des données. L'interaction avec la base de données est gérée via **Doctrine ORM (Object-Relational Mapper)**, ce qui simplifie le développement et la gestion des requêtes.

*   **Scripts d'Administration**: Des scripts shell sont utilisés pour les tâches d'administration et de maintenance, telles que les sauvegardes, les restaurations, l'exécution de tâches planifiées et l'intégration avec des services externes.

### 2.3. Diagramme de Composants

Le diagramme suivant illustre les principaux composants de WacitV2 et leurs relations :

```plantuml
@startuml
    ' Définition des composants principaux
    rectangle "Frontend (Web)" {
        [Navigateur Web]
        component "JavaScript (jQuery, Bootstrap, Stimulus)"
        component "Contrôleurs JS"
        component "Vues (Twig)"
    }

    rectangle "Backend (API/Logique Métier)" {
        component "Symfony Framework"
        component "Contrôleurs PHP"
        component "Services"
        component "Entités Doctrine"
        database "Base de Données"
    }

    rectangle "Scripts Shell (Maintenance)" {
        component "backup.sh"
        component "autres scripts"
    }

    ' Définition des relations et des flux de données
    [Navigateur Web] -- [JavaScript (jQuery, Bootstrap, Stimulus)] : Requêtes HTTP
    [JavaScript (jQuery, Bootstrap, Stimulus)] --> [Backend (API/Logique Métier)] : Requêtes API (fetch, Axios)
    [Backend (API/Logique Métier)] --> [Contrôleurs PHP] : Gestion des requêtes
    [Contrôleurs PHP] -- [Services] : Utilisation
    [Services] -- [Entités Doctrine] : Accès et manipulation
    [Entités Doctrine] -- database "Base de Données" : Accès aux données
    [Scripts Shell (Maintenance)] --> database "Base de Données" : Sauvegarde/Restauration (si applicable)
    [Scripts Shell (Maintenance)] --> [Services] : Exécution de tâches (si applicable)
    [Backend (API/Logique Métier)] -- [Services] : Tâches planifiées (via Cron ou autre)

    ' Affichage des points d'intégration
    note right of [Backend (API/Logique Métier)]
      API REST\n      (Définis par les annotations Symfony)
    end note

    note bottom of [Scripts Shell (Maintenance)]
      Intégration avec services cloud (ex: AWS S3), tâches Cron
    end note
@enduml
```

## 3. Composants et leurs Interactions

### 3.1. Frontend

*   **Technologies**: HTML, CSS, JavaScript (jQuery, Bootstrap, Stimulus), Twig.
*   **Responsabilités**: Présentation des données, interactions utilisateur, appels d'API vers le backend, gestion de l'expérience utilisateur et validation côté client (si nécessaire).
*   **Composants principaux**:
    *   **Vues**: Templates Twig pour la présentation des données. Elles affichent les informations et permettent l'interaction avec l'utilisateur. Les vues sont responsables de la mise en forme de l'affichage.
    *   **Contrôleurs JS**: Gèrent les interactions utilisateur, les requêtes AJAX, la manipulation du DOM et la mise à jour dynamique de l'interface. L'utilisation de Stimulus facilite l'organisation du code JavaScript, en associant des comportements JavaScript à des éléments HTML spécifiques.
    *   **JavaScript (jQuery, Bootstrap)**: Fournit des fonctionnalités d'interaction, de manipulation du DOM, de gestion des événements et de rendu. Bootstrap offre des composants d'interface utilisateur pré-stylisés, accélérant le développement. jQuery est utilisé pour simplifier les manipulations du DOM et les appels AJAX (bien que l'usage de `fetch` ou `Axios` soit également possible, comme indiqué dans le diagramme).
    *   **Asset Mapper**: Gestion des assets statiques (CSS, JS, images, etc.). L'Asset Mapper de Symfony optimise la gestion et le rendu des assets, en incluant la minification et le versioning pour améliorer les performances.

### 3.2. Backend

*   **Technologies**: PHP, Symfony Framework, Doctrine.
*   **Responsabilités**: Gestion des requêtes HTTP, logique métier, accès aux données, authentification et autorisation, exposition des API REST, gestion des processus métier, validation des données côté serveur.
*   **Composants principaux**:
    *   **Contrôleurs**: Reçoivent les requêtes HTTP, gèrent la logique de routage, valident les entrées, autorisent l'accès et appellent les services appropriés. Ils agissent comme intermédiaires entre les requêtes et la logique métier. Les contrôleurs sont responsables de la coordination des actions et du renvoi des réponses.
    *   **Services**: Implémentent la logique métier, gèrent les opérations complexes, encapsulent les règles métier et interagissent avec les entités Doctrine. Ils offrent une réutilisabilité et une testabilité accrue. Les services peuvent également orchestrer des opérations impliquant plusieurs entités ou composants.
    *   **Entités**: Représentent les données stockées dans la base de données. Elles définissent la structure des données et sont mappées aux tables de la base de données via Doctrine. Les entités encapsulent les données et les comportements associés.
    *   **Repositories**: Classes d'accès aux données via Doctrine. Elles fournissent des méthodes pour interroger et manipuler les données de manière structurée. Les repositories facilitent l'accès aux données et masquent les détails d'implémentation de la base de données.
    *   **Formulaires**: Gestion des formulaires, validation des données (côté serveur) et conversion des données entrées. Symfony Forms facilite la création et la gestion des formulaires, assurant la sécurité et la cohérence des données.

### 3.3. Base de Données

*   **Technologie**: Base de données relationnelle (ex: MySQL, PostgreSQL). Le choix de la base de données dépend des exigences spécifiques de l'application, telles que l'évolutivité, les performances et les contraintes de coût.
*   **Responsabilités**: Stockage persistant et récupération des données de l'application. Elle assure la cohérence, l'intégrité et la sécurité des données.
*   **Interactions**: Le backend (Doctrine ORM) interagit avec la base de données pour persister et récupérer les données des entités, facilitant l'accès et la manipulation des données. Les requêtes sont construites et exécutées par Doctrine, qui traduit les opérations en langage SQL.

### 3.4. Scripts Shell

*   **Technologie**: Bash.
*   **Responsabilités**: Tâches d'administration, de maintenance et d'intégration avec des systèmes externes. Cela inclut les sauvegardes/restaurations de la base de données, l'exécution de tâches planifiées (via cron), et l'interaction avec des services externes (par exemple, l'intégration avec des services de stockage cloud).
*   **Composants principaux**:
    *   `bin/backup.sh`: Script pour gérer les sauvegardes des données (configuration, exécution, journalisation). Ce script peut utiliser des outils tels que `mysqldump` (pour MySQL) ou `pg_dump` (pour PostgreSQL).
    *   `autres scripts`: Scripts personnalisés pour des opérations spécifiques, telles que la synchronisation de données, le traitement par lots ou l'intégration avec des API externes.

## 4. Flux de Données

Ce schéma décrit le flux de données typique lors d'une interaction utilisateur :

1.  **Requête Utilisateur**: L'utilisateur effectue une action dans le navigateur web (ex : remplit un formulaire, clique sur un bouton).
2.  **Interaction Frontend**: Le JavaScript (jQuery, Bootstrap, Stimulus, les contrôleurs JS) interagit avec l'interface utilisateur, valide les données (côté client, si applicable) et envoie une requête HTTP (généralement en format JSON) vers le backend.
3.  **Traitement Backend**: Le backend reçoit la requête, le contrôleur gère la logique de routage, valide les données reçues (côté serveur) et appelle les services nécessaires.
4.  **Accès aux Données**: Les services utilisent Doctrine pour accéder à la base de données, récupérer ou manipuler les données.
5.  **Réponse**: Le backend renvoie une réponse (généralement au format JSON pour les API) au frontend, contenant les données demandées ou un statut d'opération (succès, erreur).
6.  **Mise à Jour Frontend**: Le frontend traite la réponse, met à jour l'interface utilisateur pour refléter les changements (ex : affichage de données, messages de confirmation).
7.  **Sauvegarde/Maintenance (si applicable)**: Les scripts shell sont exécutés, accédant potentiellement à la base de données et interagissant avec des services externes pour des opérations de maintenance (sauvegarde, restauration, etc.).

### 4.1. Diagramme de Séquence (Exemple : Soumission d'un Formulaire)

Le diagramme de séquence suivant illustre le flux lors de la soumission d'un formulaire :

```plantuml
@startuml
    participant "Navigateur Web" as WB
    participant "Contrôleur JS" as CJS
    participant "Backend (Contrôleur PHP)" as BCP
    participant "Service" as S
    participant "Base de Données" as DB

    WB -> CJS : Soumission du formulaire
    activate CJS
    CJS -> CJS : Validation (côté client - optionnel)
    CJS -> BCP : Requête API (POST/PUT)
    activate BCP
    BCP -> S : Appel de méthode du service (avec les données du formulaire)
    activate S
    S -> DB : Lecture/Écriture des données (via Doctrine)
    activate DB
    DB --> S : Données (si lecture) / Confirmation (si écriture)
    deactivate DB
    S --> BCP : Réponse (succès/erreur)
    deactivate S
    BCP --> BCP : Validation (côté serveur)
    BCP --> CJS : Réponse (JSON : succès/erreur + données)
    deactivate BCP
    CJS --> WB : Mise à jour de l'interface (affichage du résultat, messages d'erreur)
    deactivate CJS
@enduml
```

## 5. Points d'Intégration

*   **API REST**:  Le backend (Symfony) expose des API RESTful pour interagir avec le frontend et potentiellement avec d'autres services externes. Ces API permettent au frontend de récupérer des données, de soumettre des formulaires et d'effectuer des actions spécifiques. L'utilisation d'API RESTful facilite l'intégration avec des clients tiers et le développement d'applications natives.
*   **Base de Données**: L'application s'intègre avec une base de données relationnelle (via Doctrine ORM) pour le stockage persistant des données. Doctrine facilite les opérations de lecture, d'écriture et de mise à jour des données, ainsi que la gestion des relations entre les entités.
*   **Services Externes**: L'application peut s'intégrer avec des services externes tels que des services cloud (ex: AWS S3 pour le stockage de fichiers), des passerelles de paiement, des services d'envoi d'e-mails et d'autres API. L'intégration avec des services externes permet d'étendre les fonctionnalités de l'application et de déléguer des tâches spécifiques à des services spécialisés.
*   **Mailer**:  Utilisation du mailer de Symfony pour l'envoi d'e-mails transactionnels et de notifications. Le mailer permet d'envoyer des emails de manière asynchrone, améliorant ainsi les performances de l'application.

## 6. Technologies Utilisées

*   **Langages**: PHP, JavaScript
*   **Frameworks**: Symfony (6 ou 7), AdminLTE (pour l'interface d'administration, optionnel), Bootstrap.
*   **ORM**: Doctrine (ORM).
*   **Librairies**: Twig, jQuery, Select2, DataTables, @hotwired (Turbo, Stimulus), Popper.
*   **Autres**: Nginx (serveur web), Docker (conteneurisation), PHPUnit (tests unitaires), Composer (gestion des dépendances).

## 7. Fichiers de Configuration Clés

*   **Configuration Symfony**:
    *   `config/`: Contient les fichiers de configuration YAML pour les bundles, les routes, les services, etc. Ce répertoire est le point central pour configurer l'application Symfony. Il est structuré pour organiser et gérer les configurations des différents composants et services.
    *   `.env`: Variables d'environnement.  Ce fichier contient des variables spécifiques à l'environnement (développement, production, etc.) comme les identifiants de la base de données. Il permet de configurer l'application sans modifier le code source.
    *   `routes.yaml`: Définition des routes de l'application. Ce fichier définit les URLs et les contrôleurs associés, ce qui permet de définir les points d'entrée de l'application.
*   **Gestionnaire de dépendances**: `composer.json` et `composer.lock`. Ces fichiers gèrent les dépendances de l'application, permettant d'installer, de mettre à jour et de gérer les librairies et les paquets requis.
*   **Tests**: `phpunit.xml.dist`. Ce fichier configure les tests unitaires de PHPUnit. Il définit les paramètres de configuration des tests, tels que les dossiers de test, les fichiers de configuration et les options de couverture du code.
*   **Docker**:  `docker-compose.yml`, `docker-compose.override.preprod.yml`, `docker-compose.override.prod.yml`, `Dockerfile`. Ces fichiers définissent la configuration Docker de l'application, permettant la conteneurisation et le déploiement de l'application.
*   **Serveur Web**:  `nginx/*` (configuration Nginx). Ces fichiers configurent le serveur web Nginx pour servir l'application, gérant le routage, la sécurité et les performances.

## 8. Développement et Déploiement

*   **Environnement de développement**: L'environnement de développement est basé sur Docker. Docker permet de containeriser l'application et ses dépendances, garantissant ainsi la cohérence de l'environnement de développement et simplifiant le déploiement. Il facilite également la collaboration entre les développeurs.
*   **Déploiement**: Le déploiement est réalisé en utilisant des conteneurs Docker. L'utilisation de Docker facilite le déploiement continu et le scaling de l'application.  Les configurations de Nginx dans le répertoire `docker/nginx` suggèrent une approche de déploiement avec Nginx. Le processus de déploiement peut être automatisé à l'aide d'outils de CI/CD (intégration et livraison continues).

## 9. Scalabilité et Performance

*   **Optimisation Frontend**: L'utilisation de jQuery, Bootstrap et Stimulus vise à améliorer l'expérience utilisateur en fournissant une interface réactive et intuitive.  La minification des ressources statiques (CSS, JavaScript) est essentielle pour réduire les temps de chargement. L'optimisation des images et le chargement asynchrone des ressources peuvent également améliorer les performances.
*   **Optimisation Backend**: L'utilisation de Doctrine, la mise en place d'un système de cache (par exemple, avec le cache Symfony) pour les données fréquemment accédées et l'optimisation des requêtes SQL sont importantes pour améliorer les performances et réduire la charge sur la base de données. L'utilisation de mécanismes de mise en cache avancés (par exemple, Redis ou Memcached) peut également améliorer les performances.
*   **Base de Données**: L'optimisation des requêtes SQL, l'utilisation d'index sur les colonnes fréquemment utilisées, et le choix d'une base de données adaptée aux besoins de l'application sont cruciaux pour la performance. Le partitionnement des données et la réplication de la base de données peuvent améliorer l'évolutivité. L'utilisation de requêtes préparées et la gestion des connexions à la base de données sont également importantes.

## 10. Sécurité

*   **Authentification/Autorisation**:  L'application utilise les mécanismes de sécurité intégrés de Symfony (ex:  Authentification via JWT, OAuth, ou sessions) pour authentifier les utilisateurs et gérer les droits d'accès. La gestion des rôles et des permissions permet de contrôler l'accès aux différentes fonctionnalités de l'application.
*   **Protection contre les attaques courantes**:  L'utilisation des protections natives de Symfony contre les attaques XSS (Cross-Site Scripting), CSRF (Cross-Site Request Forgery) et les injections SQL est essentielle. L'application doit également être protégée contre les attaques de type DoS (Denial of Service).
*   **Validation des données**:  La validation des données en entrée et en sortie est mise en place pour prévenir les vulnérabilités et garantir l'intégrité des données.  Symfony Forms est utilisé pour simplifier et sécuriser la validation des formulaires. La validation côté serveur est essentielle pour empêcher les attaques.

## 11. Conclusion

Cette documentation fournit une vue d'ensemble de l'architecture de WacitV2. Elle décrit les composants, leurs interactions, les flux de données et les technologies utilisées. Ce document est un point de départ pour comprendre et maintenir l'application. Des documents plus détaillés sur les différents modules (Astreintes, Primes, etc.) et les aspects spécifiques de l'implémentation devraient être consultés pour une compréhension complète de l'application. Cette architecture est conçue pour être robuste, évolutive et sécurisée, et doit être continuellement revue et améliorée pour répondre aux besoins en constante évolution.
```

APPROVED:


---

# Modules

---

```markdown
# Section MODULES - Documentation Technique de WacitV2

## Introduction

Cette section de la documentation fournit une description détaillée de chaque module et composant du système WacitV2. Elle est destinée aux développeurs, aux testeurs, aux architectes et aux nouveaux arrivants afin de faciliter la compréhension, la maintenance, l'évolution et la contribution au développement de l'application. Chaque module est décrit en détail, y compris ses composants, ses interactions avec d'autres modules, les règles métiers associées, et les considérations de sécurité.

## 1. Vue d'Ensemble des Modules

WacitV2 est structuré en plusieurs modules interconnectés, chacun gérant un ensemble de fonctionnalités spécifiques. Cette modularisation permet une meilleure organisation du code, une maintenance simplifiée et une évolutivité accrue. Les modules principaux sont les suivants :

*   **Gestion des Astreintes**: Permet la gestion des astreintes des collaborateurs, incluant la planification, l'enregistrement, la validation, le suivi, et le calcul des indemnités.
*   **Gestion des Primes**: Permet la gestion des primes des collaborateurs, incluant le calcul, l'attribution, la validation et l'intégration avec la paie.
*   **Gestion des Projets**: Permet la gestion des projets, des étapes, des tâches, des affectations des ressources, du suivi de l'avancement, de la gestion budgétaire et des risques.
*   **Gestion des Dépenses**: Permet la gestion des dépenses, incluant les achats, les frais, les notes de frais, les remboursements, et l'intégration avec la comptabilité.
*   **Gestion des Collaborateurs**: Gère les informations relatives aux collaborateurs, incluant les données personnelles, les informations de contact, les postes, les départements, et l'historique.
*   **Gestion des Utilisateurs et des Permissions**: Gère les comptes utilisateurs, les rôles, les permissions associées, l'authentification et l'autorisation. Ce module est essentiel pour la sécurité et le contrôle d'accès.
*   **Gestion des Calendriers**: Permet la gestion des calendriers, incluant les jours fériés, les congés, les absences, et les événements calendaires, avec prise en compte des spécificités locales.
*   **Gestion des Échanges de Devises**: Permet la gestion des taux de change pour les devises utilisées, incluant l'intégration avec des sources de données externes et la conversion des montants.
*   **Gestion des Approbations et Validations**: Gère les processus d'approbation et de validation pour différentes opérations (astreintes, primes, dépenses, etc.), avec prise en charge des workflows personnalisés et des notifications.

## 2. Détails des Modules

Cette section décrit en détail chaque module, ses composants, ses interactions, ses règles métiers, les exemples de code pertinents, ainsi que les aspects liés aux tests et à la sécurité.  Pour chaque module, les éléments suivants sont présentés : description, composants clés, règles métiers, exemples de code, interactions, tests et sécurité.

### 2.1. Gestion des Astreintes

*   **Description**: Ce module permet la gestion complète des astreintes des collaborateurs. Il inclut la définition des périodes d'astreinte, la saisie des informations relatives aux interventions, la validation par les responsables, l'approbation, et la génération de rapports. Le module gère également les exceptions (maladie, congés, etc.) et les cas particuliers liés aux astreintes, ainsi que le calcul des indemnités associées.

*   **Composants Clés**:

    *   **Entité `Astreinte.php`**: Définit la structure de données pour les astreintes. Elle contient les attributs tels que la date de début et de fin, le collaborateur concerné (clé étrangère vers l'entité `Collaborator`), le motif de l'astreinte, les informations d'intervention, le statut (en attente, validé, approuvé, refusé), les commentaires, etc.  (Exemple : `src/Entity/Astreinte.php`)
    *   **Contrôleur `AstreinteController.php`**: Gère les requêtes HTTP pour les opérations CRUD (Create, Read, Update, Delete) sur les astreintes. Il gère également les validations, les approbations, les refus, et les notifications.  Ce contrôleur fait appel aux services pour la logique métier. (Exemple : `src/Controller/AstreinteController.php`)
    *   **Repository `AstreinteRepository.php`**: Fournit des méthodes pour l'accès aux données des astreintes dans la base de données. Il permet d'effectuer des requêtes complexes, des filtrages et des tris, notamment pour la recherche d'astreintes par collaborateur, période, statut, etc.  (Exemple : `src/Repository/AstreinteRepository.php`)
    *   **Formulaires**:  Permettent la saisie et la modification des données des astreintes. Ils utilisent le composant Form de Symfony pour la gestion des formulaires HTML, la validation des données (avec des contraintes de validation personnalisées si nécessaire) et la liaison avec les entités. (ex: `TypeAstreinteType.php`). (Exemple : `src/Form/TypeAstreinteType.php`)
    *   **Templates Twig**:  Responsables de l'affichage des informations des astreintes. Ils utilisent le moteur de template Twig pour générer les vues HTML, CSS et JavaScript. Ils incluent des formulaires, des tableaux de données, et des boutons d'action. (ex: `astreinte/index.html.twig`, `astreinte/validation-index.html.twig`, `astreinte/show.html.twig`). (Exemple : `templates/astreinte/index.html.twig`)
    *   **Services**: Le module utilise des services pour encapsuler la logique métier et les opérations récurrentes.  Ces services incluent le calcul des heures d'astreinte (`AstreinteService`), l'envoi de notifications (`NotificationService`), la gestion des statuts et des workflows d'approbation (`ApprovalService`), et l'accès aux données des collaborateurs et des calendriers. (Exemple: `src/Service/AstreinteService.php`)

*   **Règles Métiers**:

    *   Une astreinte doit être associée à un collaborateur valide (clé étrangère vérifiée).
    *   Les périodes d'astreinte ne doivent pas se chevaucher pour le même collaborateur.  Une vérification de chevauchement doit être effectuée avant l'enregistrement.
    *   Les astreintes doivent être validées par les responsables appropriés selon un workflow défini (rôle et hiérarchie).
    *   Gestion des exceptions (ex: absences, maladies) et des cas particuliers (jours fériés, interventions exceptionnelles).
    *   Calcul précis des heures d'astreinte et des indemnités associées, selon les accords d'entreprise et la législation en vigueur.
    *   Prise en compte des règles de droit du travail en vigueur.
    *   Gestion des priorités et des alertes en cas d'urgence, avec une escalade des notifications si nécessaire.
    *   Possibilité de définir des types d'astreinte (ex: astreinte technique, astreinte commerciale) avec des règles spécifiques.
    *   Gestion des historiques des modifications et des validations.

*   **Exemple de Code (Extrait du Contrôleur)** :

```php
<?php
// src/Controller/AstreinteController.php
namespace App\Controller;

use App\Entity\Astreinte;
use App\Form\TypeAstreinteType;
use App\Repository\AstreinteRepository;
use App\Service\AstreinteService;
use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\HttpFoundation\Request;
use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\Routing\Annotation\Route;
use Symfony\Component\Security\Core\Authorization\AuthorizationCheckerInterface;

/**
 * @Route("/astreinte")
 */
class AstreinteController extends AbstractController
{
    private $astreinteService;

    public function __construct(AstreinteService $astreinteService)
    {
        $this->astreinteService = $astreinteService;
    }

    /**
     * @Route("/", name="astreinte_index", methods={"GET"})
     */
    public function index(AstreinteRepository $astreinteRepository): Response
    {
        $astreintes = $astreinteRepository->findAll();
        return $this->render('astreinte/index.html.twig', [
            'astreintes' => $astreintes,
        ]);
    }

    /**
     * @Route("/new", name="astreinte_new", methods={"GET","POST"})
     */
    public function new(Request $request): Response
    {
        $astreinte = new Astreinte();
        $form = $this->createForm(TypeAstreinteType::class, $astreinte);
        $form->handleRequest($request);

        if ($form->isSubmitted() && $form->isValid()) {
            try {
                $this->astreinteService->createAstreinte($astreinte);
                $this->addFlash('success', 'Astreinte créée avec succès !');
                return $this->redirectToRoute('astreinte_index');
            } catch (\Exception $e) {
                $this->addFlash('error', 'Erreur lors de la création de l\'astreinte : ' . $e->getMessage());
            }
        }

        return $this->render('astreinte/new.html.twig', [
            'astreinte' => $astreinte,
            'form' => $form->createView(),
        ]);
    }

    /**
     * @Route("/{id}/validate", name="astreinte_validate", methods={"GET","POST"})
     */
    public function validate(Request $request, Astreinte $astreinte, AuthorizationCheckerInterface $authChecker): Response
    {
      if (!$authChecker->isGranted('ROLE_RESPONSABLE_ASTREINTE', $astreinte)) {
            throw $this->createAccessDeniedException('Vous n\'avez pas les droits pour valider cette astreinte.');
        }

        if ($request->isMethod('POST')) {
            try {
                $this->astreinteService->validateAstreinte($astreinte);
                $this->addFlash('success', 'Astreinte validée avec succès !');
                return $this->redirectToRoute('astreinte_index');
            } catch (\Exception $e) {
                $this->addFlash('error', 'Erreur lors de la validation de l\'astreinte : ' . $e->getMessage());
            }
        }

        return $this->render('astreinte/validate.html.twig', [
            'astreinte' => $astreinte,
        ]);
    }
}
```

*   **Interactions**:

    *   Le module interagit avec le module "Gestion des Collaborateurs" pour référencer les collaborateurs concernés par les astreintes (clé étrangère).  L'accès aux données des collaborateurs est géré via le `CollaboratorRepository`.
    *   Il peut interagir avec le module "Gestion des Utilisateurs et des Permissions" pour la gestion des droits d'accès et les validations, en utilisant le système de rôles de Symfony. L'authentification et l'autorisation sont gérées via le système de sécurité de Symfony.
    *   Il peut interagir avec le module "Gestion des Calendriers" pour exclure les jours fériés et les congés du calcul des heures d'astreinte. L'accès aux données du calendrier se fait via un service dédié (ex : `CalendarService`).
    *   Le module envoie des notifications (email, notifications in-app) aux collaborateurs et aux responsables concernés, en utilisant le `NotificationService`.
    *   Il utilise des services (ex: `AstreinteService.php`, `NotificationService.php`, `ApprovalService.php`) pour encapsuler la logique métier et les opérations récurrentes.
    *   Le module interagit avec le module "Gestion des Primes" pour le calcul et l'attribution des primes d'astreinte, si applicable.

*   **Tests**:  Des tests unitaires et fonctionnels sont essentiels pour garantir la qualité du module. Les tests doivent couvrir :

    *   **Tests Unitaires**:
        *   Validation des données d'entrée (ex: dates de début et de fin, collaborateur, etc.).  Les tests doivent vérifier que les contraintes de validation sont correctement appliquées.
        *   La logique de calcul des heures d'astreinte et des indemnités (en utilisant des données de test variées).
        *   Les règles de validation et d'approbation (en simulant différents rôles et workflows).
        *   Les interactions avec le `AstreinteService`.
    *   **Tests Fonctionnels**:
        *   La création, la lecture, la mise à jour et la suppression (CRUD) des astreintes.
        *   La validation et l'approbation des astreintes.
        *   Les interactions avec les autres modules (collaborateurs, calendriers).  Ces tests doivent simuler les appels aux services des autres modules.
        *   Les cas d'erreur et les exceptions (ex: chevauchement d'astreintes, problèmes de validation).
        *   L'envoi de notifications.
        *   L'accès aux pages protégées (tests d'autorisation).
    *   **Tests d'Intégration**:
        *   Simuler les interactions avec les modules dépendants (Collaborateurs, Calendriers, Utilisateurs & Permissions).
        *   Vérifier l'intégrité des données entre les modules.

*   **Sécurité**:

    *   **Authentification et Autorisation**:  L'accès aux fonctionnalités du module est contrôlé par le module "Gestion des Utilisateurs et des Permissions".  Les utilisateurs doivent être authentifiés et disposer des rôles appropriés pour effectuer des actions (ex: `ROLE_GESTIONNAIRE_ASTREINTES`, `ROLE_RESPONSABLE_ASTREINTE`). Le système de sécurité de Symfony est utilisé pour gérer l'authentification et l'autorisation.
    *   **Protection contre les attaques CSRF (Cross-Site Request Forgery)** :  Les formulaires doivent inclure des tokens CSRF pour prévenir les attaques.  Le composant Form de Symfony gère automatiquement la protection CSRF.
    *   **Validation des données en entrée**: Toutes les données provenant des utilisateurs (formulaires, requêtes) doivent être validées pour prévenir les injections de code et les erreurs.  Le composant Form de Symfony et les annotations de validation sont utilisés.
    *   **Protection contre les injections SQL**:  L'utilisation de l'ORM Doctrine et des requêtes paramétrées permet de prévenir les injections SQL.
    *   **Gestion des erreurs**:  Les erreurs doivent être gérées de manière sécurisée, en évitant d'afficher des informations sensibles aux utilisateurs.  Les exceptions doivent être gérées et les messages d'erreur appropriés affichés.
    *   **Protection contre les attaques XSS (Cross-Site Scripting)** :  Les données affichées dans les vues doivent être correctement échappées pour prévenir les attaques XSS.  Twig échappe automatiquement les variables par défaut.
    *   **Journalisation (Logging)** :  Les actions importantes (création, modification, suppression, validation) doivent être journalisées pour l'audit et la traçabilité.

### 2.2. Gestion des Primes

*   **Description**: Ce module gère les primes des collaborateurs, y compris la définition des types de primes, les règles de calcul, la saisie, la validation, l'approbation et l'intégration avec la paie. Le module offre une grande flexibilité pour la définition de différents types de primes et de leurs règles associées.

*   **Composants Clés**:

    *   **Entité `Prime.php`**: Définit la structure de données pour les primes. Elle contient les attributs tels que le type de prime (clé étrangère vers une entité `PrimeType`), le collaborateur concerné (clé étrangère vers l'entité `Collaborator`), le montant, la date d'attribution, la période de référence, le statut (en attente, validé, approuvé, refusé, intégré à la paie), etc. (Exemple : `src/Entity/Prime.php`)
    *   **Contrôleur `PrimeController.php`**: Gère les requêtes HTTP pour les opérations CRUD sur les primes. Il gère également les validations, les calculs, les approbations et les notifications. (Exemple : `src/Controller/PrimeController.php`)
    *   **Repository `PrimeRepository.php`**: Fournit des méthodes pour l'accès aux données des primes dans la base de données, incluant les requêtes complexes, les filtrages et les tris. (Exemple : `src/Repository/PrimeRepository.php`)
    *   **Formulaires**:  Permettent la saisie et la modification des données des primes. Ils utilisent le composant Form de Symfony pour la gestion des formulaires HTML, la validation des données et la liaison avec les entités. (ex: `TypePrimeType.php`). (Exemple : `src/Form/TypePrimeType.php`)
    *   **Templates Twig**:  Responsables de l'affichage des informations des primes. Ils utilisent le moteur de template Twig pour générer les vues HTML, CSS et JavaScript. (ex: `prime/index.html.twig`, `prime/validation-index.html.twig`). (Exemple : `templates/prime/index.html.twig`)
    *   **Services**: Le module utilise des services pour encapsuler la logique métier et les opérations récurrentes (ex: calcul des primes (`PrimeService`), notifications (`NotificationService`), intégration avec la paie (`PayrollIntegrationService`), validation des primes (`ApprovalService`)). (Exemple: `src/Service/PrimeService.php`)
    *   **Entité `PrimeType.php`**: Définit les différents types de primes (ex: prime d'objectif, prime d'ancienneté, prime de performance). Elle contient les attributs tels que le nom du type de prime, la description, les règles de calcul (ex: formule), le statut (actif, inactif).

*   **Règles Métiers**:

    *   Les primes doivent être associées à des collaborateurs valides (clé étrangère vérifiée).
    *   Les calculs des primes doivent suivre les règles définies pour chaque type de prime (ex: primes d'objectifs, primes d'ancienneté, primes de performance).  Les règles de calcul peuvent être définies dans l'entité `PrimeType` et interprétées par le `PrimeService`.
    *   Les primes doivent être validées par les responsables appropriés selon un workflow défini (rôle et hiérarchie).
    *   Gestion des primes facturables et non facturables.
    *   Intégration avec le système de paie pour l'export des données.  Un format d'export standardisé est utilisé (ex: CSV, XML) et géré par le `PayrollIntegrationService`.
    *   Prise en compte des règles fiscales et sociales en vigueur.
    *   Gestion des plafonds et des limites pour chaque type de prime.
    *   Gestion des proratisations en cas d'absence ou de départ du collaborateur.
    *   Gestion des historiques des modifications et des validations.

*   **Exemple de Code (Extrait du Contrôleur)**:

```php
<?php
// src/Controller/PrimeController.php
namespace App\Controller;

use App\Entity\Prime;
use App\Form\TypePrimeType;
use App\Repository\PrimeRepository;
use App\Service\PrimeService;
use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\HttpFoundation\Request;
use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\Routing\Annotation\Route;

/**
 * @Route("/prime")
 */
class PrimeController extends AbstractController
{
    private $primeService;

    public function __construct(PrimeService $primeService)
    {
        $this->primeService = $primeService;
    }

    /**
     * @Route("/", name="prime_index", methods={"GET"})
     */
    public function index(PrimeRepository $primeRepository): Response
    {
        return $this->render('prime/index.html.twig', [
            'primes' => $primeRepository->findAll(),
        ]);
    }

    /**
     * @Route("/new", name="prime_new", methods={"GET","POST"})
     */
    public function new(Request $request): Response
    {
        $prime = new Prime();
        $form = $this->createForm(TypePrimeType::class, $prime);
        $form->handleRequest($request);

        if ($form->isSubmitted() && $form->isValid()) {
            try {
                $this->primeService->calculatePrime($prime);
                $this->addFlash('success', 'Prime créée avec succès !');
                return $this->redirectToRoute('prime_index');
            } catch (\Exception $e) {
                $this->addFlash('error', 'Erreur lors de la création de la prime : ' . $e->getMessage());
            }
        }

        return $this->render('prime/new.html.twig', [
            'prime' => $prime,
            'form' => $form->createView(),
        ]);
    }
}
```

*   **Interactions**:

    *   Le module interagit avec le module "Gestion des Collaborateurs" pour référencer les collaborateurs. L'accès aux données des collaborateurs est géré via le `CollaboratorRepository`.
    *   Il peut interagir avec le module "Gestion des Utilisateurs et des Permissions" pour la gestion des droits d'accès et les validations. L'authentification et l'autorisation sont gérées via le système de sécurité de Symfony.
    *   Il s'intègre avec le système de paie pour l'export des données des primes, en utilisant le `PayrollIntegrationService`.
    *   Il utilise des services (ex: `PrimeService.php`, `PayrollIntegrationService.php`, `NotificationService.php`, `ApprovalService.php`) pour encapsuler la logique métier et les opérations récurrentes.

*   **Tests**: Les tests unitaires et fonctionnels sont essentiels pour valider le module. Les tests doivent couvrir :

    *   **Tests Unitaires**:
        *   Validation des données d'entrée (ex: montants, types de primes, période de référence). Les tests doivent vérifier que les contraintes de validation sont correctement appliquées.
        *   La logique de calcul des primes (en utilisant des données de test variées pour chaque type de prime).
        *   Les règles de validation et d'approbation (en simulant différents rôles et workflows).
        *   L'intégration avec le `PrimeService`.
    *   **Tests Fonctionnels**:
        *   La création, la lecture, la mise à jour et la suppression (CRUD) des primes.
        *   La validation et l'approbation des primes.
        *   L'intégration avec le système de paie (en simulant l'export des données).
        *   Les interactions avec les autres modules (collaborateurs, types de primes). Ces tests doivent simuler les appels aux services des autres modules.
        *   Les cas d'erreur et les exceptions (ex: problèmes de validation, erreurs de calcul).
        *   L'envoi de notifications.
        *   L'accès aux pages protégées (tests d'autorisation).
    *   **Tests d'Intégration**:
        *   Simuler l'intégration avec le système de paie.
        *   Simuler les interactions avec les modules dépendants (Collaborateurs, Utilisateurs & Permissions).
        *   Vérifier l'intégrité des données entre les modules.

*   **Sécurité**:

    *   **Authentification et Autorisation**: L'accès aux fonctionnalités du module est contrôlé par le module "Gestion des Utilisateurs et des Permissions".  Les utilisateurs doivent être authentifiés et disposer des rôles appropriés pour effectuer des actions (ex: `ROLE_GESTIONNAIRE_PRIMES`, `ROLE_RESPONSABLE_PRIMES`). Le système de sécurité de Symfony est utilisé pour gérer l'authentification et l'autorisation.
    *   **Protection contre les attaques CSRF (Cross-Site Request Forgery)** :  Les formulaires doivent inclure des tokens CSRF pour prévenir les attaques.  Le composant Form de Symfony gère automatiquement la protection CSRF.
    *   **Validation des données en entrée**: Toutes les données provenant des utilisateurs (formulaires, requêtes) doivent être validées pour prévenir les injections de code et les erreurs.  Le composant Form de Symfony et les annotations de validation sont utilisés.
    *   **Protection contre les injections SQL**:  L'utilisation de l'ORM Doctrine et des requêtes paramétrées permet de prévenir les injections SQL.
    *   **Gestion des erreurs**:  Les erreurs doivent être gérées de manière sécurisée, en évitant d'afficher des informations sensibles aux utilisateurs.  Les exceptions doivent être gérées et les messages d'erreur appropriés affichés.
    *   **Protection contre les attaques XSS (Cross-Site Scripting)** :  Les données affichées dans les vues doivent être correctement échappées pour prévenir les attaques XSS.  Twig échappe automatiquement les variables par défaut.
    *   **Chiffrement des données sensibles**: Les informations sensibles (ex: informations bancaires, données de paie) doivent être chiffrées au repos et en transit.
    *   **Journalisation (Logging)** :  Les actions importantes (création, modification, suppression, validation, intégration à la paie) doivent être journalisées pour l'audit et la traçabilité.

### 2.3. Gestion des Projets

*   **Description**: Ce module gère les projets, les étapes, les tâches, les affectations des ressources, le suivi de l'avancement et la gestion budgétaire. Il permet de planifier, d'exécuter et de suivre les projets de manière efficace. Il inclut également la gestion des risques et des documents associés.

*   **Composants Clés**:

    *   **Entité `Project.php`**: Définit la structure de données pour les projets. Elle contient les attributs tels que le nom du projet, la description, les dates de début et de fin, le budget, le chef de projet (clé étrangère vers l'entité `Collaborator`), le statut (en cours, terminé, annulé, en attente), etc. (Exemple : `src/Entity/Project.php`)
    *   **Contrôleur `ProjectController.php`**: Gère les requêtes HTTP pour les opérations CRUD sur les projets. Il gère également la gestion des étapes, des tâches, des affectations, du suivi de l'avancement, de la gestion budgétaire, des risques et des documents. (Exemple : `src/Controller/ProjectController.php`)
    *   **Repository `ProjectRepository.php`**: Fournit des méthodes pour l'accès aux données des projets dans la base de données, incluant les requêtes complexes, les filtrages et les tris. (Exemple : `src/Repository/ProjectRepository.php`)
    *   **Formulaires**:  Permettent la saisie et la modification des données des projets, des étapes, des tâches, des affectations, des risques et des documents. Ils utilisent le composant Form de Symfony pour la gestion des formulaires HTML, la validation des données et la liaison avec les entités. (ex: `ProjectType.php`). (Exemple : `src/Form/ProjectType.php`)
    *   **Templates Twig**:  Responsables de l'affichage des informations des projets, des étapes, des tâches, des affectations, des risques et des documents. Ils utilisent le moteur de template Twig pour générer les vues HTML, CSS et JavaScript. (ex: `project/index.html.twig`, `project/show.html.twig`). (Exemple : `templates/project/index.html.twig`)
    *   **Services**: Le module utilise des services pour encapsuler la logique métier et les opérations récurrentes (ex: calcul de l'avancement (`ProjectService`), gestion budgétaire (`BudgetService`), gestion des risques (`RiskManagementService`), notifications (`NotificationService`), gestion des documents (`DocumentService`)). (Exemple: `src/Service/ProjectService.php`)
    *   **Entité `ProjectStage.php`**:  Représente une étape d'un projet, avec des dates de début et de fin, un statut et des dépendances éventuelles.
    *   **Entité `ProjectTask.php`**: Représente une tâche d'un projet, avec une description, une date d'échéance, une affectation à un collaborateur (clé étrangère vers l'entité `Collaborator`), et un statut.
    *   **Entité `ProjectRisk.php`**:  Représente un risque lié à un projet, avec une description, une probabilité, un impact et des actions de mitigation.
    *   **Entité `ProjectDocument.php`**: Représente un document associé à un projet (ex: cahier des charges, spécifications).

*   **Règles Métiers**:

    *   Les projets doivent avoir des dates de début et de fin valides.
    *   Les étapes des projets doivent être ordonnées et avoir des dates de début et de fin valides, ainsi que des dépendances possibles entre elles.
    *   Les collaborateurs affectés aux projets doivent être valides (clé étrangère vérifiée) et disponibles (prise en compte des congés, absences, etc.).
    *   Gestion des budgets et des dépenses par projet, avec des alertes en cas de dépassement de budget.
    *   Suivi de l'avancement des projets, avec des indicateurs de performance clés (KPIs).
    *   Gestion des alertes en cas de dépassement de budget ou de retard.
    *   Gestion des risques et des actions correctives, avec une classification des risques (probabilité, impact).
    *   Gestion des documents associés aux projets (ex: cahier des charges, spécifications, comptes rendus).
    *   Gestion des droits d'accès aux projets (ex: chef de projet, membres de l'équipe, clients).
    *   Gestion des jalons et des livrables.
    *   Intégration avec des outils de gestion de projet externes (ex: Jira, Trello) via des API.

*   **Exemple de Code (Extrait du Contrôleur)**:

```php
<?php
// src/Controller/ProjectController.php
namespace App\Controller;

use App\Entity\Project;
use App\Form\ProjectType;
use App\Repository\ProjectRepository;
use App\Service\ProjectService;
use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\HttpFoundation\Request;
use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\Routing\Annotation\Route;

/**
 * @Route("/project")
 */
class ProjectController extends AbstractController
{
    private $projectService;

    public function __construct(ProjectService $projectService)
    {
        $this->projectService = $projectService;
    }

    /**
     * @Route("/", name="project_index", methods={"GET"})
     */
    public function index(ProjectRepository $projectRepository): Response
    {
        return $this->render('project/index.html.twig', [
            'projects' => $projectRepository->findAll(),
        ]);
    }

    /**
     * @Route("/new", name="project_new", methods={"GET","POST"})
     */
    public function new(Request $request): Response
    {
        $project = new Project();
        $form = $this->createForm(ProjectType::class, $project);
        $form->handleRequest($request);

        if ($form->isSubmitted() && $form->isValid()) {
            try {
                $this->projectService->createProject($project);
                $this->addFlash('success', 'Projet créé avec succès !');
                return $this->redirectToRoute('project_index');
            } catch (\Exception $e) {
                $this->addFlash('error', 'Erreur lors de la création du projet : ' . $e->getMessage());
            }
        }

        return $this->render('project/new.html.twig', [
            'project' => $project,
            'form' => $form->createView(),
        ]);
    }
}
```

*   **Interactions**:

    *   Le module interagit avec le module "Gestion des Collaborateurs" pour les affectations des collaborateurs aux projets. L'accès aux données des collaborateurs est géré via le `CollaboratorRepository`.
    *   Il interagit avec le module "Gestion des Dépenses" pour suivre les dépenses des projets.
    *   Il peut interagir avec le module "Gestion des Documents" pour la gestion des documents associés aux projets.
    *   Il utilise des services (ex: `ProjectService.php`, `BudgetService.php`, `RiskManagementService.php`, `NotificationService.php`, `DocumentService.php`) pour encapsuler la logique métier et les opérations récurrentes.

*   **Tests**: Les tests unitaires et fonctionnels sont cruciaux pour la qualité du module. Les tests doivent couvrir :

    *   **Tests Unitaires**:
        *   Validation des données d'entrée (ex: dates, budgets, chef de projet, etc.). Les tests doivent vérifier que les contraintes de validation sont correctement appliquées.
        *   La gestion des étapes et des tâches (en testant les relations et les dépendances).
        *   Les affectations des ressources (en vérifiant la disponibilité des collaborateurs).
        *   Le calcul de l'avancement du projet.
        *   La gestion budgétaire (calcul des dépenses, alertes en cas de dépassement).
        *   La gestion des risques (évaluation de la probabilité et de l'impact).
        *   Les interactions avec le `ProjectService`.
    *   **Tests Fonctionnels**:
        *   La création, la lecture, la mise à jour et la suppression (CRUD) des projets, des étapes, des tâches et des affectations.
        *   Le suivi de l'avancement des projets.
        *   La gestion budgétaire.
        *   La gestion des risques.
        *   L'attachement et la gestion des documents.
        *   Les interactions avec les autres modules (collaborateurs, dépenses).  Ces tests doivent simuler les appels aux services des autres modules.
        *   Les cas d'erreur et les exceptions (ex: chevauchement des dates, dépassement de budget).
        *   L'envoi de notifications.
        *   L'accès aux pages protégées (tests d'autorisation).
    *   **Tests d'Intégration**:
        *   Simuler les interactions avec les modules dépendants (Collaborateurs, Dépenses, Documents, Utilisateurs & Permissions).
        *   Vérifier l'intégrité des données entre les modules.

*   **Sécurité**:

    *   **Authentification et Autorisation**: L'accès aux fonctionnalités du module est contrôlé par le module "Gestion des Utilisateurs et des Permissions".  Les utilisateurs doivent être authentifiés et disposer des rôles appropriés pour effectuer des actions (ex: `ROLE_CHEF_DE_PROJET`, `ROLE_GESTIONNAIRE_PROJETS`). Le système de sécurité de Symfony est utilisé pour gérer l'authentification et l'autorisation.
    *   **Protection contre les attaques CSRF (Cross-Site Request Forgery)** :  Les formulaires doivent inclure des tokens CSRF pour prévenir les attaques.  Le composant Form de Symfony gère automatiquement la protection CSRF.
    *   **Validation des données en entrée**: Toutes les données provenant des utilisateurs (formulaires, requêtes) doivent être validées pour prévenir les injections de code et les erreurs.  Le composant Form de Symfony et les annotations de validation sont utilisés.
    *   **Protection contre les injections SQL**:  L'utilisation de l'ORM Doctrine et des requêtes paramétrées permet de prévenir les injections SQL.
    *   **Gestion des erreurs**:  Les erreurs doivent être gérées de manière sécurisée, en évitant d'afficher des informations sensibles aux utilisateurs.  Les exceptions doivent être gérées et les messages d'erreur appropriés affichés.
    *   **Protection contre les attaques XSS (Cross-Site Scripting)** :  Les données aff

---

# Règles Métiers

---

```wiki
== RÈGLES MÉTIERS ==

### Introduction

Cette section documente les règles métiers et de gestion implémentées dans le projet WacitV2. Ces règles, issues de l'analyse du code source, des fichiers de configuration et des spécifications fonctionnelles, sont essentielles pour la compréhension, la maintenance et l'évolution du système. Elles guident les développeurs, les testeurs et les nouveaux collaborateurs dans la modification, l'extension et la validation des fonctionnalités. Cette documentation est maintenue à jour pour refléter les évolutions du code et des exigences métier. La connaissance et le respect de ces règles sont impératifs pour assurer la cohérence, la fiabilité et la conformité de l'application.

### Vue d'ensemble

Les règles métiers de WacitV2 couvrent plusieurs domaines clés de l'application. Cela inclut, mais ne se limite pas à : la gestion des astreintes, des primes, des projets, des dépenses, des collaborateurs, des utilisateurs, des calendriers et des échanges de devises. Ces règles sont implémentées en PHP (Symfony), en JavaScript (côté client) et configurées dans des fichiers YAML. L'objectif principal est d'assurer la cohérence, la validité, la sécurité et la conformité des données et des processus métier. Cette documentation détaille, pour chaque module, les règles métier spécifiques, les règles de gestion associées, ainsi que des exemples de code pertinents.

### Structure des Modules

Chaque module est présenté selon la structure suivante afin de faciliter la compréhension et la consultation :

*   **Description:** Une brève explication de la fonctionnalité du module et de son rôle dans l'application.
*   **Fichiers Pertinents:** Une liste des fichiers sources (contrôleurs, entités, formulaires, fichiers JavaScript, fichiers de configuration YAML) impliqués dans l'implémentation des règles métiers du module. Cette liste permet de localiser rapidement le code source correspondant à une règle donnée.
*   **Règles Métiers:** Les règles spécifiques au domaine métier du module. Ces règles définissent les contraintes et les validations qui s'appliquent aux données et aux processus métier.
*   **Règles de Gestion:** Les règles liées à l'administration et à l'utilisation du module. Elles traitent des aspects tels que les permissions, les workflows de validation, et les notifications.
*   **Exemples de Code:** Des extraits de code illustrant l'implémentation de certaines règles (PHP, JavaScript, YAML). Ces exemples permettent de mieux comprendre comment les règles sont appliquées dans le code. Les exemples sont choisis pour illustrer les points clés de chaque règle.
*   **Diagrammes (si pertinent):** Des diagrammes (UML, flux de données, etc.) peuvent être ajoutés pour illustrer les processus métier et les relations entre les différents composants du module.

### Règles par Module

#### Gestion des Astreintes

*   **Description:** Ce module gère le processus de gestion des astreintes des collaborateurs, incluant leur création, leur modification, leur validation, leur suivi et leur rémunération. Il permet d'assurer la disponibilité et la réactivité du personnel en dehors des heures de travail normales.

*   **Fichiers Pertinents:**

    *   `src/Controller/AstreinteController.php`
    *   `src/Entity/Astreinte.php`
    *   `src/Form/Type/AstreinteType.php`
    *   `public/assets/js/astreinte.js` (Validation et interactions côté client)
    *   `public/assets/js/astreinte-validation.js` (Validation spécifique des champs)
    *   `public/assets/js/astreinte-exceptional.js` (Gestion des cas exceptionnels, tels que les astreintes de nuit, de week-end, etc.)
    *   `src/Repository/AstreinteRepository.php` (Requêtes spécifiques pour la recherche et le calcul des astreintes)
    *   `src/Service/AstreinteService.php` (Logique métier liée aux astreintes, calculs, etc.)

*   **Règles Métiers:**

    *   **Validation des Dates:**
        *   **Règle:** Une astreinte doit toujours avoir une date et une heure de début et une date et une heure de fin valides.
        *   **Règle:** La date et l'heure de fin doivent être postérieures ou égales à la date et l'heure de début.
        *   **Implémentation:** Cette validation est assurée au niveau du formulaire (`src/Form/Type/AstreinteType.php`) en utilisant les contraintes de validation Symfony (`Assert\DateTime`). Elle est renforcée en JavaScript (`public/assets/js/astreinte-validation.js`) pour une validation en temps réel et une meilleure expérience utilisateur.
    *   **Collaborateur Obligatoire:**
        *   **Règle:** Chaque astreinte doit être associée à un collaborateur existant.
        *   **Implémentation:** Validation côté serveur dans le contrôleur (`AstreinteController.php`) et les services, garantissant l'intégrité des données. Une validation côté client est également présente pour une meilleure réactivité.
    *   **Statut de l'Astreinte:**
        *   **Règle:** Les statuts possibles d'une astreinte sont : `active`, `validée`, `refusée`, `annulée`.
        *   **Règle:** Les transitions de statut sont réglementées :
            *   Une astreinte avec le statut `active` peut être validée ou refusée.
            *   Une astreinte avec le statut `validée` ne peut plus être modifiée.
            *   Une astreinte avec le statut `annulée` ne peut plus être modifiée.
        *   **Implémentation:** La gestion des statuts et des transitions est implémentée dans le code (`AstreinteController.php`, entité `Astreinte.php`, et potentiellement dans le service `AstreinteService.php`) et influencée par les templates (vues). Des vérifications sont effectuées avant chaque changement de statut pour garantir la cohérence.
    *   **Exceptions:**
        *   **Règle:** Gestion des cas exceptionnels, tels que les astreintes non validées après un certain délai (afin d'assurer un suivi), ou les astreintes exceptionnelles (ex: astreintes de nuit, de week-end, jours fériés).
        *   **Implémentation:** La logique est implémentée dans `public/assets/js/astreinte-exceptional.js` (côté client) et `AstreinteController.php` et/ou `AstreinteService.php` (côté serveur). L'utilisation d'un service permet de centraliser la logique de gestion des exceptions et de faciliter les tests.
    *   **Calcul des Heures:**
        *   **Règle:** Calcul précis des heures d'astreinte en fonction des dates et heures de début et de fin, ainsi que du type d'astreinte (jour, nuit, week-end, etc.). Ce calcul est essentiel pour la rémunération.
        *   **Implémentation:** Implémentation dans le service `AstreinteService.php` et/ou le repository `AstreinteRepository.php`.  Le service peut exposer des méthodes comme `calculateHours()`, `calculateNightHours()`, etc.

*   **Règles de Gestion:**

    *   **Permissions:**
        *   **Règle:** Seuls les utilisateurs disposant du rôle approprié (ex: `ROLE_ADMIN`, `ROLE_MANAGER`, `ROLE_RH`) peuvent créer, modifier, valider ou refuser des astreintes. La séparation des rôles permet de définir des responsabilités claires.
        *   **Implémentation:** Le contrôle d'accès est géré dans `AstreinteController.php` en utilisant les annotations `@IsGranted` de Symfony, ainsi que via le système de sécurité Symfony basé sur les rôles et les permissions.
    *   **Notifications:**
        *   **Règle:** Envoi de notifications par e-mail aux collaborateurs concernés et aux responsables lors des événements suivants : création, modification, validation, refus et annulation d'une astreinte. Cela assure une communication efficace.
        *   **Implémentation:** Utilisation du service `NotificationService` (à documenter séparément). Ce service devrait fournir des méthodes spécifiques telles que `sendAstreinteCreatedNotification()`, `sendAstreinteValidatedNotification()`, etc. L'utilisation d'une queue de messages (avec Messenger de Symfony par exemple) est fortement recommandée pour gérer les envois de notifications de manière asynchrone.
    *   **Archivage:**
        *   **Règle:** Archivage des astreintes validées et/ou refusées après une certaine période (ex: 1 an) pour des raisons de conformité et de gestion des données.
        *   **Implémentation:**  La mise en place d'une tâche planifiée (commande Symfony) utilisant le service `AstreinteService` et le repository pour archiver les astreintes.

*   **Exemples de Code:**

    ```php
    // Exemple de validation dans AstreinteController.php
    use Symfony\Component\Validator\Constraints as Assert;
    use Symfony\Component\HttpFoundation\Response;
    use Symfony\Component\Routing\Annotation\Route;
    use App\Entity\Astreinte;
    use Doctrine\ORM\EntityManagerInterface;
    use App\Service\AstreinteService; // Importation du service AstreinteService

    #[Route('/astreinte')]
    class AstreinteController extends AbstractController
    {
        private $entityManager;
        private $astreinteService; // Injection du service

        public function __construct(EntityManagerInterface $entityManager, AstreinteService $astreinteService)
        {
            $this->entityManager = $entityManager;
            $this->astreinteService = $astreinteService; // Initialisation du service
        }

        #[Route('/valider/{id}', name: 'astreinte_valider')]
        public function validerAstreinte(Astreinte $astreinte): Response
        {
            if ($astreinte->getStatus() !== 'active') {
                $this->addFlash('error', 'L\'astreinte ne peut pas être validée car son statut n\'est pas "active".');
                return $this->redirectToRoute('astreinte_index');
            }

            // Vérifications supplémentaires (ex: chevauchement avec d'autres astreintes)
            if ($this->astreinteService->isAstreinteOverlapping($astreinte)) {
                $this->addFlash('error', 'L\'astreinte chevauche une autre astreinte.');
                return $this->redirectToRoute('astreinte_index');
            }

            $astreinte->setStatus('validée');
            $this->entityManager->flush();

            // Envoi de la notification de validation
            $this->astreinteService->sendValidationNotification($astreinte);

            $this->addFlash('success', 'L\'astreinte a été validée avec succès.');
            return $this->redirectToRoute('astreinte_index');
        }
    }
    ```

    ```javascript
    // Exemple de validation côté client (public/assets/js/astreinte-validation.js)
    function validateAstreinte() {
      const dateDebut = document.getElementById('astreinte_dateDebut').value;
      const dateFin = document.getElementById('astreinte_dateFin').value;

      if (!isValidDate(dateDebut) || !isValidDate(dateFin)) {
          return "Veuillez saisir des dates de début et de fin valides.";
      }

      if (dateFin < dateDebut) {
          return "La date de fin doit être postérieure ou égale à la date de début.";
      }

      // Autres validations côté client...
      return ""; // Retourne une chaîne vide si la validation est réussie
    }

    function isValidDate(dateString) {
        return !isNaN(new Date(dateString).getTime());
    }
    ```

#### Gestion des Primes

*   **Description:** Ce module gère l'ensemble du processus de gestion des primes des collaborateurs, incluant leur calcul, leur validation, leur paiement et le suivi de leur historique. Il permet de récompenser les performances, l'ancienneté et d'autres facteurs contribuant à la motivation des employés.

*   **Fichiers Pertinents:**

    *   `src/Controller/PrimeController.php`
    *   `src/Entity/Prime.php`
    *   `src/Entity/TypePrime.php` (si applicable)
    *   `src/Form/Type/PrimeType.php`
    *   `public/assets/js/prime.js` (Validation et interactions côté client)
    *   `src/Service/PrimeService.php` (Service dédié au calcul des primes)
    *   `src/Repository/PrimeRepository.php` (Requêtes spécifiques pour la recherche et le calcul des primes)
    *   `src/Command/ImportPrimeCommand.php` (Commande pour l'importation de primes)

*   **Règles Métiers:**

    *   **Types de Primes:**
        *   **Règle:** Définition des différents types de primes disponibles (ex: prime de performance, prime d'ancienneté, prime de vacances, bonus exceptionnel, etc.).
        *   **Implémentation:** Les types de primes peuvent être définis dans une entité dédiée (`TypePrime.php`) et gérés via une interface d'administration. Chaque type de prime est associé à un code unique, un libellé et des règles de calcul spécifiques.
    *   **Calcul des Primes:**
        *   **Règle:** Calcul des primes basé sur des règles spécifiques à chaque type de prime. Ces règles peuvent inclure le salaire de base, le pourcentage, le nombre d'années d'ancienneté, des objectifs atteints, etc.
        *   **Implémentation:** La logique de calcul est implémentée dans le service `PrimeService.php` ou dans le repository `PrimeRepository.php`. L'utilisation d'un service permet de centraliser la logique de calcul, de faciliter les tests et de gérer les évolutions des règles de calcul.
    *   **Validation des Montants:**
        *   **Règle:** Les montants des primes doivent être positifs et valides.
        *   **Implémentation:** La validation est effectuée au niveau du formulaire (`src/Form/Type/PrimeType.php`) en utilisant les contraintes de validation Symfony (`Assert\Positive`, `Assert\Type`).
    *   **Période de Paiement:**
        *   **Règle:** Définition des périodes de paiement (mensuelle, trimestrielle, annuelle, etc.).
        *   **Implémentation:** Géré dans le code (ex: dans l'entité `Prime.php`, avec un attribut `periodePaiement` de type `string` ou `enum` et/ou les services associés). Chaque prime est toujours associée à une période de paiement.

*   **Règles de Gestion:**

    *   **Processus de Validation:**
        *   **Règle:** Mise en place d'un processus de validation des primes avant le paiement. Ce processus garantit la conformité et le respect des procédures.
        *   **Implémentation:** Le processus est géré dans `PrimeController.php` et dans le service `PrimeService.php`. Les primes peuvent avoir différents statuts : `brouillon`, `soumise`, `validée`, `refusée`, `payée`. Des rôles spécifiques (ex: `ROLE_MANAGER`, `ROLE_PAYROLL`) sont définis pour les différentes étapes du processus.
    *   **Permissions:**
        *   **Règle:** Contrôle d'accès pour la création, la modification, la validation et le paiement des primes. La sécurité est essentielle pour la confidentialité des informations.
        *   **Implémentation:** Basé sur les rôles et les permissions (ex: `ROLE_ADMIN`, `ROLE_PAYROLL`, `ROLE_MANAGER`). Le contrôle d'accès est géré dans `PrimeController.php` et dans les templates en utilisant les annotations `@IsGranted` de Symfony.
    *   **Importation de Primes:**
        *   **Règle:** Possibilité d'importer des primes depuis des fichiers (ex: CSV, Excel). Cette fonctionnalité permet de gagner du temps et de réduire les erreurs manuelles.
        *   **Implémentation:** Implémenté dans `PrimeController.php` et/ou une commande Symfony (`ImportPrimeCommand.php`).  Des étapes de validation des données importées, de gestion des erreurs et de journalisation sont mises en place. L'utilisation d'une librairie d'importation de fichiers (comme `League\Csv`) est recommandée.
    *   **Audit et Historisation:**
        *   **Règle:** Archivage des informations relatives aux primes, y compris les modifications, les validations et les paiements.
        *   **Implémentation:** Utilisation du système d'audit de Doctrine ou création d'une table d'historique.

*   **Exemples de Code:**

    ```php
    // Exemple de calcul de prime (dans le service PrimeService.php)
    namespace App\Service;

    use App\Entity\Prime;
    use App\Entity\TypePrime;
    use App\Repository\PrimeRepository; // Injection du repository

    class PrimeService {
        private $primeRepository; // Déclaration du repository

        public function __construct(PrimeRepository $primeRepository)
        {
            $this->primeRepository = $primeRepository; // Initialisation du repository
        }

        public function calculerPrime(Prime $prime): float
        {
            $typePrime = $prime->getTypePrime();

            if (!$typePrime instanceof TypePrime) {
                throw new \InvalidArgumentException('Le type de prime est invalide.');
            }

            switch ($typePrime->getCode()) {
                case 'PERF':
                    return $prime->getSalaireBase() * $prime->getPourcentage() / 100;
                case 'ANC':
                    return $this->calculerPrimeAnciennete($prime);
                default:
                    return 0.0;
            }
        }

        private function calculerPrimeAnciennete(Prime $prime): float
        {
            // Logique complexe pour le calcul de la prime d'ancienneté
            $anciennete = $this->primeRepository->calculerAnciennete($prime->getCollaborateur()); // Utilisation du repository
            return $prime->getSalaireBase() * (0.01 * $anciennete); // Exemple
        }
    }
    ```

#### Gestion des Projets

*   **Description:** Ce module permet la gestion des projets, incluant leur planification, leur suivi, l'affectation des ressources, et le suivi des livrables. Il assure une gestion efficace des projets et une collaboration optimale entre les équipes.

*   **Fichiers Pertinents:**

    *   `src/Controller/ProjectController.php`
    *   `src/Entity/Project.php`
    *   `src/Form/Type/ProjectType.php`
    *   `public/assets/js/project.js` (ou `newproject.js`, `listprojects.js`)
    *   `src/Entity/CollaboratorProject.php` (Entité gérant l'association collaborateurs / projets)
    *   `src/Repository/ProjectRepository.php`
    *   `src/Service/ProjectService.php`

*   **Règles Métiers:**

    *   **Statut du Projet:**
        *   **Règle:** Définition des statuts possibles d'un projet (ex: 'En cours', 'Terminé', 'Annulé', 'En attente', 'Reporté').
        *   **Implémentation:** Géré dans l'entité `Project.php` avec un champ `status` de type `string` ou `enum`.  Utilisé dans `ProjectController.php` et les templates pour afficher l'état du projet.
    *   **Dates de Début et de Fin:**
        *   **Règle:** Validation des dates de début et de fin du projet.
        *   **Règle:** La date de fin doit être postérieure ou égale à la date de début.
        *   **Implémentation:** Validation dans le formulaire (`ProjectType.php`) en utilisant les contraintes de validation Symfony (`Assert\GreaterThanOrEqual`). L'utilisation d'un widget de type "date" permet d'améliorer l'expérience utilisateur.
    *   **Association des Collaborateurs:**
        *   **Règle:** Les collaborateurs sont associés aux projets avec des rôles spécifiques (ex: Chef de projet, Développeur, Testeur, Client). Cette association permet de gérer les responsabilités et les permissions au sein du projet.
        *   **Implémentation:** Gestion des rôles et des permissions au niveau du projet. Utilisation d'une entité de liaison `CollaboratorProject` avec une relation ManyToMany entre `Project` et `Collaborator`.
    *   **Validation des Données du Projet:**
        *   **Règle:** Vérification de la cohérence des informations du projet (ex: budget, durée, dates). Cette validation garantit l'intégrité des données et la faisabilité du projet.
        *   **Règle:** Validation des champs obligatoires (nom, dates, budget, etc.).
        *   **Implémentation:** Validation dans le formulaire (`ProjectType.php`) et/ou le contrôleur (`ProjectController.php`). Utilisation des contraintes de validation Symfony.

*   **Règles de Gestion:**

    *   **Validation par les Responsables de Projet:**
        *   **Règle:** Autorisation pour les responsables de projet de valider les informations de chaque projet, avant le démarrage ou la clôture.
        *   **Implémentation:** Géré dans le contrôleur et via les permissions. Processus de validation multi-niveaux possible, avec des statuts de validation spécifiques.
    *   **Permissions:**
        *   **Règle:** Contrôle d'accès pour la création, la modification, la suppression et la consultation des projets. La sécurité est primordiale pour la confidentialité des informations.
        *   **Implémentation:** Basé sur les rôles et les permissions (ex: `ROLE_ADMIN`, `ROLE_PROJECT_MANAGER`, `ROLE_USER`). Le contrôle d'accès est géré dans `ProjectController.php` en utilisant les annotations `@IsGranted` de Symfony.

*   **Exemples de Code:**

    ```php
    // Exemple de validation d'un formulaire de projet (dans ProjectType.php)
    use Symfony\Component\Form\AbstractType;
    use Symfony\Component\Form\FormBuilderInterface;
    use Symfony\Component\OptionsResolver\OptionsResolver;
    use Symfony\Component\Validator\Constraints as Assert;
    use Symfony\Component\Form\Extension\Core\Type\TextType;
    use Symfony\Component\Form\Extension\Core\Type\DateType;
    use App\Entity\Project; // Importation de l'entité Project

    class ProjectType extends AbstractType
    {
        public function buildForm(FormBuilderInterface $builder, array $options): void
        {
            $builder
                ->add('nom', TextType::class, [
                    'label' => 'Nom du projet',
                    'constraints' => [
                        new Assert\NotBlank(['message' => 'Le nom du projet ne peut pas être vide.']),
                        new Assert\Length(['min' => 2, 'minMessage' => 'Le nom doit comporter au moins {{ limit }} caractères.']),
                    ],
                ])
                ->add('dateDebut', DateType::class, [
                    'label' => 'Date de début',
                    'widget' => 'single_text', // Utilisation du widget texte pour un affichage adapté
                    'constraints' => [
                        new Assert\NotBlank(['message' => 'La date de début est obligatoire.']),
                    ],
                ])
                ->add('dateFin', DateType::class, [
                    'label' => 'Date de fin',
                    'widget' => 'single_text', // Utilisation du widget texte pour un affichage adapté
                    'constraints' => [
                        new Assert\NotBlank(['message' => 'La date de fin est obligatoire.']),
                        new Assert\GreaterThanOrEqual(
                            ['propertyPath' => 'dateDebut', 'message' => 'La date de fin doit être postérieure ou égale à la date de début.']
                        ),
                    ],
                ]);
                // ... Autres champs ...
        }

        public function configureOptions(OptionsResolver $resolver): void
        {
            $resolver->setDefaults([
                'data_class' => Project::class, // Assurez-vous de spécifier la classe de l'entité Project
            ]);
        }
    }
    ```

#### Gestion des Dépenses

*   **Description:** Ce module permet la gestion des dépenses, incluant les achats, les frais de déplacement, les fournitures, etc. Il facilite le suivi des dépenses, le respect des budgets et la conformité avec les politiques de l'entreprise.

*   **Fichiers Pertinents:**

    *   `src/Controller/DepenseController.php`
    *   `src/Entity/Depense.php`
    *   `src/Entity/TypeDepense.php` (si applicable)
    *   `src/Form/Type/DepenseType.php`
    *   `src/Repository/DepenseRepository.php`
    *   `src/Service/DepenseService.php`

*   **Règles Métiers:**

    *   **Types de Dépenses:**
        *   **Règle:** Définition des types de dépenses (ex: "Frais de déplacement", "Fournitures de bureau", "Restaurant").
        *   **Implémentation:** Les types de dépenses peuvent être définis dans une entité dédiée (`TypeDepense.php`) et gérés via une interface d'administration. Chaque type de dépense est associé à un code unique et un libellé.
    *   **Devise:**
        *   **Règle:** Toutes les dépenses doivent être associées à une devise. La devise est obligatoire.
        *   **Implémentation:** La devise est un attribut de l'entité `Depense.php`, de type `string` ou `enum`.  Une contrainte de validation est mise en place pour garantir que la devise est une valeur valide.
    *   **Validation des Montants:**
        *   **Règle:** Les montants des dépenses doivent être positifs et valides.
        *   **Implémentation:** La validation est effectuée au niveau du formulaire (`DepenseType.php`) en utilisant les contraintes de validation Symfony (`Assert\Positive`, `Assert\Type`).
    *   **Statut de Dépense:**
        *   **Règle:** Définition des statuts possibles (ex: "En attente", "Validée", "Refusée", "Payée", "Remboursée"). Les statuts permettent de suivre l'état d'avancement de la dépense.
        *   **Implémentation:** Le statut est un attribut de l'entité `Depense.php`, de type `string` ou `enum`. Les transitions de statut sont gérées dans `DepenseController.php` et le service `DepenseService.php`.
    *   **Association Projet/Collaborateur:**
        *   **Règle:** Les dépenses peuvent être associées à un projet et/ou à un collaborateur.
        *   **Implémentation:** Relations ManyToOne avec les entités `Project` et `Collaborator` dans l'entité `Depense.php`. La relation avec le projet et/ou le collaborateur est optionnelle.

*   **Règles de Gestion:**

    *   **Processus de Validation:**
        *   **Règle:** Mise en place d'un processus de validation des dépenses (ex: approbation par un responsable hiérarchique).
        *   **Implémentation:** Le processus de validation est géré dans `DepenseController.php` et dans le service `DepenseService.php`.  Le service gère les transitions de statut, les notifications et l'enregistrement des informations de validation. Possibilité de workflows de validation multi-niveaux.
    *   **Permissions:**
        *   **Règle:** Contrôle d'accès pour la création, la modification, la validation et le paiement des dépenses. La sécurité est essentielle pour la gestion des informations financières.
        *   **Implémentation:** Basé sur les rôles et les permissions (ex: `ROLE_ADMIN`, `ROLE_FINANCE`, `ROLE_MANAGER`). Le contrôle d'accès est géré dans `DepenseController.php` et dans les templates en utilisant les annotations `@IsGranted` de Symfony.
    *   **Justificatifs:**
        *   **Règle:** Possibilité de joindre des justificatifs de dépenses (ex: factures, reçus). Cette fonctionnalité facilite le suivi et la conformité.
        *   **Implémentation:** Gestion du stockage et de l'accès aux justificatifs (stockage dans un dossier, base de données ou service de stockage cloud). Utilisation d'un champ `file` dans le formulaire et gestion de l'upload.
    *   **Budget et Alertes:**
        *   **Règle:** Définition des budgets par projet ou par collaborateur. Alertes en cas de dépassement du budget.
        *   **Implémentation:**  Ajout de champs de budget dans les entités `Project` et/ou `Collaborator`. Calcul des dépenses et comparaison avec les budgets dans le service `DepenseService.php`. Envoi de notifications si nécessaire.
    *   **Intégration Comptable:**
        *   **Règle:**  Export des données de dépenses vers un système comptable.
        *   **Implémentation:** Mise en place d'une commande Symfony pour exporter les données au format requis (CSV, XML, etc.).  Ou intégration directe via une API.

*   **Exemples de Code:**

    ```php
    // Exemple d'association d'une dépense à un projet (dans DepenseController.php)
    use Symfony\Component\Routing\Annotation\Route;
    use Symfony\Component\HttpFoundation\Response;
    use App\Entity\Depense;
    use App\Entity\Project;
    use Doctrine\ORM\EntityManagerInterface;

    #[Route('/depense')]
    class DepenseController extends AbstractController
    {
        private $entityManager;

        public function __construct(EntityManagerInterface $entityManager)
        {
            $this->entityManager = $entityManager;
        }

        #[Route('/{id}/associer-projet/{projectId}', name: 'depense_associer_projet')]
        #[IsGranted('ROLE_FINANCE')] // Exemple de contrôle d'accès
        public function associerProjet(Depense $depense, int $projectId): Response
        {
            $projet = $this->entityManager->getRepository(Project::class)->find($projectId);

            if (!$projet) {
                throw $this->createNotFoundException('Projet non trouvé');
            }

            $depense->setProjet($projet);
            $this->entityManager->flush();

            // Redirection vers la liste des dépenses ou la page de détail de la dépense
            return $this->redirectToRoute('depense_index'); // ou depense_show
        }
    }
    ```

#### Gestion des Collaborateurs

*   **Description:** Ce module permet la gestion complète des informations relatives aux collaborateurs de l'entreprise. Il inclut les données personnelles, les informations de contact, les informations professionnelles, les informations de connexion et les rôles et permissions.

*   **Fichiers Pertinents:**

    *   `src/Controller/CollaboratorController.php`
    *   `src/Entity/Collaborator.php`
    *   `src/Form/Type/CollaboratorType.php`
    *   `public/assets/js/collaborator.js` (Validation et interactions côté client)
    *   `src/Repository/CollaboratorRepository.php`
    *   `src/Service/CollaboratorService.php`

*   **Règles Métiers:**

    *   **Informations Obligatoires:**
        *   **Règle:** Définition des champs obligatoires pour la création d'un collaborateur (Nom, Prénom, Date de naissance, Adresse e-mail, Département, etc.).  Ces informations sont cruciales pour l'identification et la gestion des collaborateurs.
        *   **Implémentation:** La validation de ces champs est assurée au niveau du formulaire (`CollaboratorType.php`) en utilisant les contraintes de validation Symfony (`Assert\NotBlank`, `Assert\Length`).
    *   **Format des Emails:**
        *   **Règle:** Validation du format des adresses e-mail.  Une adresse e-mail valide est indispensable pour la communication.
        *   **Implémentation:** Utilisation des contraintes de validation Symfony (`Assert\Email`).  Des validations JavaScript peuvent être ajoutées pour une meilleure expérience utilisateur et une validation en temps réel.
    *   **Statut d'Activité:**
        *   **Règle:** Les collaborateurs peuvent avoir un statut `actif` ou `inactif`.  Le statut `actif` est généralement le statut par défaut.
        *   **Implémentation:** Le statut est un attribut de l'entité `Collaborator.php`, de type `boolean` (ou `enum` si d'autres statuts sont nécessaires).  Le contrôleur permet d'activer/désactiver un collaborateur.
    *   **Département:**
        *   **Règle:** Les collaborateurs doivent appartenir à un département.  Le département est essentiel pour l'organisation et la gestion des ressources.
        *   **Implémentation:** Relation ManyToOne avec l'entité `Department`.  Le département est sélectionné via une liste déroulante dans le formulaire.
    *   **Numéro de Sécurité Sociale (NIR):**
        *   **Règle:** Validation du format du numéro de sécurité sociale (NIR).
        *   **Implémentation:**  Ajout d'un champ `nir` dans l'entité `Collaborator`. Utilisation d'une librairie tierce ou d'une fonction personnalisée pour valider le format du NIR.

*   **Règles de Gestion:**

    *   **Authentification des Collaborateurs:**
        *   **Règle:** Les collaborateurs peuvent avoir un compte utilisateur et se connecter à l'application.  Cette fonctionnalité est nécessaire pour l'accès aux fonctionnalités de l'application.
        *   **Implémentation:** Gestion des informations d'identification (nom d'utilisateur, mot de passe) dans une entité `User` (ou ajout de ces informations directement dans l'entité `Collaborator` si les collaborateurs sont aussi des utilisateurs). Utilisation du composant Security de Symfony pour la gestion de l'authentification.
    *   **Permissions:**
        *   **Règle:** Gestion des rôles et des permissions des collaborateurs.  Les rôles définissent les droits d'accès aux différentes fonctionnalités de l'application.
        *   **Implémentation:** Définition des rôles et des permissions dans `security.yaml`.  Contrôle d'accès dans `CollaboratorController.php` et les templates en utilisant les annotations `@IsGranted` de Symfony.
    *   **Importation de Collaborateurs:**
        *   **Règle:** Possibilité d'importer des collaborateurs depuis des fichiers (CSV, Excel, etc.).  Cette fonctionnalité permet de faciliter l'intégration et la mise à jour des données.
        *   **Implémentation:** Implémenté dans `CollaboratorController.php` et/ou une commande Symfony. Validation des données importées, gestion des erreurs et journalisation.  L'utilisation d'une librairie d'importation de fichiers est recommandée.
    *   **Gestion des Mots de Passe:**
        *   **Règle:** Application de règles de sécurité pour les mots de passe (longueur minimale, complexité, etc.).
        *   **Implémentation:** Configuration des règles de sécurité dans `security.yaml` (ou via des paramètres). Utilisation du `UserPasswordEncoderInterface` pour encoder les mots de passe.
    *   **Gestion des Données Personnelles (RGPD):**
        *   **Règle:** Conformité avec le Règlement Général sur la Protection des Données (RGPD).

---

# Règles de Gestion

---

```wiki
# Règles de Gestion et Contraintes Système

## Introduction

Cette section documente les règles de gestion (ou *business rules*) et les contraintes système appliquées au sein de l'application WacitV2. Elle est essentielle pour comprendre le fonctionnement de l'application, garantir la cohérence et l'intégrité des données, et assurer le respect des exigences métier. Ces règles et contraintes sont cruciales pour la stabilité, la fiabilité, la sécurité et la maintenabilité de l'application.  Cette documentation est destinée aux développeurs, aux architectes et aux équipes de test.

## Règles de Gestion

Les règles de gestion définissent la manière dont les opérations sont effectuées et dont les données sont traitées au sein du système. Elles sont implémentées principalement dans le code PHP de l'application, mais peuvent également être influencées par la configuration et les contraintes imposées par l'architecture. Chaque règle de gestion est conçue pour garantir l'intégrité des données et le respect des processus métiers.  Le non-respect de ces règles peut entraîner des anomalies de données, des dysfonctionnements de l'application, ou des violations des exigences métier.

### 1. Gestion des Astreintes

*   **Règle 1 : Validation des Informations d'Astreinte**

    *   **Description** : Avant l'enregistrement d'une astreinte, le système doit valider plusieurs informations pour s'assurer de leur conformité et de leur cohérence.  Cette validation permet de prévenir les erreurs de saisie, d'assurer la qualité des données et de respecter les contraintes métier.
    *   **Détails** :
        *   **Agent concerné** : L'agent affecté à l'astreinte doit exister dans le système et être marqué comme *actif*.  La référence à l'entité `Collaborateur.php` permet de vérifier cette condition.  Les agents inactifs ne peuvent pas être assignés à des astreintes.
        *   **Date de l'astreinte** : La date de l'astreinte doit être valide et ne pas être antérieure à la date du jour.  Les classes `Astreinte.php` et `TypeAstreinteController.php` sont impliquées dans cette vérification.  Ceci garantit que les astreintes ne sont pas planifiées dans le passé.
        *   **Type d'astreinte** : Le type d'astreinte spécifié doit être valide et défini dans le système.  Ceci est vérifié en relation avec l'entité `TypeAstreinte.php`. Seuls les types d'astreinte prédéfinis sont autorisés.
        *   **Horaires** : Les heures de début et de fin de l'astreinte doivent être cohérentes, avec l'heure de fin postérieure à l'heure de début. Cette règle garantit la logique temporelle et évite les erreurs dans le calcul des durées.
        *   **Localisation (Optionnel)** : Si la localisation de l'astreinte est obligatoire, elle doit être renseignée. Si elle est optionnelle, elle est validée si elle est renseignée (ex: adresse valide).
    *   **Implémentation** :
        *   La validation des données est effectuée au sein des contrôleurs, notamment `AstreinteController.php` et potentiellement `TypeAstreinteController.php`.
        *   Des formulaires Symfony sont utilisés pour la saisie des données et intègrent des mécanismes de validation des champs (ex: `AstreinteType.php`).
        *   La validation côté serveur est essentielle pour garantir l'intégrité des données et empêcher les contournements potentiels (par exemple, via des requêtes HTTP directes ou des manipulations client-side).  Elle est complémentaire à la validation côté client.
        *   Le code de validation est généralement encapsulé dans des méthodes dédiées au sein des entités ou des services pour une meilleure réutilisabilité et lisibilité.
*   **Règle 2 : Approbation des Astreintes**

    *   **Description** : Le système exige que les astreintes soient approuvées par un responsable hiérarchique avant d'être considérées comme valides et prises en compte. Ce processus garantit le respect des procédures internes, le contrôle des dépenses, et l'autorisation préalable des heures d'astreinte.
    *   **Détails** :
        *   Un workflow d'approbation est mis en place.  Ce workflow définit les étapes et les acteurs impliqués dans le processus d'approbation.  Les statuts possibles d'une astreinte dans le workflow sont : *Soumis*, *En attente d'approbation*, *Approuvé*, et *Rejeté*.
        *   Le statut de l'astreinte est mis à jour tout au long du processus. Ces statuts sont gérés au sein de l'entité `Astreinte.php` et dans le `AstreinteRepository.php`. Les transitions de statut sont contrôlées pour garantir la cohérence (par exemple, une astreinte ne peut pas être directement "Approuvée" sans être passée par l'état "En attente d'approbation").
        *   Des notifications sont envoyées automatiquement aux acteurs concernés (agent, responsable, etc.) à chaque changement de statut de l'astreinte. Ces notifications informent les utilisateurs de l'état actuel de l'astreinte, des actions à effectuer, et des délais éventuels.
        *   Le responsable a la possibilité de rejeter une astreinte, avec la possibilité de fournir un commentaire expliquant la raison du rejet.
    *   **Implémentation** :
        *   Un système de workflow est implémenté en PHP pour gérer les transitions de statut des astreintes.  Le code associé se trouve dans `Workflow.php` (ou une implémentation similaire).
        *   Le service `NotificationService` est utilisé pour l'envoi des notifications aux utilisateurs (email, notifications in-app).
        *   Les contrôleurs, notamment `AstreinteController.php`, gèrent les changements de statut de l'astreinte et les interactions avec le workflow. Ils orchestrent les transitions de statut et déclenchent l'envoi de notifications.
        *   L'implémentation s'appuie sur des événements et des listeners pour gérer les transitions de statut de manière découplée et extensible.

### 2. Gestion des Primes

*   **Règle 3 : Calcul des Primes**

    *   **Description** : Le système calcule automatiquement les primes en se basant sur des règles et des paramètres spécifiques définis par l'entreprise. Ce calcul automatique garantit l'exactitude et l'efficacité du processus de paie.
    *   **Détails** :
        *   Le calcul des primes est conditionné par le type de prime (`TypePrime.php`), les paramètres associés (coefficients, montants fixes, etc.), ainsi que les données pertinentes (heures supplémentaires, etc.).  Chaque type de prime est associé à une formule de calcul spécifique.
        *   Les formules de calcul peuvent varier en fonction du type de prime et des règles définies. Elles peuvent inclure des calculs arithmétiques simples, des conditions basées sur des seuils, ou des calculs plus complexes.
        *   Les paramètres de calcul (coefficients, montants fixes) sont configurables par les administrateurs via une interface dédiée.
    *   **Implémentation** :
        *   La logique de calcul des primes est encapsulée dans des services dédiés, comme `PrimeService`.  Ces services sont responsables de l'application des formules de calcul et de la gestion des paramètres.
        *   Les types de primes et leurs paramètres sont enregistrés dans les entités appropriées (`Prime.php`, `TypePrime.php`). La définition des types de primes est administrable.
        *   Les formules de calcul sont appliquées en PHP, potentiellement en utilisant des structures conditionnelles et des boucles pour gérer les différents cas de figure. Il est recommandé d'utiliser des méthodes dédiées pour chaque type de prime pour faciliter la maintenance et les tests.
        *   L'utilisation d'un moteur d'expression (ex: Symfony Expression Language) peut être envisagée pour permettre une configuration plus flexible des formules de calcul.
*   **Règle 4 : Validation des Données de Prime**

    *   **Description** : Avant de créer ou de modifier une prime, le système procède à la validation des données saisies afin d'assurer leur cohérence et leur conformité avec les règles en vigueur.  Cette validation est essentielle pour éviter les erreurs de paie et garantir l'intégrité des données financières.
    *   **Détails** :
        *   **Collaborateur** : Le collaborateur concerné par la prime doit exister dans le système et être *actif*.
        *   **Type de prime** : Le type de prime sélectionné doit être valide et correspondre à une définition existante.
        *   **Montants et dates** : Les montants et les dates associés à la prime doivent être cohérents, valides et respecter les règles en vigueur (par exemple, les montants doivent être positifs, les dates doivent être comprises dans une période valide).
        *   **Période** : La période de la prime (mois, année) doit être cohérente avec la date de la prime.
    *   **Implémentation** :
        *   Des formulaires Symfony, utilisant des contraintes de validation spécifiques, sont employés pour la saisie des données (ex: `PrimeAdminType.php`, `TypePrimeType.php`).
        *   Une validation côté serveur est également effectuée dans les contrôleurs (ex: `PrimeController.php`) pour garantir l'intégrité des données, même en cas de contournement des validations client.
        *   Des tests unitaires et fonctionnels sont mis en place pour assurer la validité des règles de validation et le bon fonctionnement du calcul des primes.

### 3. Gestion des Projets

*   **Règle 5 : Validation des Informations de Projet**

    *   **Description** : Le système valide les informations relatives aux projets afin d'assurer leur conformité et leur cohérence. Cette validation assure l'intégrité des données de projet et facilite le suivi et la gestion des projets.
    *   **Détails** :
        *   **Nom du projet** : Le nom du projet doit être unique.  Cette contrainte garantit qu'il n'y ait pas de conflits et permet d'identifier de manière unique chaque projet.
        *   **Dates** : Les dates de début et de fin du projet doivent être valides et cohérentes (la date de fin doit être postérieure à la date de début).  Cette règle assure la logique temporelle du projet.
        *   **Responsables** : Les responsables de projet doivent être des utilisateurs existants et *actifs*. Seuls les utilisateurs autorisés peuvent être désignés comme responsables de projet.
        *   **Budget (Optionnel)** : Si un budget est défini, il doit être un nombre positif.
        *   **Statut (Optionnel)**: Le statut du projet doit être un des statuts prédéfinis et valides (ex: En cours, Terminé, Suspendu).
    *   **Implémentation** :
        *   Les données sont validées via des formulaires Symfony (`ProjectType.php`).
        *   Des contraintes d'unicité sont appliquées au nom du projet, au niveau de l'entité et du repository.
        *   La validation est également effectuée dans les contrôleurs (ex: `ProjectController.php`).
        *   L'utilisation de validateurs personnalisés peut être envisagée pour des validations plus complexes (ex: validation du budget en fonction du type de projet).
*   **Règle 6 : Approbation des Projets**

    *   **Description** : Certains projets, en fonction de leur nature ou de leur importance, requièrent une approbation formelle avant de pouvoir être lancés ou considérés comme valides. Ce processus d'approbation permet de garantir que les projets respectent les procédures et les exigences de l'entreprise.
    *   **Détails** :
        *   Un workflow d'approbation est mis en place pour gérer le processus d'approbation des projets. Le workflow définit les étapes et les acteurs impliqués.
        *   Le statut du projet évolue au cours du workflow (soumis, en attente d'approbation, approuvé, rejeté). Ces statuts sont gérés dans les entités `Project.php` et `ProjectRepository.php`.
        *   Des notifications sont envoyées aux acteurs concernés (chef de projet, responsable, etc.) à chaque étape du workflow, pour les informer des actions à mener.
        *   Le responsable a la possibilité de rejeter un projet, avec la possibilité de fournir un commentaire expliquant la raison du rejet.
    *   **Implémentation** :
        *   Un système de workflow est implémenté en PHP (`Workflow.php`) pour gérer les états et les transitions des projets.
        *   Le service `NotificationService` est utilisé pour l'envoi des notifications.
        *   Les contrôleurs, notamment `ProjectController.php`, gèrent les changements de statut du projet et l'interaction avec le workflow.
        *   L'intégration avec le système de gestion des utilisateurs et des rôles est essentielle pour déterminer les approbateurs et les autorisations associées.

### 4. Autres Règles

*   **Règle 7 : Accès aux Données**

    *   **Description** : Le système met en œuvre des règles de sécurité strictes pour contrôler l'accès aux données, en se basant sur les rôles et les permissions des utilisateurs. Ceci garantit la confidentialité, l'intégrité et la disponibilité des informations.
    *   **Détails** :
        *   Le système intègre un système de gestion des rôles et des permissions.  Les rôles définissent les fonctions et les responsabilités des utilisateurs (ex: administrateur, gestionnaire de projet, etc.). Les permissions définissent les actions autorisées (ex: lecture, écriture, suppression) sur les ressources (ex: projets, astreintes, etc.).
        *   Les informations sensibles (mots de passe, données personnelles, etc.) sont protégées par des mécanismes de sécurité robustes (chiffrement, etc.).
        *   L'accès aux données est limité selon le principe du moindre privilège (un utilisateur ne dispose que des permissions nécessaires pour accomplir ses tâches).
    *   **Implémentation** :
        *   La gestion des rôles et des permissions est assurée par le composant Symfony Security, configuré dans `config/packages/security.yaml`.
        *   Les rôles et les permissions sont définis et stockés dans la base de données.
        *   Des services sont utilisés pour vérifier les permissions des utilisateurs et autoriser ou refuser l'accès aux ressources. L'utilisation d'ACL (Access Control Lists) est recommandée pour une gestion fine des permissions.
        *   Des mécanismes d'authentification multi-facteurs peuvent être envisagés pour renforcer la sécurité de l'accès.
*   **Règle 8 : Sauvegarde et Restauration**

    *   **Description** : Le système met en place des processus réguliers de sauvegarde des données pour garantir leur protection et permettre leur restauration en cas d'incident (perte de données, corruption, erreur humaine). Cette règle assure la continuité de l'activité et la préservation des informations.
    *   **Détails** :
        *   Des sauvegardes régulières des données sont effectuées, selon une planification définie (quotidienne, hebdomadaire, etc.).
        *   Des journaux de sauvegarde sont maintenus pour suivre l'historique des sauvegardes, faciliter la restauration et permettre le suivi des anomalies.
        *   Une procédure de restauration des données est disponible et testée régulièrement.  La procédure de restauration doit être documentée et accessible.
        *   Les sauvegardes sont stockées de manière sécurisée (par exemple, dans un emplacement distinct, avec des contrôles d'accès).
    *   **Implémentation** :
        *   Des scripts shell (ex: `bin/backup.sh`) sont utilisés pour automatiser les sauvegardes.
        *   La configuration de la base de données est optimisée pour faciliter les opérations de sauvegarde et de restauration (ex: utilisation de bases de données répliquées).
        *   Des outils de gestion de version (ex: Git) sont utilisés pour gérer les fichiers de code source et permettre la restauration en cas de besoin.

## Contraintes Système

Les contraintes système décrivent les limitations imposées par l'environnement technique et les exigences d'exploitation. Elles sont essentielles pour assurer la compatibilité, la performance, la sécurité et la maintenabilité de l'application.

### 1. Environnement Technique

*   **Technologies** : PHP (version et extensions spécifiques), Symfony 6/7, Doctrine (ORM), Base de données relationnelle (ex: MySQL, PostgreSQL), Javascript (jQuery, Bootstrap).  La version exacte de chaque technologie doit être précisée.
*   **Contrainte** : L'application WacitV2 doit être compatible et fonctionner correctement dans l'environnement technique spécifié.  Toute modification de l'environnement technique doit être documentée et testée.
*   **Conséquences** :
    *   Le code source doit respecter les standards de codage de PHP et de Symfony, ainsi que les recommandations de sécurité (PSR standards).
    *   Les bibliothèques tierces doivent être compatibles avec les versions des frameworks et des langages utilisés.  Une gestion des dépendances via Composer est obligatoire.
    *   Les performances de l'application dépendent de l'optimisation de la base de données, du code PHP, et de la mise en cache des données.  Une attention particulière doit être portée à ces aspects. Des tests de performance réguliers doivent être effectués.
    *   L'utilisation de conteneurs (ex: Docker) est recommandée pour faciliter le déploiement et garantir la cohérence de l'environnement.
    *   L'application doit être déployée sur un serveur respectant les prérequis techniques.

### 2. Sécurité

*   **Authentification et Autorisation** : Le système doit garantir la sécurité de l'accès à l'application.
    *   **Contrainte** : Les accès doivent être strictement contrôlés en fonction des rôles et des permissions des utilisateurs. L'authentification et l'autorisation sont des aspects critiques de la sécurité.
    *   **Implémentation** :
        *   Mise en place d'une authentification robuste (ex: JWT, OAuth, ou une solution similaire) pour vérifier l'identité des utilisateurs. L'utilisation de protocoles sécurisés (HTTPS) est obligatoire.
        *   Gestion précise des rôles et des permissions pour contrôler l'accès aux différentes fonctionnalités et données. L'implémentation doit être maintenue à jour face aux nouvelles vulnérabilités.
        *   Utilisation du composant Symfony Security (`config/packages/security.yaml`) pour gérer l'authentification et l'autorisation.
*   **Protection contre les Attaques** : L'application doit être protégée contre les attaques de sécurité courantes.  La sécurité est une préoccupation constante.
    *   **Contrainte** : Les vulnérabilités potentielles doivent être minimisées et corrigées rapidement.  La sécurité doit être intégrée tout au long du cycle de développement.
    *   **Implémentation** :
        *   Validation et échappement systématiques des données saisies par l'utilisateur pour prévenir les attaques de type XSS (Cross-Site Scripting) et Injection SQL.  L'utilisation de prepared statements est obligatoire pour les requêtes SQL.
        *   Utilisation des protections intégrées de Symfony (CSRF tokens, etc.) pour prévenir les attaques CSRF (Cross-Site Request Forgery).
        *   Mise à jour régulière des bibliothèques et des frameworks pour corriger les failles de sécurité connues.  Un suivi des vulnérabilités et des mises à jour de sécurité est indispensable.
        *   Tests de sécurité réguliers (ex: scan de vulnérabilités, tests d'intrusion) doivent être réalisés.
        *   Mise en place d'un système de logging pour enregistrer les événements de sécurité (tentatives de connexion, accès non autorisés, etc.).

### 3. Performance et Scalabilité

*   **Performance** : Le système doit être performant et répondre rapidement aux requêtes des utilisateurs. La performance est cruciale pour l'expérience utilisateur.
    *   **Contrainte** : Optimisation continue des performances, incluant l'optimisation des requêtes SQL, la mise en cache des données, et l'optimisation du code source. Des objectifs de performance (temps de réponse, nombre de requêtes par seconde) doivent être définis et mesurés.
    *   **Implémentation** :
        *   Utilisation d'index sur les colonnes des tables de la base de données qui sont fréquemment utilisées dans les requêtes. L'analyse des requêtes lentes est essentielle.
        *   Implémentation du système de cache de Symfony (ex: mise en cache des résultats des requêtes, des fragments de pages, etc.).
        *   Optimisation du code PHP pour éviter les boucles et les opérations inutiles, et pour améliorer l'efficacité du code.
        *   Minification et compression des ressources statiques (CSS, JavaScript).
        *   Utilisation d'outils de profilage pour identifier les goulots d'étranglement.
*   **Scalabilité** : Le système doit être capable de gérer une charge de travail importante et de s'adapter à une croissance du nombre d'utilisateurs et de données. La scalabilité est essentielle pour anticiper la croissance de l'application.
    *   **Contrainte** : L'application doit pouvoir gérer un nombre croissant d'utilisateurs et de données, sans perte de performance.
    *   **Implémentation** :
        *   Utilisation de serveurs web performants (ex: Nginx) et de conteneurs (ex: Docker) pour faciliter le déploiement, la gestion et la mise à l'échelle de l'application.
        *   Mise en place d'une architecture de load balancing (équilibrage de charge) pour répartir la charge de travail sur plusieurs serveurs, si nécessaire.
        *   Utilisation d'une base de données adaptée à la scalabilité (ex: base de données distribuée).
        *   Mise en place d'une gestion asynchrone des tâches (ex: utilisation de queues de messages comme RabbitMQ ou Redis) pour améliorer les performances.

### 4. Disponibilité

*   **Disponibilité** : L'application doit être disponible pour les utilisateurs. La disponibilité est un indicateur clé de la qualité du service.
    *   **Contrainte** : Minimisation des temps d'arrêt (maintenance planifiée, incidents). Des objectifs de disponibilité (SLA - Service Level Agreement) doivent être définis.
    *   **Implémentation** :
        *   Mise en place d'un système de surveillance de l'application (ex: monitoring, alerting) pour détecter rapidement les problèmes et les incidents.
        *   Mise en place de sauvegardes régulières des données et d'une procédure de restauration pour limiter l'impact des incidents.
        *   Mise en place d'une infrastructure redondante (serveurs, bases de données) pour assurer la haute disponibilité.
        *   Gestion des erreurs et des exceptions avec des mécanismes de journalisation appropriés.

## Exemple de Code (Règle de Validation d'une Astreinte - Pseudo Code)

```php
<?php
// src/Controller/AstreinteController.php
namespace App\Controller;

use App\Entity\Astreinte;
use App\Form\AstreinteType;
use Doctrine\ORM\EntityManagerInterface;
use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\HttpFoundation\Request;
use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\Routing\Annotation\Route;
use Symfony\Component\Validator\Validator\ValidatorInterface; // Importez le ValidatorInterface

class AstreinteController extends AbstractController
{
    /**
     * @Route("/astreinte/new", name="astreinte_new")
     */
    public function new(Request $request, EntityManagerInterface $entityManager, ValidatorInterface $validator): Response
    {
        $astreinte = new Astreinte();
        $form = $this->createForm(AstreinteType::class, $astreinte);

        $form->handleRequest($request);

        if ($form->isSubmitted() && $form->isValid()) {
            // Règle de Gestion : Validation (déplacé dans une fonction de validation)
            $errors = $this->validateAstreinte($astreinte, $validator);

            if (count($errors) > 0) {
                // Afficher les erreurs de validation
                foreach ($errors as $error) {
                    $this->addFlash('error', $error->getMessage());
                }
                return $this->redirectToRoute('astreinte_new');
            }

            $entityManager->persist($astreinte);
            $entityManager->flush();

            $this->addFlash('success', 'Astreinte enregistrée avec succès.');

            return $this->redirectToRoute('astreinte_show', ['id' => $astreinte->getId()]);
        }

        return $this->render('astreinte/new.html.twig', [
            'form' => $form->createView(),
        ]);
    }

    /**
     * Fonction pour valider une astreinte.  Utilisation du ValidatorInterface pour une validation plus standard.
     */
    private function validateAstreinte(Astreinte $astreinte, ValidatorInterface $validator): \Symfony\Component\Validator\ConstraintViolationListInterface
    {
        // Validation de l'agent (peut être déplacé dans une contrainte personnalisée)
        if (!$astreinte->getAgent() || !$astreinte->getAgent()->isActive()) {
            $this->addFlash('error', 'L\'agent sélectionné n\'est pas valide ou n\'est pas actif.');
        }

        // Utilisation du validateur Symfony pour les contraintes déclarées dans l'entité
        $errors = $validator->validate($astreinte);

        // Validation manuelle (exemples)
        if ($astreinte->getDate() < new \DateTime()) {
           $errors->addViolation('La date de l\'astreinte ne peut pas être antérieure à la date du jour.');
        }

        if ($astreinte->getHeureFin() <= $astreinte->getHeureDebut()) {
            $errors->addViolation('L\'heure de fin doit être postérieure à l\'heure de début.');
        }

        return $errors;
    }
}
```

*   **Améliorations dans l'exemple de code:**
    *   **Utilisation du ValidatorInterface:** Intégration du `ValidatorInterface` de Symfony pour effectuer la validation, ce qui est la manière recommandée.
    *   **Retour des erreurs:** La fonction `validateAstreinte` retourne maintenant un objet `ConstraintViolationListInterface` contenant les erreurs, ce qui est plus robuste.
    *   **Gestion des erreurs:** Le contrôleur affiche les erreurs de validation retournées par la fonction.
    *   **Contraintes personnalisées:** Il est recommandé d'utiliser des contraintes personnalisées pour les validations complexes, qui peuvent être définies directement dans les entités.
    *   **Clarté:** Ajout de commentaires pour expliquer chaque étape du code.
    *   **Robustesse:** Le code gère les cas où des validations échouent.
    *   **Séparation des responsabilités:** La validation est séparée du contrôleur pour une meilleure lisibilité et maintenabilité.

## Conclusion

Les règles de gestion et les contraintes système décrites dans cette section sont fondamentales pour le bon fonctionnement, la sécurité, la performance et la pérennité de WacitV2.  Le respect rigoureux de ces règles et contraintes est une responsabilité partagée par tous les développeurs, les architectes, les équipes de test et les administrateurs, afin d'assurer la qualité et la fiabilité de l'application. Une compréhension approfondie de ces éléments est essentielle pour toute personne impliquée dans le développement, la maintenance ou l'utilisation de WacitV2.  Toute modification ou ajout de règles de gestion et de contraintes système doit être documenté dans cette section et impactant les autres sections de la documentation.
```
APPROVED: [content]
```

---

# API

---

```wiki
== Documentation de l'API WacitV2 ==

=== Introduction ===
Cette documentation détaille l'API (Application Programming Interface) de WacitV2. Elle est destinée aux développeurs souhaitant intégrer WacitV2 à d'autres systèmes ou créer des applications clientes. La documentation décrit en détail les endpoints disponibles, les méthodes HTTP supportées, les paramètres attendus, les réponses possibles et les consignes d'authentification.

=== Architecture de l'API ===
L'API WacitV2 est conçue selon les principes RESTful et est implémentée avec le framework Symfony. Elle expose des endpoints via des contrôleurs, avec des routes définies par des annotations. L'API utilise généralement le format JSON pour l'échange de données.

*   **Méthodes HTTP Supportées**: `GET`, `POST`, `PUT`, `PATCH`, `DELETE`.
*   **Format de données**: JSON
*   **Authentification**: L'API utilise JWT (JSON Web Tokens) pour l'authentification et l'autorisation. Des sessions Symfony peuvent également être utilisées dans certains contextes, bien que JWT soit la méthode privilégiée.

=== Conventions ===
*   **URL de base**: `<votre_domaine>/api` (à adapter selon votre environnement). Toutes les URLs des endpoints sont relatives à cette URL de base. Par exemple, l'endpoint pour récupérer les astreintes sera `<votre_domaine>/api/astreintes`.
*   **En-têtes HTTP**:
    *   `Content-Type`: `application/json` (pour les requêtes envoyant des données au format JSON).
    *   `Accept`: `application/json` (pour indiquer que le client accepte une réponse au format JSON).
    *   `Authorization`: `Bearer <votre_token>` (pour l'authentification, où `<votre_token>` est le JWT fourni après l'authentification réussie via `/api/login`).

=== Gestion de l'Authentification et des Autorisations ===
L'API WacitV2 utilise les JWT (JSON Web Tokens) pour l'authentification. Chaque requête nécessitant une authentification doit inclure le token JWT dans l'en-tête `Authorization`. La gestion des rôles et des permissions est assurée côté serveur, déterminant ainsi l'accès aux différentes ressources.

*   **Obtention du Token**: L'authentification se fait via l'endpoint `/login` (POST). En cas de succès, un token JWT est renvoyé.
*   **Utilisation du Token**: Le token doit être inclus dans l'en-tête `Authorization` de chaque requête subséquente : `Authorization: Bearer <votre_token>`.
*   **Expiration du Token**: Les tokens ont une durée de vie limitée. Il est recommandé d'utiliser des tokens de courte durée et des mécanismes de rafraîchissement (refresh tokens) pour améliorer la sécurité et l'expérience utilisateur.
*   **Refresh Token (si implémenté)**: Si le refresh token est implémenté, il peut être utilisé pour obtenir un nouveau token sans avoir à se réauthentifier, généralement via l'endpoint `/refresh` (POST).

=== Endpoints de l'API ===
Cette section décrit les différents endpoints disponibles, leurs méthodes, paramètres et exemples de réponses. **Note :** La liste des endpoints est basée sur l'analyse du projet et sur des hypothèses. Sans accès direct au code source, cette liste est susceptible d'être incomplète. Il est fortement recommandé de consulter la documentation officielle (si disponible) ou d'inspecter le code source pour obtenir des informations complètes et à jour.

==== 1. Gestion des Astreintes ====
*   **Description**: Permet de gérer les informations relatives aux astreintes des collaborateurs.

*   **Endpoint:** `/astreintes`
    *   **Méthodes:**
        *   `GET`: Récupère la liste des astreintes. Nécessite une authentification.
        *   `POST`: Crée une nouvelle astreinte. Nécessite une authentification et des permissions spécifiques.
    *   **Endpoint:** `/astreintes/{id}`
        *   **Méthodes:**
            *   `GET`: Récupère les détails d'une astreinte spécifique (par ID). Nécessite une authentification.
            *   `PUT`: Met à jour une astreinte existante. Nécessite une authentification et des permissions spécifiques.
            *   `DELETE`: Supprime une astreinte. Nécessite une authentification et des permissions spécifiques.
*   **Paramètres (Exemples)** :

    *   **Pour `POST /astreintes`**:
        *   `date`: `string` (Format: `YYYY-MM-DD`), obligatoire. Représente la date de l'astreinte.
        *   `agent_id`: `integer`, obligatoire. L'identifiant de l'agent concerné par l'astreinte.
        *   `type_astreinte_id`: `integer`, obligatoire. L'identifiant du type d'astreinte (ex: nuit, week-end).
        *   `description`: `string`, optionnel. Une description textuelle de l'astreinte.

    *   **Pour `PUT /astreintes/{id}`**: (Mêmes paramètres que `POST`, plus la possibilité de modifier l'ID. L'ID dans l'URL doit correspondre à celui de l'astreinte à modifier. Tous les champs peuvent être mis à jour).

*   **Réponses (Exemples)**:

    *   `GET /astreintes`:
        *   `200 OK`:
            ```json
            [
                {
                    "id": 1,
                    "date": "2024-10-27",
                    "agent_id": 123,
                    "type_astreinte_id": 1,
                    "description": "Astreinte de nuit",
                    "status": "active"
                },
                {
                    "id": 2,
                    "date": "2024-10-28",
                    "agent_id": 456,
                    "type_astreinte_id": 2,
                    "description": "Astreinte de week-end",
                    "status": "active"
                }
            ]
            ```
        *   `401 Unauthorized`: Si l'authentification échoue (token JWT invalide ou manquant).
        *   `403 Forbidden`: Si l'utilisateur n'a pas les permissions nécessaires.
        *   `500 Internal Server Error`: En cas d'erreur serveur. Le corps de la réponse peut contenir des informations de débogage (non destiné à l'utilisateur final).

    *   `POST /astreintes`:
        *   `201 Created`: La ressource a été créée avec succès. L'en-tête `Location` de la réponse doit pointer vers l'URL de la nouvelle ressource (ex: `/api/astreintes/23`).
            ```json
            {
                "id": 2,
                "date": "2024-10-28",
                "agent_id": 456,
                "type_astreinte_id": 2,
                "description": "Astreinte de week-end",
                "status": "active"
            }
            ```
        *   `400 Bad Request`: Si les données soumises sont invalides (ex: champs manquants, format incorrect). Le corps de la réponse contiendra probablement des détails sur les erreurs de validation.
        *   `401 Unauthorized`: Si l'authentification échoue.
        *   `403 Forbidden`: Si l'utilisateur n'a pas les permissions nécessaires.
        *   `500 Internal Server Error`: En cas d'erreur serveur.

    *   `GET /astreintes/{id}`:
        *   `200 OK`:
            ```json
            {
                "id": 1,
                "date": "2024-10-27",
                "agent_id": 123,
                "type_astreinte_id": 1,
                "description": "Astreinte de nuit",
                "status": "active"
            }
            ```
        *   `404 Not Found`: Si l'astreinte avec l'ID spécifié n'est pas trouvée.
        *   `401 Unauthorized`: Si l'authentification échoue.
        *   `403 Forbidden`: Si l'utilisateur n'a pas les permissions nécessaires.
        *   `500 Internal Server Error`: En cas d'erreur serveur.

    *   `PUT /astreintes/{id}`:
        *   `200 OK`: Retourne les données mises à jour.
            ```json
            {
                "id": 1,
                "date": "2024-10-28",
                "agent_id": 789,
                "type_astreinte_id": 2,
                "description": "Astreinte de week-end - Modifiée",
                "status": "active"
            }
            ```
        *   `400 Bad Request`: Si les données soumises sont invalides.
        *   `401 Unauthorized`: Si l'authentification échoue.
        *   `403 Forbidden`: Si l'utilisateur n'a pas les permissions nécessaires.
        *   `404 Not Found`: Si l'astreinte avec l'ID spécifié n'est pas trouvée.
        *   `500 Internal Server Error`: En cas d'erreur serveur.

    *   `DELETE /astreintes/{id}`:
        *   `204 No Content`: La suppression a réussi.
        *   `401 Unauthorized`: Si l'authentification échoue.
        *   `403 Forbidden`: Si l'utilisateur n'a pas les permissions nécessaires.
        *   `404 Not Found`: Si l'astreinte avec l'ID spécifié n'est pas trouvée.
        *   `500 Internal Server Error`: En cas d'erreur serveur.

==== 2. Gestion des Primes ====
*   **Description**: Permet de gérer les primes des collaborateurs.
*   **Endpoint:** `/primes`
    *   **Méthodes:**
        *   `GET`: Récupère la liste des primes. Nécessite une authentification et des permissions spécifiques.
        *   `POST`: Crée une nouvelle prime. Nécessite une authentification et des permissions spécifiques.
*   **Endpoint:** `/primes/{id}`
    *   **Méthodes:**
        *   `GET`: Récupère les détails d'une prime spécifique (par ID). Nécessite une authentification et des permissions spécifiques.
        *   `PUT`: Met à jour une prime existante. Nécessite une authentification et des permissions spécifiques.
        *   `DELETE`: Supprime une prime. Nécessite une authentification et des permissions spécifiques.
*   **Paramètres (Exemples)** :
    *   **Pour `POST /primes`**:
        *   `collaborateur_id`: `integer`, obligatoire. L'identifiant du collaborateur concerné par la prime.
        *   `type_prime_id`: `integer`, obligatoire. L'identifiant du type de prime (ex: prime de performance, prime d'ancienneté).
        *   `montant`: `decimal`, obligatoire. Le montant de la prime.
        *   `date_paiement`: `string` (Format: `YYYY-MM-DD`), obligatoire. La date de paiement de la prime.
        *   `description`: `string`, optionnel. Une description textuelle de la prime.
    *   **Pour `PUT /primes/{id}`**: (Mêmes paramètres que `POST`, plus la possibilité de modifier l'ID).

*   **Réponses (Exemples)**: (Similaires aux réponses de `/astreintes`, avec des champs adaptés pour les primes, et les codes d'erreurs appropriés).

==== 3. Gestion des Projets ====
*   **Description**: Permet de gérer les informations relatives aux projets.
*   **Endpoint:** `/projets`
    *   **Méthodes:**
        *   `GET`: Récupère la liste des projets. Nécessite une authentification et des permissions spécifiques.
        *   `POST`: Crée un nouveau projet. Nécessite une authentification et des permissions spécifiques.
*   **Endpoint:** `/projets/{id}`
    *   **Méthodes:**
        *   `GET`: Récupère les détails d'un projet spécifique (par ID). Nécessite une authentification et des permissions spécifiques.
        *   `PUT`: Met à jour un projet existant. Nécessite une authentification et des permissions spécifiques.
        *   `DELETE`: Supprime un projet. Nécessite une authentification et des permissions spécifiques.
*   **Paramètres (Exemples)** :
    *   **Pour `POST /projets`**:
        *   `nom`: `string`, obligatoire. Le nom du projet.
        *   `description`: `string`, optionnel. Une description du projet.
        *   `date_debut`: `string` (Format: `YYYY-MM-DD`), optionnel. La date de début du projet.
        *   `date_fin`: `string` (Format: `YYYY-MM-DD`), optionnel. La date de fin du projet.
    *   **Pour `PUT /projets/{id}`**: (Mêmes paramètres que `POST`, plus la possibilité de modifier l'ID).

*   **Réponses (Exemples)**: (Similaires aux réponses de `/astreintes`, avec des champs adaptés pour les projets, et les codes d'erreurs appropriés).

==== 4. Gestion des Collaborateurs ====
*   **Description**: Permet de gérer les informations sur les collaborateurs.
*   **Endpoint:** `/collaborateurs`
    *   **Méthodes:**
        *   `GET`: Récupère la liste des collaborateurs. Nécessite une authentification et des permissions spécifiques (par exemple, le rôle 'admin').
        *   `POST`: Crée un nouveau collaborateur. Nécessite une authentification et des permissions spécifiques (par exemple, le rôle 'admin').
*   **Endpoint:** `/collaborateurs/{id}`
    *   **Méthodes:**
        *   `GET`: Récupère les détails d'un collaborateur spécifique (par ID). Nécessite une authentification et des permissions spécifiques (par exemple, le rôle 'admin' ou l'accès à son propre profil).
        *   `PUT`: Met à jour un collaborateur existant. Nécessite une authentification et des permissions spécifiques (par exemple, le rôle 'admin').
        *   `DELETE`: Supprime un collaborateur. Nécessite une authentification et des permissions spécifiques (par exemple, le rôle 'admin').
*   **Paramètres (Exemples)** :
    *   **Pour `POST /collaborateurs`**:
        *   `nom`: `string`, obligatoire. Le nom de famille du collaborateur.
        *   `prenom`: `string`, obligatoire. Le prénom du collaborateur.
        *   `email`: `string` (format d'email valide), obligatoire. L'adresse e-mail du collaborateur.
        *   `date_embauche`: `string` (Format: `YYYY-MM-DD`), optionnel. La date d'embauche du collaborateur.
    *   **Pour `PUT /collaborateurs/{id}`**: (Mêmes paramètres que `POST`, plus la possibilité de modifier l'ID).

*   **Réponses (Exemples)**: (Similaires aux réponses de `/astreintes`, avec des champs adaptés pour les collaborateurs, et les codes d'erreurs appropriés).

==== 5. Gestion des Utilisateurs ====
*   **Description**: Permet de gérer les informations relatives aux utilisateurs (droits, accès).
*   **Endpoint:** `/utilisateurs`
    *   **Méthodes:**
        *   `GET`: Récupère la liste des utilisateurs (nécessite des droits d'administrateur).
        *   `POST`: Crée un nouvel utilisateur (nécessite des droits d'administrateur).
*   **Endpoint:** `/utilisateurs/{id}`
    *   **Méthodes:**
        *   `GET`: Récupère les détails d'un utilisateur spécifique (par ID, nécessite des droits d'administrateur ou l'accès à son propre profil).
        *   `PUT`: Met à jour un utilisateur existant (nécessite des droits d'administrateur ou l'accès à son propre profil).
        *   `DELETE`: Supprime un utilisateur (nécessite des droits d'administrateur).
*   **Endpoint:** `/utilisateurs/motdepasse`
    *   **Méthodes:**
        *   `POST`: Change le mot de passe de l'utilisateur connecté.
*   **Paramètres (Exemples)** :
    *   **Pour `POST /utilisateurs`**:
        *   `email`: `string` (format d'email valide), obligatoire. L'adresse e-mail de l'utilisateur.
        *   `mot_de_passe`: `string`, obligatoire. Le mot de passe de l'utilisateur.
        *   `roles`: `array` (ex: `['ROLE_ADMIN', 'ROLE_USER']`), obligatoire. Un tableau de rôles attribués à l'utilisateur. Les rôles déterminent les permissions de l'utilisateur.
    *   **Pour `POST /utilisateurs/motdepasse`**:
        *   `ancien_mot_de_passe`: `string`, obligatoire. L'ancien mot de passe de l'utilisateur.
        *   `nouveau_mot_de_passe`: `string`, obligatoire. Le nouveau mot de passe.

*   **Réponses (Exemples)**: (Similaires aux réponses de `/astreintes`, avec des champs adaptés pour les utilisateurs, et les codes d'erreurs appropriés).

==== 6. Authentification (Exemple) ====
*   **Description**: Fournit des endpoints pour l'authentification et l'obtention de tokens.
*   **Endpoint:** `/login`
    *   **Méthodes:**
        *   `POST`: Authentifie l'utilisateur et renvoie un token JWT.
*   **Paramètres:**
    *   `email`: `string`, obligatoire. L'adresse e-mail de l'utilisateur.
    *   `password`: `string`, obligatoire. Le mot de passe de l'utilisateur.
*   **Réponses:**
    *   `200 OK`: L'authentification a réussi.
        ```json
        {
            "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VybmFtZSI6ImFkbWluQGV4YW1wbGUuY29tIiwicm9sZXMiOlsiUk9MRV9BRE1JTiJdLCJpYXQiOjE2OTU3MzYwMDAsImV4cCI6MTY5NTc0MzIwMH0.S6-M3QkG25rK7G_Qk7d6Q6lFf_vYx-A4z0n4K3aE-lI"
        }
        ```
    *   `401 Unauthorized`: L'authentification a échoué (identifiants incorrects).
    *   `500 Internal Server Error`: En cas d'erreur serveur.
*   **Endpoint:** `/logout`
    *   **Méthodes:**
        *   `POST`: Invalide le token (si l'authentification par session est utilisée). Cette méthode est optionnelle, selon l'implémentation du mécanisme d'authentification.  Dans le cas de JWT pur, la déconnexion côté serveur est souvent inutile (le token est auto-suffisant).
*   **Endpoint:** `/refresh` (Si implémenté)
    *   **Méthodes:**
        *   `POST`: Rafraîchit le token JWT (si les tokens rafraîchis sont utilisés).
        ```json
        {
            "token": "..."
        }
        ```
        *   `401 Unauthorized`: Si l'authentification échoue (token expiré ou invalide).
        *   `500 Internal Server Error`: En cas d'erreur serveur.

*   **Header d'autorisation**: Pour les requêtes authentifiées, inclure le token JWT dans l'en-tête `Authorization`:
    *   `Authorization: Bearer <token>`

==== 7. Autres Endpoints (Hypothétiques) ====
*   `/devise/echanges` : Gestion des échanges de devises. (Requiert probablement une authentification).
*   `/approbations` : Gestion des approbations et validations. (Requiert probablement une authentification et des rôles spécifiques).
*   `/calendrier` : Gestion des calendriers. (Requiert probablement une authentification).
*   `/parametres` : Accès aux paramètres de l'application (peut nécessiter des droits d'administrateur). (Requiert probablement une authentification et des rôles spécifiques).

=== Guide d'Intégration ===
==== 1. Prérequis ====
*   Un environnement de développement capable d'effectuer des requêtes HTTP (ex: `curl`, Postman, Insomnia, ou un code client).
*   Des identifiants d'authentification valides (si l'authentification est requise - cf. section Authentification). Contactez l'équipe de développement pour obtenir des identifiants de test.
*   Connaissance de base du format JSON et des requêtes HTTP.

==== 2. Authentification ====
*   Si l'API nécessite une authentification (ce qui est très probable), vous devez d'abord vous authentifier en utilisant l'endpoint `/login` (POST).
*   Le serveur renverra un token (JWT) dans la réponse.
*   Pour chaque requête ultérieure vers des endpoints protégés, incluez ce token dans l'en-tête `Authorization` de la requête: `Authorization: Bearer <votre_token>`. **Important :** Conservez le token de manière sécurisée.  Considérez l'utilisation d'un coffre-fort de secrets ou de mécanismes de stockage sécurisés en fonction de votre environnement.
*   Si des tokens de rafraîchissement sont utilisés, implémentez la logique de rafraîchissement du token (via l'endpoint `/refresh`) avant l'expiration du token.

==== 3. Exemples de Requêtes et de Réponses ====
Les exemples ci-dessous utilisent l'outil `curl`. Adaptez les URLs et les valeurs des paramètres en fonction de votre environnement et de vos données. Remplacez `<votre_token>` par le token JWT obtenu après l'authentification. Remplacez `<votre_domaine>` par l'adresse de votre instance de WacitV2 (par exemple, `https://api.example.com`).

*   **Exemple 1 : Récupération de la liste des astreintes (GET /astreintes)**

```bash
curl -X GET "<votre_domaine>/api/astreintes" -H "Authorization: Bearer <votre_token>" -H "Accept: application/json"
```

*   **Exemple 2 : Création d'une astreinte (POST /astreintes)**

```bash
curl -X POST "<votre_domaine>/api/astreintes" \
  -H "Authorization: Bearer <votre_token>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "date": "2024-10-28",
        "agent_id": 456,
        "type_astreinte_id": 2,
        "description": "Astreinte de week-end"
    }'
```

*   **Exemple 3 : Authentification (POST /login)**

```bash
curl -X POST "<votre_domaine>/api/login" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "email": "votre_email@exemple.com",
        "password": "votre_mot_de_passe"
    }'
```

==== 4. Gestion des Erreurs ====
L'API utilise les codes de statut HTTP pour signaler le succès ou l'échec d'une requête. Les codes de statut courants sont :

*   `200 OK`: Succès. La requête a été traitée avec succès.
*   `201 Created`: La ressource a été créée avec succès. L'en-tête `Location` dans la réponse fournit l'URL de la nouvelle ressource.
*   `204 No Content`: La requête a réussi, mais il n'y a pas de contenu à renvoyer (souvent utilisé pour les requêtes `DELETE`).
*   `400 Bad Request`: La requête est invalide (ex: paramètres manquants ou invalides, format incorrect). Le corps de la réponse peut fournir des détails sur les erreurs de validation.
*   `401 Unauthorized`: Authentification requise. Le token JWT est manquant ou invalide. Vérifiez votre token et assurez-vous que vous êtes authentifié.
*   `403 Forbidden`: L'utilisateur n'a pas les permissions nécessaires pour accéder à la ressource.
*   `404 Not Found`: La ressource demandée n'a pas été trouvée. Vérifiez l'URL de la ressource.
*   `500 Internal Server Error`: Erreur interne du serveur. Contactez l'équipe de développement si vous rencontrez fréquemment cette erreur.

En cas d'erreur, l'API renvoie généralement un corps de réponse au format JSON avec des informations d'erreur. Consultez le corps de la réponse pour comprendre la nature de l'erreur. Analysez attentivement les codes de statut HTTP et les messages d'erreur pour diagnostiquer et résoudre les problèmes.

=== Modèles de Données ===
*   Cette section décrit les structures de données utilisées par l'API. Les attributs indiqués sont des exemples. Vérifiez la documentation officielle ou le code source pour les détails précis.
    *   **Astreinte**:
        ```json
        {
            "id": integer,
            "date": string (YYYY-MM-DD),
            "agent_id": integer,
            "type_astreinte_id": integer,
            "description": string,
            "status": string (active, terminée, etc.)
        }
        ```
    *   **Prime**:
        ```json
        {
          "id": integer,
          "collaborateur_id": integer,
          "type_prime_id": integer,
          "montant": decimal,
          "date_paiement": string (YYYY-MM-DD),
          "description": string
        }
        ```
    *   **Projet**:
        ```json
        {
            "id": integer,
            "nom": string,
            "description": string,
            "date_debut": string (YYYY-MM-DD, optionnel),
            "date_fin": string (YYYY-MM-DD, optionnel)
        }
        ```
    *   **Collaborateur**:
        ```json
        {
            "id": integer,
            "nom": string,
            "prenom": string,
            "email": string,
            "date_embauche": string (YYYY-MM-DD)
        }
        ```
    *   **Utilisateur**:
        ```json
        {
            "id": integer,
            "email": string,
            "roles": array (ex: ['ROLE_ADMIN', 'ROLE_USER'])
        }
        ```
*   D'autres modèles de données existent pour les types d'astreintes, les types de primes, etc. Ces modèles ne sont pas détaillés ici, mais seront structurés de manière similaire. Consultez les sections des endpoints correspondants pour plus de détails.

=== Exemples de Code (Clients) ===
Les exemples de code suivants montrent comment effectuer des requêtes à l'API en utilisant différents langages de programmation. Adaptez le code en fonction de votre environnement et de vos besoins. **Important :** Gérez les erreurs correctement dans votre code client (ex: vérifiez le code de statut HTTP de la réponse).

==== 1. Exemple en JavaScript (avec `fetch`) ====
```javascript
async function getAstreintes(token) {
  try {
    const response = await fetch('<votre_domaine>/api/astreintes', { // Utilisez l'URL complète, incluant le domaine
      method: 'GET',
      headers: {
        'Authorization': `Bearer ${token}`,
        'Content-Type': 'application/json',
        'Accept': 'application/json'
      }
    });

    if (!response.ok) {
      // Gestion des erreurs HTTP
      throw new Error(`Erreur HTTP: ${response.status} - ${response.statusText}`);
    }

    const astreintes = await response.json();
    console.log(astreintes);
    return astreintes;

  } catch (error) {
    console.error('Erreur lors de la récupération des astreintes:', error);
    return null;
  }
}

// Exemple d'utilisation:
// getAstreintes(votreTokenJWT);
```
==== 2. Exemple en Python (avec `requests`) ====
```python
import requests
import json

def get_astreintes(token, base_url):
    url = f'{base_url}/api/astreintes' # Utilisez l'URL complète, incluant le domaine
    headers = {
        'Authorization': f'Bearer {token}',
        'Content-Type': 'application/json',
        'Accept': 'application/json'
    }
    try:
        response = requests.get(url, headers=headers)
        response.raise_for_status() # Lève une exception pour les codes d'erreur HTTP

        astreintes = response.json()
        print(json.dumps(astreintes, indent=4)) # Affichage formaté
        return astreintes

    except requests.exceptions.RequestException as e:
        print(f'Erreur lors de la requête: {e}')
        return None

# Exemple d'utilisation:
# token = "votreTokenJWT"
# base_url = "http://votre_domaine" # Exemple: "http://localhost:8000" ou "https://api.example.com"
# get_astreintes(token, base_url)
```

=== Sécurité ===
*   **HTTPS**: Toutes les communications avec l'API doivent être effectuées via HTTPS pour garantir la sécurité des données. L'utilisation de HTTP est fortement déconseillée.
*   **Validation des données**: Validez toujours les données entrantes côté client et, surtout, côté serveur (Symfony utilise le validateur). Ne faites jamais confiance aux données envoyées par le client.
*   **Protection contre les attaques**: Assurez-vous que les applications clientes sont protégées contre les attaques courantes (XSS, CSRF, injection SQL, etc.). Utilisez des bibliothèques et des pratiques de développement sécurisées.
*   **Gestion des accès**: Utilisez des mécanismes d'autorisation appropriés (RBAC - Role-Based Access Control) pour contrôler l'accès aux ressources. Les rôles définissent les permissions des utilisateurs.
*   **Stockage sécurisé des tokens**: Si vous stockez le token côté client (ex: dans le navigateur), utilisez des mécanismes de stockage sécurisés (ex: `httpOnly` cookies, `localStorage` avec des mesures de sécurité supplémentaires). Privilégiez les cookies `httpOnly` pour une meilleure protection contre les attaques XSS.
*   **Expiration des tokens**: Implémentez une expiration pour les tokens (JWT) afin de limiter l'impact d'une compromission. Utilisez des tokens rafraîchis (refresh tokens) pour renouveler les tokens sans que l'utilisateur ait à se réauthentifier.
*   **Protection des endpoints sensibles**: Les endpoints qui modifient les données (POST, PUT, DELETE) doivent être protégés par une authentification et une autorisation appropriées.
*   **Protection contre le Cross-Origin Resource Sharing (CORS)**: Configurez correctement les en-têtes CORS (Access-Control-Allow-Origin, etc.) sur le serveur pour limiter les requêtes provenant de domaines non autorisés.
*   **Utilisation de bibliothèques de sécurité**: Utilisez des bibliothèques de sécurité reconnues et maintenues pour gérer l'authentification, l'autorisation, la validation des données et la protection contre les vulnérabilités.
*   **Mise à jour régulière**: Assurez-vous de maintenir votre application et ses dépendances à jour pour corriger les vulnérabilités de sécurité connues.
*   **Surveillance et journalisation**: Mettez en place une surveillance et une journalisation complètes pour détecter les activités suspectes et les tentatives d'attaque.

=== Limitations et Considérations ===
*   Cette documentation est basée sur une analyse du projet et est sujette à des changements. **Consultez toujours la documentation officielle, le code source ou l'équipe de développement pour obtenir les informations les plus précises et à jour.**
*   Les endpoints et les paramètres listés sont des exemples et peuvent ne pas être complets. Certains endpoints et paramètres peuvent être spécifiques à des configurations ou à des modules particuliers.
*   Les limitations peuvent dépendre des droits d'accès de l'utilisateur. Les utilisateurs avec des rôles différents auront des permissions différentes.
*   Les formats de dates et d'heures (ex: `YYYY-MM-DD`) peuvent être soumis aux paramètres régionaux et aux configurations du serveur. Utilisez des formats de date et d'heure standardisés (ex: ISO 8601) pour éviter les ambiguïtés.
*   Considérez l'implémentation de la pagination pour les requêtes qui renvoient de grandes quantités de données (ex: `/astreintes`, `/primes`, `/projets`, `/collaborateurs`).
*   Documentez les limites de débit (rate limiting) et les quotas d'utilisation de l'API.

=== Contact et Support ===
*   Pour toute question, problème ou demande de clarification concernant l'API, veuillez contacter l'équipe de développement à l'adresse suivante : `<adresse_email_support>`.
*   **Pour signaler un problème**, veuillez fournir autant d'informations détaillées que possible, notamment :
    *   L'URL de l'API utilisée.
    *   La requête HTTP (méthode, URL, en-têtes, corps).
    *   La réponse reçue (codes de statut, corps de la réponse).
    *   Les informations de débogage (messages d'erreur, logs, captures d'écran).
    *   Les étapes pour reproduire le problème.
*   **Pour les demandes de nouvelles fonctionnalités ou d'améliorations**, veuillez fournir une description claire de votre demande, ainsi que les cas d'utilisation.
```
APPROVED:
```

---

# Données

---

```wiki
== Section DONNÉES ==

Cette section de la documentation détaille les modèles de données, les structures de données, et les flux de données de l'application WacitV2. Elle est conçue pour servir de ressource essentielle pour les développeurs, les testeurs, les nouveaux collaborateurs et toute personne impliquée dans la compréhension et la manipulation des données au sein de l'application. Une bonne compréhension de cette section est cruciale pour le développement, la maintenance et l'évolution du système.

### 1. Modèles de Données

Les modèles de données de WacitV2 sont principalement définis par les entités Doctrine. Ces entités, basées sur le modèle de données relationnel, représentent les différentes entités métier et leurs attributs, servant de fondation pour la persistance des données dans la base de données. Elles encapsulent la logique métier et les règles de validation associées aux données.

#### 1.1. Liste des Entités Principales

La liste suivante présente les entités principales de l'application, identifiées après une analyse du code source et des composants clés. Chaque entité est accompagnée d'une brève description de son rôle et de sa vocation. Il est important de noter que cette liste est sujette à évolution et reflète l'état actuel de l'application. Pour une compréhension exhaustive, il est fortement recommandé de consulter le code source et d'utiliser les outils de mapping fournis par Doctrine (par exemple, la commande `doctrine:mapping:info` de Symfony) afin d'analyser en détail les entités et leurs relations.

*   **AchatIts**: Gère les achats de matériel et de services IT, incluant les informations sur les fournisseurs, les articles commandés, les prix et les dates d'achat.
*   **Activity**: Représente les activités liées aux projets. Cela inclut des activités telles que le développement, les tests, la gestion de projet, et toute autre tâche associée à un projet.  Elle est souvent liée aux entités `Project` et `SkillActivity`.
*   **AppStatus**: Définit les différents statuts possibles de l'application (par exemple, "En cours", "Arrêtée", "Maintenance", "En ligne"). Utilisée pour surveiller et gérer l'état opérationnel de l'application.
*   **Astreinte**: Contient les informations relatives aux astreintes, notamment les dates de début et de fin, le collaborateur concerné, le type d'astreinte, et les détails associés (par exemple, les commentaires).
*   **ClassificationCoef**: Définit les coefficients utilisés pour la classification et l'évaluation des éléments (par exemple, des projets, des compétences, des risques).
*   **CmdCapAchats**: Gère les commandes de capital et d'achats, incluant les informations de commande, les articles achetés, les quantités, les prix unitaires, les dates, les fournisseurs et les détails financiers associés.
*   **Collaborator**: Représente les collaborateurs de l'entreprise. Contient des informations personnelles et professionnelles, telles que le nom, prénom, adresse email, numéro de téléphone, département, fonction, et informations de connexion.
*   **Costs**: Enregistre les coûts et les dépenses liés aux projets et aux activités, incluant les types de coûts, les montants, les dates, et les références aux projets ou aux activités.
*   **DateOpening**: Informations sur les dates d'ouverture, potentiellement liées à des processus spécifiques ou à des calendriers (par exemple, les jours d'ouverture d'un bureau ou d'un service).
*   **Departement**: Définit les différents départements de l'entreprise (par exemple, "Ressources Humaines", "Développement", "Marketing").
*   **Depense**: Enregistre les dépenses, qu'elles soient liées aux projets, aux collaborateurs ou à d'autres activités. Cela inclut les informations sur le type de dépense, le montant, la date, et le collaborateur concerné.
*   **DepenseStatus**: Gère les statuts des dépenses (par exemple, "Soumise", "Approuvée", "Rejetée", "En attente de validation", "Payée").
*   **DesignationExpense**: Contient la désignation des dépenses, permettant de catégoriser et de clarifier les types de dépenses (par exemple, "Frais de déplacement", "Fournitures de bureau").
*   **Devise**: Définit les différentes devises utilisées dans l'application (par exemple, EUR, USD, CHF).
*   **Dossier**: Représente les dossiers liés aux projets ou aux collaborateurs, permettant de regrouper des informations connexes (par exemple, documents, contrats, rapports).
*   **Dotation**: Gère les dotations et les allocations de ressources (par exemple, l'allocation de matériel, de budget, ou de personnel à un projet ou à un département).
*   **Etape**: Définit les étapes d'un processus, telles que les étapes d'un projet ou d'un workflow.
*   **Expense**: Représente les dépenses générales, incluant les informations sur le type de dépense, le montant, la date, et le collaborateur concerné. Similaire à `Depense`, mais peut avoir des utilisations spécifiques ou des relations différentes.
*   **Frequency**: Définit la fréquence des paiements ou d'autres activités récurrentes (par exemple, "Mensuel", "Trimestriel", "Annuel").
*   **GsmKey**: Gère les clés GSM, probablement liées à des collaborateurs ou à des équipements.
*   **HeureSup**: Enregistre les informations relatives aux heures supplémentaires, incluant le collaborateur, les dates et heures de début et de fin, et le type d'heure supplémentaire.
*   **HistoriqueForfait**: Stocke l'historique des forfaits (par exemple, les forfaits téléphoniques, les forfaits de données).
*   **HistoriqueValidation**: Conserve l'historique des validations, permettant de suivre les approbations et les rejets (par exemple, les validations des dépenses, des projets, des demandes).
*   **Imputation**: Gère les imputations comptables.
*   **Libelle**: Contient des libellés ou des descriptions utilisés dans l'application pour faciliter la localisation et la traduction.
*   **Order**: Représente les commandes et les ordres.
*   **OtherExpenses**: Enregistre les autres dépenses non catégorisées.
*   **PaimentMethode**: Définit les méthodes de paiement utilisées (par exemple, "Virement bancaire", "Carte de crédit", "Chèque").
*   **Permission**: Gère les permissions et les rôles des utilisateurs, contrôlant l'accès aux différentes fonctionnalités de l'application.
*   **PlaneTicket**: Enregistre les informations relatives aux billets d'avion.
*   **Prime**: Contient les informations relatives aux primes.
*   **Project**: Représente les projets, incluant les informations de base (nom, description, date de début, date de fin, chef de projet) et les relations avec d'autres entités (par exemple, les activités, les dépenses, les collaborateurs).
*   **ProjectValidation**: Gère la validation des projets, incluant les informations sur l'état de validation, les validateurs et les dates de validation.
*   **PublicHolidays**: Contient les informations relatives aux jours fériés.
*   **PurchasingSuppliers**: Définit les fournisseurs.
*   **RateExchange**: Gère les taux de change.
*   **Regularisation**: Enregistre les régularisations.
*   **SkillActivity**: Lie les activités aux compétences requises, permettant de définir les compétences nécessaires pour chaque activité.
*   **Transport**: Contient les informations relatives au transport.
*   **TypeAchat**: Définit les types d'achats (par exemple, "Fournitures", "Services", "Matériel").
*   **TypeAchatItics**: Définit les types d'achats ITICS.
*   **TypeAstreinte**: Définit les types d'astreintes (par exemple, "Astreinte téléphonique", "Astreinte sur site").
*   **TypeExpense**: Définit les types de dépenses (par exemple, "Frais de déplacement", "Fournitures", "Salaires").
*   **TypeForfait**: Définit les types de forfaits (par exemple, "Forfait téléphonique", "Forfait de données").
*   **TypeFrais**: Définit les types de frais (par exemple, "Frais de repas", "Frais de transport").
*   **TypeHeuresSup**: Définit les types d'heures supplémentaires (par exemple, "Heures supplémentaires de jour", "Heures supplémentaires de nuit").
*   **TypePrime**: Définit les types de primes (par exemple, "Prime de performance", "Prime d'ancienneté").
*   **TypeValidator**: Définit les types de validateurs.
*   **User**: Représente les utilisateurs du système, avec leurs informations de connexion et leurs rôles.
*   **UserBackup**: Contient les sauvegardes des utilisateurs.
*   **Workflow**: Définit les flux de travail.

#### 1.2. Exemple de Définition d'Entité (Conceptuel)

L'exemple suivant illustre la structure d'une entité Doctrine et ses annotations. Il est important de noter que ceci est une représentation simplifiée et ne reflète pas la totalité des attributs ou des relations que pourraient avoir les entités réelles dans l'application.

```php
<?php
// src/Entity/Collaborator.php
namespace App\Entity;

use Doctrine\ORM\Mapping as ORM;
use Symfony\Component\Validator\Constraints as Assert;

/**
 * @ORM\Entity
 * @ORM\Table(name="collaborator")
 */
class Collaborator
{
    /**
     * @ORM\Id
     * @ORM\GeneratedValue
     * @ORM\Column(type="integer")
     */
    private $id;

    /**
     * @ORM\Column(type="string", length=255)
     * @Assert\NotBlank
     * @Assert\Length(max=255)
     */
    private $firstName;

    /**
     * @ORM\Column(type="string", length=255)
     * @Assert\NotBlank
     * @Assert\Length(max=255)
     */
    private $lastName;

    /**
     * @ORM\Column(type="string", length=255, unique=true)
     * @Assert\NotBlank
     * @Assert\Email
     * @Assert\Length(max=255)
     */
    private $email;

    // ... autres attributs et méthodes (getters/setters)
}
```

*   **Description :** Cet exemple illustre l'entité `Collaborator`. Elle utilise les annotations Doctrine pour mapper les attributs aux colonnes de la base de données. L'annotation `@ORM\Entity` indique que la classe est une entité et sera mappée à une table dans la base de données. Les annotations `@ORM\Column` définissent le type et les contraintes des colonnes. Des contraintes de validation Symfony (par exemple, `@Assert\NotBlank`, `@Assert\Email`, `@Assert\Length`) sont également utilisées pour garantir l'intégrité des données au niveau de l'entité.
*   **Fichier Source :** `src/Entity/Collaborator.php`. Les autres entités sont définies dans le répertoire `src/Entity/`.
*   **Règles de gestion :** La structure et les types de données des attributs (par exemple, `string`, `integer`, `datetime`) doivent respecter les règles métier, telles que la validation des formats de noms, et les contraintes sur les valeurs des champs. Les contraintes de validation sont implémentées via les annotations Doctrine, les annotations Symfony (comme illustré dans l'exemple), ou par des validateurs personnalisés (voir la section 4.1). Ces règles assurent la cohérence et la qualité des données.

### 2. Structures de Données

Les structures de données de WacitV2 sont variées et incluent les entités Doctrine, les formulaires Symfony, et les structures de données côté client (JavaScript). Elles jouent un rôle crucial dans l'échange et la manipulation des données au sein de l'application, permettant une communication efficace entre le serveur et le client et assurant l'intégrité des informations.

#### 2.1. Relations Entre Entités

Les relations entre les entités sont définies grâce aux annotations Doctrine (par exemple, `@ORM\ManyToOne`, `@ORM\OneToMany`, `@ORM\ManyToMany`). Ces relations définissent la manière dont les entités sont connectées et comment les données sont liées, et sont essentielles pour le bon fonctionnement de l'application. La définition précise de ces relations est cruciale pour l'intégrité référentielle, la cohérence des données, et l'efficacité des requêtes de la base de données.

*   **Types de relations :**
    *   **OneToOne :** Une entité est associée à une autre entité.
    *   **OneToMany :** Une entité est associée à plusieurs autres entités.
    *   **ManyToOne :** Plusieurs entités sont associées à une seule entité (relation inverse de OneToMany).
    *   **ManyToMany :** Plusieurs entités sont associées à plusieurs autres entités.

*   **Exemple (Conceptuel) :**

```php
<?php
// src/Entity/Project.php
namespace App\Entity;

use Doctrine\ORM\Mapping as ORM;
use Doctrine\Common\Collections\ArrayCollection;

/**
 * @ORM\Entity
 */
class Project
{
    /**
     * @ORM\Id
     * @ORM\GeneratedValue
     * @ORM\Column(type="integer")
     */
    private $id;

    /**
     * @ORM\Column(type="string", length=255)
     */
    private $name;

    /**
     * @ORM\OneToMany(targetEntity="Expense", mappedBy="project")
     */
    private $expenses;

    public function __construct()
    {
        $this->expenses = new ArrayCollection();
    }

    // ...
}
```

```php
<?php
// src/Entity/Expense.php
namespace App\Entity;

use Doctrine\ORM\Mapping as ORM;

/**
 * @ORM\Entity
 */
class Expense
{
    /**
     * @ORM\Id
     * @ORM\GeneratedValue
     * @ORM\Column(type="integer")
     */
    private $id;

    /**
     * @ORM\Column(type="decimal", precision=10, scale=2)
     */
    private $amount;

    /**
     * @ORM\ManyToOne(targetEntity="Project", inversedBy="expenses")
     * @ORM\JoinColumn(name="project_id", referencedColumnName="id")
     */
    private $project;

    // ...
}
```

*   **Description :** L'exemple montre une relation `OneToMany` entre `Project` et `Expense`. Un projet peut avoir plusieurs dépenses. L'entité `Expense` utilise la relation `ManyToOne` pour se connecter à un `Project`, et définit la clé étrangère `project_id` dans la table `expense`. L'attribut `mappedBy` dans l'entité `Project` indique le nom du champ (ici, `project`) dans l'entité `Expense` qui contient la relation inverse. La classe `ArrayCollection` est utilisée pour gérer la collection de dépenses associées à un projet. L'attribut `amount` est un exemple de champ de type `decimal` avec une précision et une échelle définies.
*   **Importance :** Comprendre les relations entre les entités est essentiel pour naviguer dans le code source, comprendre le modèle de données et effectuer des requêtes efficaces.

#### 2.2. Formulaires

Les formulaires Symfony sont utilisés pour la saisie, la validation, et la manipulation des données. Ils offrent une approche structurée et maintenable pour la gestion des données entrantes. Les formulaires Symfony simplifient l'interaction avec les utilisateurs et garantissent l'intégrité des données grâce à des mécanismes de validation intégrés et personnalisables.

*   **Fichiers Source :** Les définitions des formulaires se trouvent généralement dans le répertoire `src/Form/*Type.php`.

*   **Fonctionnalités clés :**
    *   **Définition des champs :** Définition des champs de saisie (text, number, date, select, etc.)
    *   **Validation :** Intégration de validateurs pour assurer la validité des données (longueur, format, contraintes métier).
    *   **Gestion des données :** Liaison avec les entités Doctrine (via l'option `data_class`) pour la création et la mise à jour des objets.
    *   **Personnalisation :** Possibilité de personnaliser l'apparence et le comportement des formulaires.

*   **Exemple :** (Simplifié)

```php
<?php
// src/Form/ProjectType.php
namespace App\Form;

use Symfony\Component\Form\AbstractType;
use Symfony\Component\Form\FormBuilderInterface;
use Symfony\Component\Form\Extension\Core\Type\TextType;
use Symfony\Component\Form\Extension\Core\Type\DateType;
use Symfony\Component\OptionsResolver\OptionsResolver;
use Symfony\Component\Validator\Constraints as Assert;

class ProjectType extends AbstractType
{
    public function buildForm(FormBuilderInterface $builder, array $options)
    {
        $builder
            ->add('name', TextType::class, [
                'label' => 'Nom du projet',
                'constraints' => [
                    new Assert\NotBlank(),
                    new Assert\Length(['max' => 255]),
                ],
            ])
            ->add('startDate', DateType::class, [
                'label' => 'Date de début',
                'widget' => 'single_text',
            ])
            // ...
        ;
    }

    public function configureOptions(OptionsResolver $resolver)
    {
        $resolver->setDefaults([
            'data_class' => 'App\Entity\Project', // Classe de l'entité liée au formulaire
        ]);
    }
}
```

*   **Description :** Le formulaire `ProjectType` est utilisé pour créer ou modifier un projet. Il définit les champs (nom, date de début, etc.) et peut inclure des validateurs. La classe `ProjectType` est liée à l'entité `Project` via l'option `data_class`. L'exemple montre l'utilisation de contraintes de validation (par exemple, `Assert\NotBlank`, `Assert\Length`) pour garantir que le champ "name" ne soit pas vide et ne dépasse pas 255 caractères. Le widget `single_text` est utilisé pour l'affichage de la date de début dans un champ texte.
*   **Règles de gestion :** Les validateurs définis dans les formulaires assurent le respect des règles métier. Par exemple, la validation du nom d'un projet pour vérifier qu'il ne dépasse pas une certaine longueur, ou la validation de la date de début pour s'assurer qu'elle est bien définie. Les validateurs peuvent être définis directement dans le formulaire (comme dans l'exemple) ou via des classes de validation dédiées (voir la section 4.1).

#### 2.3. Structures Côté Client (JavaScript)

Les structures de données côté client (JavaScript) sont cruciales pour l'interaction dynamique avec les données dans le navigateur. Elles permettent de manipuler et d'afficher les données reçues du serveur, de gérer les interactions utilisateur et de soumettre des requêtes au serveur. Ces structures facilitent une expérience utilisateur riche et réactive.

*   **Fonctionnalités clés :**
    *   **Réception des données :** Réception des données du serveur, généralement au format JSON, via des appels API.
    *   **Manipulation des données :** Manipulation et transformation des données en utilisant des objets JavaScript.
    *   **Affichage des données :** Affichage dynamique des données dans l'interface utilisateur (par exemple, en utilisant des frameworks comme React, Vue.js, ou Angular).
    *   **Validation côté client :** Validation des données saisies par l'utilisateur avant de les envoyer au serveur, pour une meilleure expérience utilisateur.
    *   **Interaction avec le serveur :** Envoi de requêtes au serveur (par exemple, via AJAX) pour effectuer des opérations CRUD (Create, Read, Update, Delete).

*   **Fichiers Source :** Les fichiers JavaScript se trouvent généralement dans le répertoire `public/assets/js/*.js` ou dans d'autres répertoires spécifiques au framework frontend utilisé (par exemple, `src/components` pour React).

*   **Exemple (Conceptuel) :**

```javascript
// Exemple de structure de données en JavaScript
const project = {
    id: 123,
    name: "Projet WacitV2",
    startDate: "2024-01-01",
    endDate: "2024-12-31",
    status: "En cours",
    // ... autres propriétés
};

// Exemple d'utilisation d'une bibliothèque de validation (Yup)
import * as yup from 'yup';

const projectSchema = yup.object().shape({
    name: yup.string().required().max(255),
    startDate: yup.date().required(),
    // ...
});

async function validateProject(project) {
    try {
        await projectSchema.validate(project);
        return true; // Validation réussie
    } catch (error) {
        console.error("Erreur de validation :", error.errors);
        return false; // Validation échouée
    }
}
```

*   **Description :** Les structures de données en JavaScript sont généralement des objets JavaScript qui correspondent aux données des entités. Par exemple, un objet `project` représente un projet et contient des propriétés qui correspondent aux attributs de l'entité `Project`. Les données sont souvent récupérées via les API du backend, au format JSON. L'exemple montre également l'utilisation de la bibliothèque Yup pour la validation côté client.
*   **Règles de gestion :** La validation des données côté client (par exemple, dans un formulaire en JavaScript) aide à améliorer l'expérience utilisateur en détectant les erreurs de saisie avant l'envoi au serveur. Les validations doivent dupliquer une partie des règles de gestion présentes côté serveur pour une cohérence et une sécurité optimale. Les bibliothèques de validation JavaScript (par exemple, Yup, Joi) peuvent être utilisées pour faciliter l'implémentation des validations.

### 3. Flux de Données

Cette section décrit les principaux flux de données dans l'application WacitV2, en partant de l'interaction de l'utilisateur jusqu'à la persistance des données en base. Elle détaille les étapes clés impliquées dans le traitement des données, de l'interface utilisateur au stockage persistant.

#### 3.1. Flux de Données Généraux

Ce flux décrit le processus global de gestion des données dans l'application. Il fournit une vue d'ensemble des interactions entre les différents composants de l'application, depuis l'interface utilisateur jusqu'à la base de données.

1.  **Interaction Utilisateur :** Un utilisateur interagit avec l'interface web (par exemple, en remplissant un formulaire, en cliquant sur un bouton, en sélectionnant des options).
2.  **Requête HTTP :** L'interface web envoie une requête HTTP (GET, POST, PUT, DELETE) au backend (Symfony). Les requêtes peuvent inclure des données (par exemple, les données d'un formulaire) au format JSON ou sous d'autres formats.
3.  **Routage :** Symfony route la requête vers le contrôleur approprié en fonction de l'URL et de la méthode HTTP (GET, POST, PUT, DELETE). Le routage est défini dans les fichiers de configuration de Symfony (par exemple, `config/routes.yaml`).
4.  **Traitement de la Requête :** Le contrôleur exécute la logique métier. Il peut appeler des services, manipuler les entités Doctrine, valider les données, et effectuer d'autres opérations nécessaires au traitement de la requête.
5.  **Validation des Données :** Les données sont validées au niveau du contrôleur et/ou des services, en utilisant les validateurs définis dans les formulaires Symfony, les annotations Doctrine, ou des classes de validation personnalisées.
6.  **Accès à la Base de Données :** Les services utilisent Doctrine (EntityManager) pour interagir avec la base de données (lecture, écriture, mise à jour). Les opérations CRUD (Create, Read, Update, Delete) sont effectuées sur les entités Doctrine.
7.  **Gestion des Transactions :** Les opérations de base de données peuvent être gérées dans des transactions pour garantir l'intégrité des données. En cas d'erreur, la transaction est annulée (rollback) pour éviter les incohérences.
8.  **Réponse HTTP :** Le backend renvoie une réponse HTTP au frontend. La réponse peut inclure des données (par exemple, au format JSON pour les API) ou des messages de succès/erreur. Le code de statut HTTP indique le résultat de la requête (par exemple, 200 OK, 201 Created, 400 Bad Request, 500 Internal Server Error).
9.  **Mise à Jour de l'Interface Utilisateur :** Le frontend traite la réponse HTTP et met à jour l'interface utilisateur. Cela peut inclure l'affichage des données, l'affichage de messages de succès/erreur, la redirection vers une autre page, ou la mise à jour dynamique de certains éléments de l'interface.

#### 3.2. Flux de Données pour la Gestion des Astreintes

Ce flux de données détaille le processus de gestion des astreintes, de la saisie des informations à la validation et à la persistance en base de données. Ce processus est essentiel pour assurer le suivi et la gestion efficace des astreintes.

1.  **Saisie de l'Astreinte :** L'utilisateur (par exemple, un agent ou un responsable) saisit les informations relatives à une astreinte via un formulaire. Ce formulaire est généralement géré par un formulaire Symfony (`AstreinteType`). Les champs du formulaire incluent typiquement la date, l'agent concerné, les heures de début et de fin, le type d'astreinte et éventuellement des commentaires.
2.  **Validation du Formulaire :** Le formulaire est validé. La validation peut être effectuée côté client (JavaScript) pour une meilleure expérience utilisateur et côté serveur (Symfony) pour garantir l'intégrité des données. Les validateurs vérifient le format et la cohérence des données saisies, par exemple, que les dates sont valides, que l'agent existe, et que les heures de début et de fin sont cohérentes.
3.  **Création/Mise à Jour de l'Entité Astreinte :** Si la validation réussit, une entité `Astreinte` est créée ou mise à jour en utilisant les données du formulaire. L'entité est liée à l'utilisateur ou au collaborateur concerné.
4.  **Calcul et Valorisation des Données (si nécessaire) :** Avant la persistance, des calculs peuvent être effectués (par exemple, calcul de la durée de l'astreinte en heures).
5.  **Persistance :** L'entité `Astreinte` est persistée dans la base de données en utilisant Doctrine (EntityManager).
6.  **Validation (par un Responsable) :** Un responsable valide l'astreinte. Cette étape peut impliquer des contrôles supplémentaires et des mises à jour de l'état de l'astreinte (par exemple, l'approbation ou le rejet).
7.  **Historisation des modifications :** Les modifications et les validations sont stockées dans l'historique des validations.
8.  **Notifications (si applicable):** Des notifications peuvent être envoyées (par email, etc.) pour informer les parties prenantes (par exemple, le collaborateur concerné, le responsable) de l'état de l'astreinte (par exemple, soumission, validation, rejet). Ces notifications sont généralement gérées par des services de notification.

#### 3.3. Flux de Données pour la Gestion des Projets

Ce flux de données décrit le processus de gestion des projets, de la création à la validation, en passant par l'ajout de tâches et d'étapes. Ce processus est fondamental pour la gestion des projets au sein de l'application.

1.  **Création d'un Projet :** Un utilisateur (par exemple, un chef de projet ou un administrateur) crée un nouveau projet en remplissant un formulaire (par exemple, `ProjectType`). Le formulaire inclut des champs tels que le nom du projet, la description, la date de début, la date de fin, le chef de projet, et éventuellement d'autres informations.
2.  **Validation du Formulaire :** Le formulaire est validé côté client et/ou côté serveur. Les validateurs vérifient que les informations sont valides et respectent les règles métier (par exemple, la date de fin ne peut pas être antérieure à la date de début, le chef de projet doit être un collaborateur existant).
3.  **Création de l'Entité Project :** Si la validation réussit, une entité `Project` est créée en utilisant les données du formulaire. L'entité est ensuite initialisée avec les informations saisies.
4.  **Persistance en Base de Données :** L'entité `Project` est persistée dans la base de données en utilisant Doctrine (EntityManager).
5.  **Gestion des Étapes/Tâches du Projet :** Des étapes ou des tâches sont ajoutées, modifiées ou supprimées. Ces opérations peuvent impliquer la création, la mise à jour, ou la suppression d'entités telles que `Activity` ou `Etape`. Chaque étape ou tâche peut être associée à des informations spécifiques (par exemple, la description, la date de début, la date de fin, l'état d'avancement, les ressources allouées).
6.  **Gestion des Ressources :** Gestion de l'allocation des ressources au projet.
7.  **Suivi de l'avancement :** Le suivi de l'avancement du projet est effectué, avec une mise à jour régulière de l'état des différentes étapes et tâches.
8.  **Validation du Projet (si applicable):** Un responsable valide le projet. Cette étape peut impliquer des contrôles supplémentaires et une vérification de la conformité du projet avec les objectifs définis. Des vérifications sont faites sur l'avancement global du projet.
9.  **Clôture du projet (si applicable) :** Le projet est clôturé après validation.

#### 3.4. Flux de Données pour l'Import de Données

Ce flux décrit le processus d'importation de données à partir de fichiers, permettant d'intégrer des données externes dans l'application. Ce processus est essentiel pour l'intégration de données en provenance d'autres systèmes ou de fichiers.

*   **Fichiers Source :** Des fichiers CSV, Excel, ou d'autres formats peuvent être importés. Ces fichiers contiennent les données à importer et doivent respecter une structure définie (par exemple, avec des colonnes spécifiques pour chaque attribut).
*   **Commandes :** Des commandes Symfony (situées dans le répertoire `src/Command/`) sont utilisées pour importer les données. Ces commandes sont des scripts PHP qui traitent les fichiers et effectuent les opérations nécessaires pour intégrer les données dans la base de données.
*   **Fonctionnement des Commandes d'importation :**
    1.  **Lecture du fichier :** La commande lit le fichier source (CSV, Excel, etc.).
    2.  **Transformation des données :** Les données sont transformées pour correspondre aux structures de données de l'application (par exemple, en mappant les colonnes du fichier aux attributs des entités Doctrine).
    3.  **Validation des données :** Les données sont validées pour garantir leur intégrité et leur conformité aux règles métier (par exemple, vérification des formats, unicité des valeurs).
    4.  **Persistance des données :** Les données validées sont persistées dans la base de données en utilisant Doctrine (EntityManager).
*   **Exemple d'utilisation d'une commande :**

```bash
php bin/console app:import-table-collaborator --file=data/collaborators.csv
```

*   **Fichiers Source (Exemple) :**

```csv
id,first_name,last_name,email
1,John,Doe,john.doe@example.com
2,Jane,Smith,jane.smith@example.com
```

*   **Description :** Les commandes d'importation traitent des fichiers (CSV, Excel...) et les intègrent dans la base de données en utilisant des entités Doctrine et des requêtes SQL ou des méthodes ORM. Elles permettent d'importer des données en masse et de les intégrer rapidement dans l'application. Les commandes d'importation facilitent l'intégration de données externes dans l'application.
*   **Règles de gestion :** Les commandes d'importation doivent gérer les erreurs (par exemple, les données mal formatées, les doublons) et suivre les règles métier (ex: validation des données lors de l'importation). Des mécanismes de logging doivent être implémentés pour faciliter le suivi des opérations d'importation. Des tests unitaires devraient être inclus pour garantir la qualité de l'import. Les commandes d'importation devraient offrir des options pour gérer les doublons (par exemple, en mettant à jour les enregistrements existants ou en ignorant les doublons).

### 4. Règles de Gestion et Règles Métiers (Résumé)

Cette section résume les règles métier et de gestion les plus importantes liées aux données dans WacitV2. Ces règles garantissent la cohérence, l'intégrité, la sécurité et la conformité des données. Leur respect est essentiel pour le bon fonctionnement de l'application et la qualité des données.

#### 4.1. Validation des Données

La validation des données est essentielle pour garantir la qualité des données. Elle s'applique à plusieurs niveaux, notamment dans les formulaires Symfony, les entités Doctrine et les validations côté client (JavaScript). La validation assure que les données saisies et stockées respectent les exigences définies.

*   **Formats des données :** Les champs doivent respecter des formats spécifiques (date, email, numéros de téléphone, codes postaux, etc.). L'application utilise des validateurs pour vérifier la conformité des données aux formats attendus.
*   **Champs obligatoires :** Certains champs sont obligatoires (par exemple, le nom d'un collaborateur, la date d'une astreinte, le nom d'un projet). Les validateurs vérifient que ces champs ne sont pas vides.
*   **Plages de valeurs :** Certaines valeurs doivent se situer dans des plages spécifiques (par exemple, les heures supplémentaires doivent être positives, les pourcentages doivent être entre 0 et 100). Les validateurs garantissent que les valeurs sont dans les plages autorisées.
*   **Unicité :** Certains champs doivent être uniques (par exemple, l'adresse email d'un collaborateur, le nom d'un projet). Les validateurs vérifient l'unicité des valeurs.
*   **Cohérence et Intégrité Référentielle :** La validation doit garantir la cohérence entre les données et l'intégrité des relations entre les entités (par exemple, vérifier qu'un chef de projet existe dans la table des collaborateurs).

#### 4.2. Règles Métiers Liées aux Astreintes

Ces règles sont spécifiques à la gestion des astreintes.

*   **État du Collaborateur :** Une astreinte ne peut être validée que si l'agent est actif. La validation vérifie l'état du collaborateur avant de valider l'astreinte.
*   **Calcul de la Durée :** Les durées d'astreinte sont calculées sur la base de la date et de l'heure de début et de fin. Des règles spécifiques sont appliquées pour les chevauchements et les interruptions.
*   **Gestion des Cas Exceptionnels :** La gestion des cas exceptionnels (astreintes non validées, erreurs de saisie, etc.) est assurée par des mécanismes de gestion des erreurs et des alertes. Des contrôles et des règles spécifiques sont définis pour traiter ces cas.
*   **Types d'Astreinte :** Les règles de gestion peuvent dépendre du type d'astreinte (par exemple, astreinte téléphonique, astreinte sur site). Des règles spécifiques peuvent s'appliquer en fonction du type d'astreinte.

#### 4.3. Règles Métiers Liées aux Pro

---

# Sécurité

---

```markdown
# Section Sécurité de WacitV2

## 1. Introduction

Cette section de la documentation détaille les mécanismes de sécurité, d'authentification et d'autorisation implémentés dans l'application WacitV2. Elle est conçue pour fournir une compréhension claire et complète des mesures de sécurité aux développeurs, aux testeurs, aux administrateurs et aux nouveaux membres de l'équipe. La documentation est maintenue à jour afin de refléter les évolutions de la sécurité de l'application et d'incorporer les meilleures pratiques en matière de sécurité informatique.

## 2. Vue d'ensemble des mécanismes de sécurité

WacitV2 adopte une approche de sécurité multicouche, s'appuyant sur les composants de Symfony, les bonnes pratiques de développement sécurisé, et des configurations spécifiques. L'objectif principal est de protéger les données, les fonctionnalités de l'application et son intégrité contre les accès non autorisés et les attaques potentielles.

Les principaux mécanismes de sécurité mis en œuvre sont les suivants :

*   **Authentification**: Vérification de l'identité de l'utilisateur. Ce processus permet de s'assurer que l'utilisateur accédant à l'application est bien celui qu'il prétend être.
*   **Autorisation**: Contrôle d'accès aux ressources et aux fonctionnalités de l'application, basé sur le rôle et les permissions de l'utilisateur authentifié. Ce mécanisme assure que seuls les utilisateurs autorisés peuvent accéder à certaines parties de l'application.
*   **Protection contre les attaques courantes**: Prévention et mitigation des vulnérabilités connues telles que les attaques XSS (Cross-Site Scripting), CSRF (Cross-Site Request Forgery) et l'injection SQL. Cela inclut des mesures pour garantir la sécurité des données et l'intégrité de l'application.
*   **Gestion des sessions sécurisées**: Mise en place de mécanismes pour sécuriser les sessions utilisateurs, incluant l'utilisation de cookies sécurisés et des stratégies de renouvellement de session.
*   **Validation et assainissement des entrées**: Validation rigoureuse des données fournies par les utilisateurs et assainissement des données afin de prévenir les attaques par injection et autres failles liées aux données.

## 3. Authentification

### 3.1. Mécanismes d'Authentification

WacitV2 utilise le composant de sécurité de Symfony pour gérer l'authentification, offrant une flexibilité pour s'adapter à différents scénarios d'authentification. Les stratégies d'authentification sont configurées en fonction des besoins spécifiques de l'application.

Les mécanismes d'authentification suivants sont actuellement supportés :

*   **Authentification par formulaire**: L'utilisateur fournit un identifiant (généralement une adresse e-mail ou un nom d'utilisateur) et un mot de passe via un formulaire de connexion. Ce mécanisme est couramment utilisé pour l'accès aux interfaces web.
*   **Authentification via JWT (JSON Web Tokens)**: Pour les API, les JWT sont utilisés pour authentifier les requêtes. Le client envoie un token dans l'en-tête `Authorization` de chaque requête, utilisant le schéma `Bearer`. Ce mécanisme permet une authentification sans état (stateless) et est particulièrement adapté aux applications distribuées et aux architectures de microservices.
*   **Autres Méthodes (potentiellement)**: En fonction des besoins spécifiques du projet, d'autres méthodes d'authentification telles que OAuth ou SAML pourraient être intégrées. L'intégration de ces méthodes se ferait également via le composant de sécurité de Symfony, en configurant les *providers* et les *firewalls* en conséquence.

### 3.2. Fichiers et Composants Clés

Les fichiers et composants suivants sont essentiels pour la gestion de l'authentification :

*   **`config/packages/security.yaml`**: Ce fichier de configuration est le point central pour la configuration de la sécurité dans Symfony. Il définit les mécanismes d'authentification (formulaire, JWT, etc.), les *User Providers* (fournisseurs d'utilisateurs), les *password encoders* (encodeurs de mots de passe), les règles de pare-feu (firewalls) et les stratégies de déconnexion.

    ```yaml
    # config/packages/security.yaml
    security:
        password_hashers:
            App\\Entity\\User: 'auto' # Utilise l'encodeur de mot de passe recommandé par Symfony (Argon2i par défaut)
        providers:
            app_user_provider: # Définition du User Provider. Remplacez 'email' par l'attribut utilisé pour l'identification (ex: username).
                entity:
                    class: App\Entity\User
                    property: email
        firewalls:
            dev:
                pattern: ^/(_(profiler|wdt)|css|js)/
                security: false # Désactive la sécurité pour les URLs de développement (profiler, etc.)
            main:
                lazy: true
                provider: app_user_provider
                custom_authenticator: App\Security\AppCustomAuthenticator # Utilisation de l'authentificateur personnalisé
                logout:
                    path: app_logout # URL de déconnexion
                    # where to redirect after logout
                    # target: app_any_route
                # ... autres configurations du firewall, notamment access_control
    ```

    **Explication des principaux éléments :**

    *   `password_hashers`: Définit l'algorithme utilisé pour hacher les mots de passe des utilisateurs. `'auto'` sélectionne l'algorithme recommandé par Symfony (Argon2i par défaut). Il est crucial de *ne jamais* stocker les mots de passe en clair. L'utilisation de l'algorithme Argon2i est fortement recommandée pour une sécurité accrue.
    *   `providers`: Définit comment l'application récupère les utilisateurs. Dans l'exemple, il utilise une entité `User` stockée dans une base de données et identifiée par son adresse e-mail. Le `property` définit l'attribut de l'entité `User` utilisé pour l'authentification (par exemple, `email` ou `username`).
    *   `firewalls`: Définit les zones de sécurité de l'application.
        *   `dev`: Désactive la sécurité pour les ressources de développement (profiler, etc.).
        *   `main`: La zone principale de l'application. Elle utilise l'authentificateur personnalisé (`AppCustomAuthenticator`) et le `User Provider` défini précédemment. La section `logout` configure la gestion de la déconnexion. L'option `lazy: true` optimise le chargement de la sécurité.

*   **`src/Security/AppCustomAuthenticator.php`**:  Ce fichier contient la logique d'authentification personnalisée. Il est utilisé lorsque des exigences spécifiques en matière d'authentification sont nécessaires, comme la gestion des redirections après la connexion, la validation d'identifiants supplémentaires, ou l'intégration avec des systèmes d'authentification externes. L'authentificateur implémente l'interface `AuthenticatorInterface` ou étend la classe `AbstractLoginFormAuthenticator` pour gérer le processus d'authentification.

    ```php
    <?php

    namespace App\Security;

    use App\Entity\User;
    use Doctrine\ORM\EntityManagerInterface;
    use Symfony\Component\HttpFoundation\RedirectResponse;
    use Symfony\Component\HttpFoundation\Request;
    use Symfony\Component\HttpFoundation\Response;
    use Symfony\Component\Routing\Generator\UrlGeneratorInterface;
    use Symfony\Component\Security\Core\Authentication\Token\TokenInterface;
    use Symfony\Component\Security\Core\Security;
    use Symfony\Component\Security\Http\Authenticator\AbstractLoginFormAuthenticator;
    use Symfony\Component\Security\Http\Authenticator\Passport\Badge\CsrfTokenBadge;
    use Symfony\Component\Security\Http\Authenticator\Passport\Badge\RememberMeBadge;
    use Symfony\Component\Security\Http\Authenticator\Passport\Credentials\PasswordCredentials;
    use Symfony\Component\Security\Http\Authenticator\Passport\Passport;
    use Symfony\Component\Security\Http\Util\TargetPathTrait;
    use Symfony\Component\PasswordHasher\Hasher\UserPasswordHasherInterface;

    class AppCustomAuthenticator extends AbstractLoginFormAuthenticator
    {
        use TargetPathTrait;

        public const LOGIN_ROUTE = 'app_login';

        private UrlGeneratorInterface $urlGenerator;
        private EntityManagerInterface $entityManager;
        private UserPasswordHasherInterface $passwordHasher;

        public function __construct(UrlGeneratorInterface $urlGenerator, EntityManagerInterface $entityManager, UserPasswordHasherInterface $passwordHasher)
        {
            $this->urlGenerator = $urlGenerator;
            $this->entityManager = $entityManager;
            $this->passwordHasher = $passwordHasher;
        }

        public function authenticate(Request $request): Passport
        {
            $email = $request->request->get('email', '');
            $request->getSession()->set(Security::LAST_USERNAME, $email);

            return new Passport(
                new \Symfony\Component\Security\Core\User\UserBadge($email, function (string $userIdentifier) {
                    $user = $this->entityManager->getRepository(User::class)->findOneBy(['email' => $userIdentifier]);

                    if (!$user) {
                        return null;
                    }

                    return $user;
                }),
                new PasswordCredentials($request->request->get('password', '')),
                [
                    new CsrfTokenBadge('authenticate', $request->request->get('_csrf_token')),
                    new RememberMeBadge(),
                ]
            );
        }

        public function onAuthenticationSuccess(Request $request, TokenInterface $token, string $firewallName): ?Response
        {
            if ($targetPath = $this->getTargetPath($request->getSession(), $firewallName)) {
                return new RedirectResponse($targetPath);
            }

            return new RedirectResponse($this->urlGenerator->generate('app_homepage')); // Redirige vers la page d'accueil après la connexion
        }

        protected function getLoginUrl(Request $request): string
        {
            return $this->urlGenerator->generate(self::LOGIN_ROUTE);
        }
    }
    ```

    **Explication du code :**

    *   `authenticate()` : Cette méthode est appelée pour authentifier l'utilisateur. Elle récupère les informations d'identification (email et mot de passe) de la requête et crée un objet `Passport`.  L'objet `Passport` encapsule les informations d'identification et les badges (par exemple, le jeton CSRF et la fonctionnalité "se souvenir de moi"). La méthode récupère également l'utilisateur depuis la base de données.
    *   `onAuthenticationSuccess()` :  Cette méthode est appelée en cas de succès de l'authentification. Elle redirige l'utilisateur vers la page demandée initialement (si une URL de redirection a été enregistrée) ou vers la page d'accueil.
    *   `getLoginUrl()` :  Retourne l'URL de la page de connexion.

*   **Entité `User` (`src/Entity/User.php`)**: Cette entité représente les utilisateurs de l'application et contient les informations d'authentification, telles que l'adresse e-mail, le mot de passe haché, et les rôles. Elle implémente les interfaces `UserInterface` et `PasswordAuthenticatedUserInterface`.

    ```php
    <?php

    namespace App\Entity;

    use Doctrine\ORM\Mapping as ORM;
    use Symfony\Component\Security\Core\User\PasswordAuthenticatedUserInterface;
    use Symfony\Component\Security\Core\User\UserInterface;

    #[ORM\Entity(repositoryClass: UserRepository::class)]
    class User implements UserInterface, PasswordAuthenticatedUserInterface
    {
        #[ORM\Id]
        #[ORM\GeneratedValue]
        #[ORM\Column]
        private ?int $id = null;

        #[ORM\Column(length: 180, unique: true)]
        private ?string $email = null;

        #[ORM\Column(length: 255)]
        private ?string $password = null;

        #[ORM\Column(type: 'json')]
        private array $roles = [];

        // ... Getters et Setters ...

        public function getRoles(): array
        {
            $roles = $this->roles;
            // guarantee every user at least has ROLE_USER
            $roles[] = 'ROLE_USER';

            return array_unique($roles);
        }

        public function setRoles(array $roles): self
        {
            $this->roles = $roles;

            return $this;
        }

        public function getPassword(): string
        {
            return $this->password;
        }

        public function setPassword(string $password): self
        {
            $this->password = $password;

            return $this;
        }

        public function getEmail(): ?string
        {
            return $this->email;
        }

        public function setEmail(string $email): self
        {
            $this->email = $email;

            return $this;
        }

        public function getUserIdentifier(): string
        {
            return (string) $this->email;
        }

    }
    ```

    **Explication du code :**

    *   L'entité `User` implémente les interfaces `UserInterface` et `PasswordAuthenticatedUserInterface`.
    *   `getUserIdentifier()`: Retourne l'identifiant unique de l'utilisateur (ici, l'adresse e-mail).  Cet identifiant est utilisé pour charger l'utilisateur depuis le *User Provider*.
    *   `getPassword()`: Retourne le mot de passe haché.
    *   `getRoles()` et `setRoles()`: Gèrent les rôles de l'utilisateur. Chaque utilisateur a au moins le rôle `ROLE_USER`.

### 3.3. Processus d'Authentification (Formulaire)

Le processus d'authentification par formulaire se déroule en plusieurs étapes :

1.  **Requête de Connexion**: L'utilisateur soumet le formulaire de connexion, en fournissant son identifiant (généralement l'adresse e-mail) et son mot de passe.
2.  **Authentification**: L'`AppCustomAuthenticator` (ou l'authentificateur par défaut de Symfony) récupère les identifiants soumis.
3.  **Validation**: L'authentificateur utilise le `User Provider` pour charger l'utilisateur correspondant à l'identifiant fourni. Le mot de passe soumis est validé par rapport au mot de passe haché stocké dans la base de données, en utilisant l'encodeur de mot de passe défini dans `security.yaml`.
4.  **Session**: Si l'authentification est réussie, une session est créée pour l'utilisateur, et l'objet utilisateur est stocké dans la session. L'utilisation de sessions sécurisées (avec des paramètres tels que `cookie: { secure: true, httponly: true }` dans la configuration du firewall) est cruciale pour la sécurité.
5.  **Redirection**: L'utilisateur est redirigé vers la page demandée initialement (si une URL de redirection a été enregistrée) ou vers la page d'accueil.

### 3.4. Authentification via JWT (si API)

Dans le cas d'une API, l'authentification JWT se déroule généralement comme suit :

1.  **Requête de Connexion**: L'utilisateur envoie ses identifiants (identifiant et mot de passe) à un endpoint d'authentification (par exemple, `/api/login`).
2.  **Validation**: Le backend valide les identifiants fournis. Cette validation doit inclure des vérifications de sécurité, telles que la limitation du nombre de tentatives de connexion.
3.  **Génération du JWT**: Si l'authentification est réussie, le backend génère un JWT signé et le renvoie au client. Le JWT contient généralement des informations sur l'utilisateur (ID, rôles, etc.).  Le JWT doit être généré avec une clé secrète forte et une durée de vie limitée.
4.  **Utilisation du JWT**: Le client inclut le JWT dans l'en-tête `Authorization` de chaque requête API, en utilisant le schéma `Bearer` (ex: `Authorization: Bearer <token>`).
5.  **Vérification du JWT**: Le backend vérifie le JWT à chaque requête API. Cela implique de vérifier la signature du token, sa date d'expiration, et les informations qu'il contient.  Il est également important de vérifier que le JWT n'a pas été révoqué.

## 4. Autorisation

### 4.1. Mécanismes d'Autorisation

L'autorisation contrôle l'accès aux ressources et aux fonctionnalités de l'application *après* l'authentification. WacitV2 utilise plusieurs mécanismes pour gérer l'autorisation, offrant une flexibilité pour définir des règles d'accès précises :

*   **Rôles**: Les utilisateurs se voient attribuer des rôles (ex: `ROLE_ADMIN`, `ROLE_USER`, `ROLE_MODERATEUR`). Les rôles sont des groupes de permissions qui simplifient la gestion des autorisations.
*   **Permissions**: Les rôles sont associés à des permissions qui définissent les actions qu'un utilisateur peut effectuer (ex: `EDIT_PROJECT`, `VIEW_ASTREINTE`, `CREATE_USER`). Les permissions sont souvent gérées au niveau des contrôleurs ou des services, en utilisant des annotations telles que `@IsGranted`.
*   **Voters (Symfony)**: Les *Voters* de Symfony permettent d'implémenter une logique d'autorisation plus complexe et personnalisée. Ils permettent de définir des règles d'accès basées sur des attributs spécifiques (par exemple, l'appartenance à un projet, ou le statut d'une ressource).  Les Voters offrent une granularité fine dans le contrôle d'accès.

### 4.2. Fichiers et Composants Clés

Les fichiers et composants suivants sont essentiels pour la gestion de l'autorisation :

*   **`config/packages/security.yaml`**: Ce fichier définit les règles de sécurité, y compris la gestion des rôles et des permissions, ainsi que les règles d'accès globales.  Il contient notamment la section `access_control` qui permet de définir des règles d'accès basées sur les rôles et les chemins d'URL.

    ```yaml
    # config/packages/security.yaml
    security:
        # ...
        access_control:
            - { path: ^/admin, roles: ROLE_ADMIN } # Seuls les utilisateurs avec le rôle ROLE_ADMIN peuvent accéder aux URLs commençant par /admin
            - { path: ^/profile, roles: ROLE_USER } # Seuls les utilisateurs authentifiés peuvent accéder aux URLs commençant par /profile
            # ... autres configurations de l'accès
    ```

    **Explication :**

    *   `access_control`: Définit les règles d'accès aux URLs.
        *   `path`: Définit le motif d'URL.  Utilisez des expressions régulières pour une flexibilité accrue.
        *   `roles`: Définit les rôles requis pour accéder aux URLs correspondantes.

*   **Entité `User` (`src/Entity/User.php`)**: Contient les rôles attribués à l'utilisateur. Les rôles sont stockés dans un champ ( `roles` dans l'exemple) et sont utilisés pour accorder ou refuser l'accès aux ressources. La gestion des rôles dans l'entité `User` doit être cohérente avec la configuration de `access_control` dans `security.yaml`.

    ```php
    <?php
    // src/Entity/User.php
    namespace App\Entity;

    use Doctrine\ORM\Mapping as ORM;
    use Symfony\Component\Security\Core\User\UserInterface;
    use Symfony\Component\Security\Core\User\PasswordAuthenticatedUserInterface;

    #[ORM\Entity(repositoryClass: UserRepository::class)]
    class User implements UserInterface, PasswordAuthenticatedUserInterface
    {
        // ...
        #[ORM\Column(type: 'json')]
        private array $roles = [];

        public function getRoles(): array
        {
            $roles = array_unique(array_merge($this->roles, ['ROLE_USER'])); // Chaque utilisateur a au moins le rôle ROLE_USER

            return $roles;
        }

        public function setRoles(array $roles): self
        {
            $this->roles = $roles;

            return $this;
        }
    }
    ```

    **Explication :**

    *   `getRoles()`: Retourne un tableau de rôles attribués à l'utilisateur. Il est recommandé d'ajouter `ROLE_USER` par défaut pour simplifier la gestion des rôles.
    *   La gestion des rôles dans l'entité doit être synchronisée avec les configurations `access_control` et les annotations `@IsGranted`.

*   **Voters (si utilisés)**: Des classes spécifiques (ex: `src/Security/ProjectVoter.php`) peuvent être créées pour implémenter une logique d'autorisation personnalisée et complexe. Les Voters permettent de prendre des décisions d'autorisation basées sur des critères plus fins que les simples rôles. Ils sont utilisés pour contrôler l'accès à des entités spécifiques ou à des actions, en tenant compte des relations entre l'utilisateur, les objets et les actions.

    ```php
    <?php
    namespace App\Security;

    use App\Entity\Project;
    use Symfony\Component\Security\Core\Authentication\Token\TokenInterface;
    use Symfony\Component\Security\Core\Authorization\Voter\Voter;
    use Symfony\Component\Security\Core\User\UserInterface;

    class ProjectVoter extends Voter
    {
        const VIEW = 'view';
        const EDIT = 'edit';

        protected function supports(string $attribute, mixed $subject): bool
        {
            // if the attribute isn't one we support, return false
            if (!in_array($attribute, [self::VIEW, self::EDIT])) {
                return false;
            }

            // only vote on `Project` objects
            if (!$subject instanceof Project) {
                return false;
            }

            return true;
        }

        protected function voteOnAttribute(string $attribute, mixed $subject, TokenInterface $token): bool
        {
            $user = $token->getUser();
            // if the user is not logged in; do not grant access
            if (!$user instanceof UserInterface) {
                return false;
            }

            // you can access the project object via $subject
            /** @var Project $project */
            $project = $subject;

            switch ($attribute) {
                case self::VIEW:
                    return $this->canView($project, $user);
                case self::EDIT:
                    return $this->canEdit($project, $user);
            }

            return false;
        }

        private function canView(Project $project, UserInterface $user): bool
        {
            // if they can edit, they can view
            if ($this->canEdit($project, $user)) {
                return true;
            }

            // the project must be public
            if ($project->isPublic()) {
                return true;
            }

            return false;
        }

        private function canEdit(Project $project, UserInterface $user): bool
        {
            // this assumes that the Project object has a method getOwner() which returns the User object
            return $user === $project->getOwner();
        }
    }
    ```

    **Explication du code :**

    *   `supports()` : Définit les attributs et les sujets pour lesquels le voter est pertinent.
    *   `voteOnAttribute()` : Contient la logique d'autorisation. Elle prend en compte l'attribut (l'action à effectuer, ex: 'view', 'edit'), le sujet (l'objet sur lequel l'action est effectuée, ex: un projet), et le token d'authentification (qui contient l'utilisateur).
    *   Les méthodes `canView()` et `canEdit()` contiennent la logique spécifique pour vérifier si l'utilisateur a le droit de voir ou d'éditer le projet. Les Voters doivent être enregistrés en tant que services pour être utilisés.

### 4.3. Processus d'Autorisation

Le processus d'autorisation se déroule généralement comme suit :

1.  **Accès à une Ressource**: L'utilisateur authentifié essaie d'accéder à une ressource ou d'effectuer une action.
2.  **Vérification des Permissions**: Le système vérifie si l'utilisateur a les permissions nécessaires pour accéder à la ressource. Cela se fait en combinant les rôles, les Voters, et les annotations `@IsGranted`.
    *   **Rôles**: Si la ressource est protégée par un rôle (défini dans `access_control`), le système vérifie si l'utilisateur a ce rôle. Cette vérification se fait automatiquement grâce à la configuration de Symfony.
    *   **Voters (si utilisés)**: Si un Voter est associé à la ressource, le système appelle le Voter approprié pour évaluer des conditions plus complexes. Le Voter prend des décisions basées sur des attributs et des sujets, et utilise l'utilisateur courant pour prendre ces décisions.
    *   **Annotations `@IsGranted`**: Les annotations `@IsGranted` (utilisées dans les contrôleurs) permettent de vérifier si l'utilisateur courant a les permissions requises. Elles peuvent être combinées avec les rôles et les Voters.
3.  **Décision**: Le système autorise ou refuse l'accès en fonction des résultats de la vérification. Si l'autorisation est refusée, une exception est généralement levée (par exemple, `AccessDeniedException`), et l'utilisateur est redirigé vers une page d'erreur ou de connexion.

## 5. Protection contre les attaques courantes

WacitV2 intègre des mesures de sécurité robustes pour se protéger contre les attaques courantes, assurant ainsi la sécurité et l'intégrité de l'application et des données.

### 5.1. Protection contre XSS (Cross-Site Scripting)

*   **Échappement des données**: Symfony et Twig (le moteur de template par défaut de Symfony) échappent automatiquement les données affichées dans les templates. Cela empêche l'exécution de code JavaScript malveillant injecté via les données utilisateur. L'échappement est effectué par défaut pour tous les affichages de variables, utilisant le contexte approprié (HTML, JavaScript, URL, etc.).
*   **Utilisation de la politique de sécurité du contenu (CSP)**: Mise en œuvre de politiques de sécurité du contenu (CSP) pour contrôler les ressources (scripts, feuilles de style, images, etc.) que le navigateur est autorisé à charger. Le CSP aide à prévenir les attaques XSS en limitant les sources de contenu autorisées. La configuration du CSP doit être gérée de manière stricte dans les en-têtes HTTP et dans les balises `<meta>` pour maximiser la protection.
*   **Validation et assainissement des entrées**: Les entrées utilisateur doivent être validées et assainies pour empêcher l'injection de code malveillant.

### 5.2. Protection contre CSRF (Cross-Site Request Forgery)

*   **Jetons CSRF**: Symfony utilise des jetons CSRF dans les formulaires pour empêcher les attaques CSRF. Les formulaires incluent un champ caché (`_token`) contenant un jeton unique généré pour la session de l'utilisateur.
*   **Vérification des jetons**: Le backend vérifie la validité du jeton CSRF lors de la soumission des formulaires. Cette vérification est automatique dans Symfony si le jeton est inclus dans le formulaire.
*   **Utilisation de la méthode POST pour les formulaires**: L'utilisation de la méthode POST pour les formulaires qui modifient les données aide à prévenir les attaques CSRF.

### 5.3. Protection contre l'injection SQL

*   **Doctrine (ORM)**: L'utilisation de Doctrine comme ORM aide à prévenir l'injection SQL en utilisant des requêtes préparées et en échappant automatiquement les données. Doctrine utilise des requêtes paramétrées pour éviter l'injection de code SQL malveillant.
*   **Validation des données**: Validation rigoureuse des entrées utilisateur pour s'assurer qu'elles correspondent au format attendu. Cela inclut la validation du type de données, de la longueur, du format, et de la plage de valeurs. La validation est effectuée côté serveur avant de traiter les données.
*   **Utilisation des requêtes préparées**: Lorsque vous devez écrire du SQL manuellement (ce qui est généralement déconseillé), utilisez toujours des requêtes préparées pour éviter l'injection SQL.

### 5.4. Autres Mesures

*   **Mots de passe sécurisés**:
    *   Les mots de passe sont hachés et salés. L'algorithme de hachage recommandé par Symfony est utilisé par défaut (Argon2i).
    *   Il est recommandé d'utiliser des algorithmes de hachage robustes (par exemple, Argon2) et de configurer un nombre suffisant d'itérations pour augmenter la résistance aux attaques par force brute.
    *   Mettre en place des politiques de complexité de mots de passe et encourager l'utilisation de gestionnaires de mots de passe.
*   **Mise à jour des dépendances**: Maintenir les dépendances (packages et librairies) à jour pour corriger les failles de sécurité connues. Les mises à jour de sécurité doivent être appliquées rapidement. Utiliser des outils d'analyse de vulnérabilités (ex: Snyk, Dependabot) pour identifier et gérer les vulnérabilités potentielles.
*   **Journalisation et surveillance**: Journaliser les événements de sécurité (tentatives de connexion, accès non autorisés, etc.) et surveiller l'activité suspecte. Cela permet de détecter et de réagir aux incidents de sécurité. La journalisation doit inclure des informations détaillées, telles que l'adresse IP de l'utilisateur, le type de requête, et les éventuelles erreurs.
*   **Validation des entrées**: Valider toutes les entrées utilisateurs, y compris les valeurs des formulaires, les paramètres des requêtes et les données provenant d'autres sources. La validation doit être effectuée côté serveur et côté client (avec une validation client non-fiable).
*   **Protection de la session**: Utilisation de cookies sécurisés (Secure, HttpOnly) pour la gestion des sessions. Cela protège les cookies contre les attaques de type cross-site scripting (XSS) et garantit qu'ils ne sont transmis que via HTTPS. Implémenter des stratégies de renouvellement de session et de révocation de session pour réduire le risque d'attaques basées sur les sessions.
*   **Gestion des erreurs**: Ne pas afficher d'informations sensibles dans les messages d'erreur. Les messages d'erreur doivent être génériques et ne pas révéler de détails sur la structure interne de l'application ou les informations de configuration.
*   **Protection contre les attaques par force brute**: Implémenter des mécanismes pour limiter le nombre de tentatives de connexion, comme le verrouillage de compte après plusieurs tentatives infructueuses et l'utilisation de CAPTCHA.

## 6. Bonnes pratiques et recommandations

*   **Suivre les principes de sécurité par défaut**: Appliquer les meilleures pratiques de sécurité dès la conception de l'application. Cela inclut l'utilisation de frameworks et de librairies sécurisés, la validation des entrées, l'échappement des sorties, et l'adoption d'une approche de "sécurité dès la conception".
*   **Effectuer des tests de sécurité réguliers**: Réaliser des tests de pénétration et des audits de code pour identifier et corriger les vulnérabilités. Les tests doivent être effectués régulièrement tout au long du cycle de vie de l'application, en utilisant des outils d'analyse statique de code et des tests dynamiques.
*   **Former les développeurs**: Former les développeurs aux pratiques de codage sécurisé et aux menaces de sécurité courantes. La formation doit être continue et adaptée aux nouvelles menaces. Inclure des sessions de sensibilisation à la sécurité dans les processus de développement.
*   **Mettre à jour la documentation**: Mettre régulièrement à jour cette documentation pour refléter les changements dans les mesures de sécurité et les nouvelles recommandations. La documentation doit être claire, concise et à jour.
*   **Gestion des secrets**: Ne jamais stocker de secrets (mots de passe, clés API, etc.) en clair dans le code source. Utiliser des variables d'environnement, un gestionnaire de secrets (par exemple, le composant Symfony Dotenv) ou un service de gestion de secrets (par exemple, HashiCorp Vault).
*   **Gestion des accès aux données sensibles**: Appliquer le principe du moindre privilège (PoLP) pour accorder uniquement les droits d'accès nécessaires aux utilisateurs et aux services. Examiner régulièrement les droits d'accès pour s'assurer qu'ils sont toujours appropriés.
*   **Surveillance continue**: Mettre en place une surveillance continue de l'application et de son infrastructure, en surveillant les journaux, les métriques et les alertes pour détecter les anomalies et les incidents de sécurité.

## 7. Fichiers et composants spécifiques à la Sécurité (Récapitulatif)

*   `config/packages/security.yaml`: Configuration principale de la sécurité, incluant les *firewalls*, les *providers*, les *password hashers* et les règles d'accès.
*   `src/Security/AppCustomAuthenticator.php`: Authentificateur personnalisé (si utilisé), pour gérer l'authentification spécifique à l'application.
*   `src/Entity/User.php`: Entité utilisateur avec les rôles, le mot de passe haché, et l'identifiant.
*   `src/Security/Voter/*.php`: Classes de Voter pour une autorisation fine (si utilisées), pour implémenter une logique d'autorisation personnalisée.
*   Les contrôleurs utilisent les annotations `@Route` pour définir les routes et, si nécessaire, les restrictions d'accès (ex: `@IsGranted`), ainsi que des mécanismes de validation des données.

## 8. Guide d'installation et de configuration

### 8.1. Prérequis

*   PHP 8.1 ou supérieur
*   Composer (gestionnaire de dépendances PHP)
*   Base de données (ex: MySQL, PostgreSQL, SQLite) - Les informations de connexion sont configurées dans le fichier `.env`.
*   Serveur web (ex: Apache, Nginx) - Configurer le serveur web pour servir l'application depuis le répertoire `public`.
*   Node.js et npm (si l'application utilise des dépendances front-end)

### 8.2. Installation

1.  **Cloner le dépôt** : `git clone <url_du_dépôt>`
2.  **Installer les dépendances PHP** : `composer install`
3.  **Installer les dépendances front-end (si nécessaire)**: `npm install` ou `yarn install` (si un fichier `package.json` est présent)
4.  **Configurer la base de données** : Modifier le fichier `.env` à la racine du projet et configurer la variable `DATABASE_URL` avec les informations de connexion à votre base de données.

    ```
    DATABASE_URL="mysql://db_user:db_password@127.0.0.1:3306/db_name?serverVersion=8.0&charset=utf8mb4"
    ```

    *   Remplacez `db_user`, `db_password`, `127.0.0.1:3306` et `db_name` par les valeurs appropriées pour votre configuration de base de données.
    *   `?serverVersion=8.0&charset=utf8mb4` est une configuration courante pour MySQL. Adaptez-la en fonction de votre base de données.
5.  **Créer la base de données et migrer les schémas** :

    ```bash
    php bin/console doctrine:database:create # Crée la base de données (si elle n'existe pas)
    php bin/console doctrine:migrations:migrate # Applique les migrations pour créer/mettre à jour les tables dans la base de données
    ```

6.  **Compiler les assets front-end (si nécessaire)**: `npm run build` ou `yarn build` (si un fichier `webpack.config.js` est présent)
7.  **Créer un utilisateur admin (si nécessaire)**: Utilisez une commande console personnalisée ou une commande de Doctrine pour créer un utilisateur avec le rôle `ROLE_ADMIN`. Consultez la documentation de l'application pour les instructions spécifiques à la création

---

# FAQ

---

```wiki
== Foire aux Questions (FAQ) - WacitV2 ==

=== Introduction ===

Cette section de la documentation a pour objectif de répondre aux questions fréquemment posées (FAQ) concernant le projet WacitV2. Elle est conçue comme une ressource essentielle pour les développeurs, les testeurs et les nouveaux contributeurs au projet. Avant de poser vos questions sur les canaux de communication prévus, nous vous encourageons vivement à consulter cette FAQ.

=== Généralités ===

==== Qu'est-ce que WacitV2 ? ====

*   WacitV2 est une application web de gestion d'entreprise, développée en utilisant le framework Symfony et d'autres technologies modernes. Elle est conçue pour gérer efficacement plusieurs aspects clés de la gestion d'entreprise. Pour une description plus détaillée du projet, veuillez consulter la section [Description du Projet]([lien vers la section Description du Projet]). Les principales fonctionnalités incluent :

    *   Gestion des astreintes
    *   Gestion des primes
    *   Gestion des projets
    *   Gestion des dépenses
    *   Gestion des collaborateurs et des utilisateurs

==== Comment puis-je contribuer au projet ? ====

*   Nous accueillons favorablement les contributions au projet WacitV2. Pour contribuer, veuillez suivre ces étapes :

    1.  **Consultation du Guide de Contribution :** Consultez attentivement le [Guide de Contribution]([lien vers le Guide de Contribution]) pour connaître les étapes détaillées, les bonnes pratiques et les conventions de contribution. Ce guide est votre ressource de référence pour comprendre le processus de contribution.
    2.  **Respect des Conventions de Codage :** Assurez-vous de respecter scrupuleusement les [Conventions de Codage]([lien vers les Conventions de Codage]) établies. Le respect de ces conventions est crucial pour garantir la cohérence, la lisibilité et la maintenabilité du code source.
    3.  **Soumission des Contributions via Pull Requests :** Toutes les contributions doivent être soumises via des *pull requests* (PR) sur le dépôt Git du projet. Les *pull requests* permettent de réviser, de discuter et de fusionner le code de manière contrôlée.
    4.  **Tests Unitaires et Fonctionnels Obligatoires :** Les tests unitaires et fonctionnels sont *obligatoires* pour toutes les contributions. Vos contributions ne seront pas intégrées si elles ne sont pas accompagnées de tests adéquats. Les tests garantissent la qualité et la stabilité du code.

=== Installation et Configuration ===

==== Comment configurer l'environnement de développement ? ====

*   L'environnement de développement de WacitV2 est basé sur Docker pour garantir la reproductibilité, la cohérence et la facilité de configuration. Voici les étapes détaillées à suivre :

    1.  **Prérequis :** Assurez-vous d'avoir Docker et Docker Compose installés sur votre système. Vous pouvez télécharger et installer ces outils en suivant les instructions officielles de Docker, disponibles à l'adresse suivante : [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/).
    2.  **Clonage du Dépôt :** Clonez le dépôt Git du projet WacitV2 sur votre machine locale en utilisant la commande `git clone [URL du dépôt]`.
    3.  **Configuration du fichier `.env` :**

        *   Copiez le fichier `.env.dist` et renommez-le en `.env`.  Le fichier `.env` contiendra les variables d'environnement spécifiques à votre configuration locale.
        *   Modifiez les variables d'environnement dans le fichier `.env` pour correspondre à votre configuration locale. Les variables les plus importantes à configurer incluent :

            *   `DATABASE_URL` :  Cette variable est *cruciale* et contient les informations de connexion à la base de données (par exemple, `DATABASE_URL=mysql://user:password@host:port/database_name`).  Remplacez les valeurs par défaut par les informations appropriées pour votre environnement de développement. Assurez-vous que la base de données existe ou que le conteneur Docker peut la créer.
            *   `APP_ENV` :  Définit l'environnement de l'application (par défaut, `dev` pour le développement).
            *   `APP_DEBUG` : Active ou désactive le mode de débogage (définissez sur `1` pour activer le débogage en développement). *N'activez pas `APP_DEBUG=1` en production.*
    4.  **Lancement des Conteneurs :**  Dans le répertoire racine du projet, exécutez la commande `docker-compose up -d`.  Cette commande construira, si nécessaire, et démarrera les conteneurs définis dans le fichier `docker-compose.yml`. L'option `-d` permet de lancer les conteneurs en arrière-plan (mode détaché).
    5.  **Accès à l'Application :** Une fois les conteneurs lancés, vous pouvez accéder à l'application via l'URL configurée dans votre fichier `.env`.  Généralement, l'application est accessible à l'adresse `http://localhost`. Si vous avez configuré une autre adresse dans votre fichier `.env` (par exemple, en utilisant un nom de domaine), utilisez cette adresse à la place.
    6.  **Initialisation de la Base de Données et Exécution des Migrations :** Si c'est la première fois que vous lancez l'application ou après toute modification du modèle de données, vous devrez exécuter les migrations de la base de données. Reportez-vous à la section "Comment puis-je exécuter les migrations Doctrine ?" ci-dessous. Vous devrez également créer les schémas de la base de données si elle n'existe pas.

*   Pour des instructions plus détaillées, des informations de dépannage et des configurations avancées, veuillez consulter le [Guide d'Installation]([lien vers le Guide d'Installation]).

==== Où puis-je trouver les fichiers de configuration ? ====

*   Les fichiers de configuration de l'application Symfony se trouvent principalement dans le répertoire `config/`. Voici une description des principaux sous-répertoires et fichiers :

    *   `config/packages/` : Ce répertoire contient les fichiers de configuration spécifiques aux bundles et aux packages installés dans le projet. Vous y trouverez, entre autres, la configuration de Doctrine, de Monolog (logging), de sécurité, et d'autres bibliothèques.
    *   `config/routes/` : Ce répertoire contient les fichiers de définition des routes de l'application. C'est ici que vous définissez les URLs accessibles et les contrôleurs associés, ainsi que les méthodes HTTP associées (GET, POST, etc.).
    *   `.env` : Ce fichier contient les variables d'environnement spécifiques à votre installation (par exemple, les informations de connexion à la base de données, le mode de débogage, etc.). Il est *crucial* de ne *jamais* commiter ce fichier dans le dépôt Git. Il contient des informations sensibles.
    *   `.env.dist` : Ce fichier sert de modèle pour le fichier `.env`. Il contient les valeurs par défaut des variables d'environnement et doit être commité dans le dépôt Git.
    *   `config/services.yaml` : Ce fichier définit les services de l'application. Les services sont des objets réutilisables et configurables qui peuvent être injectés dans d'autres classes. Il permet de configurer le conteneur de services de Symfony.

==== Comment puis-je installer les dépendances ? ====

*   Les dépendances du projet sont gérées par Composer, le gestionnaire de dépendances de PHP. Pour installer les dépendances, suivez ces étapes :

    1.  **Accédez au Conteneur PHP :** Ouvrez un terminal et accédez au conteneur PHP. Pour ce faire, utilisez la commande `docker-compose exec php bash` dans le répertoire racine du projet.
    2.  **Exécutez Composer :** Dans le conteneur PHP, exécutez la commande `composer install`. Cette commande installera toutes les dépendances listées dans les fichiers `composer.json` et `composer.lock`. Elle télécharge également les fichiers de classes et les place dans le dossier `vendor`.
    3.  **Mise à Jour des Dépendances :** Si vous avez modifié le fichier `composer.json`, vous devrez exécuter `composer update` au lieu de `composer install` pour mettre à jour les dépendances et générer le nouveau fichier `composer.lock`. Cette commande mettra à jour les versions des librairies.

==== Comment puis-je exécuter les migrations Doctrine ? ====

*   Les migrations Doctrine sont utilisées pour gérer les modifications de la base de données de manière structurée et contrôlée. Pour exécuter les migrations, suivez ces étapes :

    1.  **Accédez au Conteneur PHP :** Comme pour l'installation des dépendances, vous devez d'abord accéder au conteneur PHP en utilisant la commande `docker-compose exec php bash` dans le répertoire racine du projet.
    2.  **Exécuter les Migrations :** Dans le conteneur PHP, exécutez la commande `php bin/console doctrine:migrations:migrate`. Cette commande appliquera toutes les migrations disponibles qui n'ont pas encore été exécutées.
    3.  **Créer une Nouvelle Migration :** Pour créer une nouvelle migration (par exemple, après avoir modifié vos entités), exécutez la commande `php bin/console make:migration`. Cette commande générera un nouveau fichier de migration dans le répertoire `migrations/`.
    4.  **Modifier la Migration :** Ouvrez le fichier de migration généré et modifiez les méthodes `up()` et `down()` pour effectuer les changements nécessaires dans la base de données (par exemple, création de tables, ajout de colonnes, modification des relations, etc.). La méthode `up()` définit les changements à effectuer (ajout, modification), tandis que la méthode `down()` définit comment annuler ces changements (suppression, restauration).
    5.  **Exécuter la Migration :** Une fois la migration modifiée, exécutez à nouveau la commande `php bin/console doctrine:migrations:migrate` pour appliquer les changements.

=== Développement et Tests ===

==== Comment puis-je exécuter les tests unitaires ? ====

*   Les tests unitaires sont essentiels pour assurer la qualité, la fiabilité et la stabilité du code. WacitV2 utilise PHPUnit pour les tests unitaires. Voici comment les exécuter :

    1.  **Accédez au Conteneur PHP :** Utilisez la commande `docker-compose exec php bash` pour accéder au conteneur PHP.
    2.  **Exécuter les Tests :** Dans le conteneur PHP, exécutez la commande `php bin/phpunit` depuis le répertoire racine du projet. Cette commande exécutera tous les tests unitaires trouvés dans le répertoire `tests/`.
    3.  **Emplacement des Tests :** Les fichiers de test se trouvent généralement dans le répertoire `tests/`. L'arborescence des tests doit refléter l'arborescence des classes testées (par exemple, `tests/Controller/MonControleurTest.php` pour tester la classe `src/Controller/MonControleur.php`).
    4.  **Fichiers de Configuration des Tests :** Le fichier `phpunit.xml.dist` contient la configuration de PHPUnit, incluant, entre autres, les paramètres de connexion à la base de données de test. Si vous devez configurer des paramètres spécifiques pour les tests, vous pouvez créer un fichier `phpunit.xml` dans le répertoire racine du projet et y surcharger les configurations de `phpunit.xml.dist`. Assurez-vous de configurer correctement la base de données de test pour éviter d'affecter les données de développement.

==== Comment puis-je déboguer l'application ? ====

*   Le débogage est une composante essentielle du processus de développement. WacitV2 est compatible avec Xdebug, un puissant outil de débogage pour PHP. Voici comment déboguer l'application :

    1.  **Configuration de Xdebug :**
        *   **Vérifiez l'Installation et la Configuration de Xdebug :** Assurez-vous que Xdebug est correctement installé et configuré dans le conteneur PHP. La configuration Xdebug est généralement définie dans le fichier `docker-compose.yml` (ou via des variables d'environnement). Vérifiez les paramètres suivants :
            *   `xdebug.mode`:  Ce paramètre doit être configuré sur `develop`, `debug` ou `coverage` (pour activer le débogage).  `debug` est le mode le plus courant pour le débogage.
            *   `xdebug.idekey`:  Ce paramètre identifie l'IDE utilisé.  La valeur doit correspondre à la configuration de votre IDE (par exemple, `PHPSTORM` pour PhpStorm).
            *   `xdebug.client_host` :  L'adresse IP de votre machine hôte.  Assurez-vous que cette adresse est correcte et que le conteneur PHP peut y accéder.
            *   `xdebug.client_port` :  Le port utilisé par votre IDE pour écouter les connexions de Xdebug (généralement 9003). Assurez-vous que ce port est ouvert sur votre machine hôte.
    2.  **Configuration de l'IDE :** Configurez votre IDE (par exemple, PhpStorm, VS Code) pour utiliser Xdebug. Vous devrez spécifier l'adresse IP et le port du conteneur PHP, ainsi que le port de débogage.  Consultez la documentation de votre IDE pour obtenir des instructions spécifiques.
    3.  **Points d'Arrêt (Breakpoints) :** Définissez des points d'arrêt (breakpoints) dans votre code dans votre IDE. Ces points d'arrêt indiqueront à Xdebug où arrêter l'exécution du code afin que vous puissiez inspecter les variables, le flux d'exécution et l'état de l'application.
    4.  **Déclenchement du Débogage :** Démarrez l'application et accédez à l'endroit du code où vous avez défini un point d'arrêt. L'IDE devrait s'arrêter au point d'arrêt, vous permettant d'examiner l'état de l'application, d'évaluer des expressions, de parcourir le code pas à pas et de diagnostiquer les problèmes.  Vous pouvez utiliser les contrôles de l'IDE pour avancer dans le code, inspecter les variables, etc.

==== Comment puis-je utiliser les commandes console Symfony ? ====

*   Symfony fournit un ensemble de commandes console puissantes et utiles pour diverses tâches, telles que la génération de code, la gestion de la base de données, le nettoyage du cache, l'exécution de tâches planifiées, etc.

    *   **Localisation des Commandes :** Les commandes console Symfony se trouvent dans le répertoire `src/Command/` et peuvent être exécutées de plusieurs manières :
        *   **Exécution Simple :** `php bin/console <nom_de_la_commande>`. Remplacez `<nom_de_la_commande>` par le nom complet de la commande (par exemple, `app:encrypt-user-data`).
        *   **Exécution avec Options et Arguments :** Vous pouvez également passer des options et des arguments aux commandes en les ajoutant à la ligne de commande. Consultez la documentation de chaque commande pour connaître les options disponibles. Utilisez l'option `--help` pour obtenir de l'aide sur une commande spécifique (par exemple, `php bin/console app:encrypt-user-data --help`).
    *   **Exemple :** `php bin/console app:encrypt-user-data` - Cette commande pourrait être utilisée pour chiffrer des données utilisateur. L'exemple est purement illustratif et dépend de la commande spécifique définie dans l'application.
    *   **Découverte des Commandes :** Pour lister toutes les commandes disponibles et leurs descriptions, utilisez `php bin/console list`.  Cela vous permet de découvrir les commandes disponibles et de comprendre leur objectif.
    *   **Personnalisation des Commandes :**  Vous pouvez créer vos propres commandes personnalisées en étendant la classe `Symfony\Component\Console\Command\Command`.  Cela vous permet d'automatiser des tâches spécifiques à votre application.

==== Comment puis-je accéder aux logs ? ====

*   Les logs sont essentiels pour le débogage, la surveillance et l'analyse des problèmes de l'application. Ils fournissent des informations détaillées sur les événements qui se produisent. Les logs sont généralement stockés dans le répertoire `var/log/`.

    *   **Fichiers de Logs Principaux :**
        *   `var/log/dev.log` : Ce fichier contient les logs de l'environnement de développement. Il est utile pour identifier les erreurs, les exceptions, les messages de débogage et les problèmes qui surviennent pendant le développement.
        *   `var/log/prod.log` : Ce fichier contient les logs de l'environnement de production. Il est utilisé pour surveiller l'application en production, pour diagnostiquer les problèmes qui pourraient survenir et pour analyser les performances.
    *   **Configuration du Logging :** La configuration du logging (par exemple, le niveau de verbosité, les canaux, les formats des logs) se trouve dans le fichier `config/packages/monolog.yaml`. Vous pouvez modifier ce fichier pour adapter la configuration du logging à vos besoins (par exemple, pour ajouter des canaux spécifiques, pour modifier le format des logs ou pour filtrer les messages).
    *   **Accès aux Logs :** Pour consulter les logs, vous pouvez soit accéder directement aux fichiers de logs (par exemple, en utilisant la commande `cat` dans le conteneur PHP), soit utiliser un outil de visualisation de logs. Les outils de visualisation de logs peuvent faciliter la recherche, le filtrage et l'analyse des logs. Des outils comme Graylog, ELK Stack (Elasticsearch, Logstash, Kibana) ou Splunk sont des solutions courantes pour la gestion des logs en production.

=== Problèmes et Solutions ===

==== J'ai des problèmes avec la base de données. Comment puis-je les résoudre ? ====

*   Les problèmes de base de données sont fréquents et peuvent être dus à diverses causes. Voici quelques étapes pour les diagnostiquer et les résoudre :

    1.  **Vérifiez la Configuration `.env` :**
        *   Assurez-vous que la variable `DATABASE_URL` dans le fichier `.env` est correctement configurée avec les informations de connexion à la base de données (hôte, port, nom de la base de données, nom d'utilisateur, mot de passe). Vérifiez que les informations sont correctes et correspondent à votre configuration de base de données. Une erreur de frappe ou une mauvaise configuration est une cause fréquente d'erreur.
    2.  **Vérifiez l'État de la Base de Données :**
        *   Assurez-vous que le service de base de données est en cours d'exécution. Vous pouvez vérifier l'état du service de base de données en utilisant la commande `docker ps`. Cette commande affichera une liste des conteneurs en cours d'exécution. Recherchez le conteneur de base de données (par exemple, `mysql` ou `postgres`). Si le conteneur de base de données n'est pas en cours d'exécution, vous devrez le démarrer en utilisant la commande `docker-compose up -d`.
    3.  **Exécutez les Migrations :**
        *   Assurez-vous que les migrations Doctrine ont été exécutées après chaque modification du modèle de données. Exécutez la commande `php bin/console doctrine:migrations:migrate` pour appliquer les migrations et synchroniser le schéma de la base de données avec le code.
    4.  **Vérifiez les Logs :**
        *   Consultez les logs de l'application (`var/log/dev.log` en développement, `var/log/prod.log` en production) et les logs de la base de données (si disponibles) pour obtenir des informations sur les erreurs potentielles. Les logs peuvent fournir des indications précises sur la cause des problèmes. Les erreurs de connexion à la base de données, les erreurs de requête SQL et les contraintes de clés étrangères non respectées sont souvent enregistrées dans les logs.
    5.  **Vérifiez les Permissions :**
        *   Assurez-vous que l'utilisateur de la base de données (configuré dans `DATABASE_URL`) dispose des permissions nécessaires pour accéder à la base de données et effectuer les opérations requises (création, lecture, modification, suppression de données). Les erreurs de permissions peuvent empêcher l'accès à la base de données. Vérifiez également si la base de données existe.
    6.  **Vérification de la Connexion avec un Client de Base de Données :**
        *   Si possible, connectez-vous directement à la base de données en utilisant un client de base de données (par exemple, MySQL Workbench, pgAdmin) pour vérifier si vous pouvez accéder à la base de données avec les mêmes informations d'identification et pour diagnostiquer les problèmes de connexion.

==== L'application affiche une erreur 500. Que dois-je faire ? ====

*   Une erreur 500 (Internal Server Error) indique généralement un problème interne au serveur, ce qui signifie que l'application a rencontré une erreur inattendue et n'a pas pu traiter la requête. Voici les étapes à suivre pour diagnostiquer et résoudre ce type d'erreur :

    1.  **Activez le Mode de Débogage (Développement Uniquement) :**
        *   Dans le fichier `.env`, définissez la variable `APP_DEBUG=1`. Cela permettra d'afficher les informations de débogage détaillées, telles que les traces d'erreurs, directement dans le navigateur. *N'activez pas `APP_DEBUG=1` en production.*
    2.  **Consultez les Logs :**
        *   Consultez les logs de l'application (`var/log/dev.log` en développement, `var/log/prod.log` en production) pour identifier la cause de l'erreur. Les logs contiennent souvent des informations précieuses sur le problème, telles que le nom de la classe, le nom de la méthode, et la ligne de code où l'erreur s'est produite. Recherchez les exceptions, les erreurs de PHP et les messages d'erreur.
    3.  **Examinez le Code :**
        *   Examinez le code concerné pour trouver des erreurs potentielles. Utilisez les informations des logs et des traces d'erreurs (si `APP_DEBUG=1` est activé) pour localiser le code fautif.
        *   Utilisez votre IDE et Xdebug pour déboguer le code, examiner les variables, le flux d'exécution et l'état de l'application. Les points d'arrêt peuvent vous aider à identifier le problème.
    4.  **Vérifiez la Configuration :**
        *   Vérifiez que la configuration de l'application est correcte. Vérifiez la configuration des services, des routes, des paramètres, des fichiers de configuration, etc. Assurez-vous que tous les fichiers de configuration sont correctement configurés et qu'il n'y a pas d'erreurs de syntaxe.
    5.  **Effacez le Cache :**
        *   Effacez le cache de l'application en exécutant la commande `php bin/console cache:clear`. Cela peut résoudre les problèmes liés aux fichiers de cache corrompus ou obsolètes.
    6.  **Vérifiez la Configuration du Serveur Web (si applicable):**
        *   Si vous utilisez un serveur web (par exemple, Apache, Nginx), vérifiez sa configuration pour vous assurer qu'il est correctement configuré et qu'il ne rencontre pas de problèmes (par exemple, erreurs de permission, problèmes de configuration du virtual host).

==== Comment puis-je effacer le cache Symfony ? ====

*   Le cache Symfony peut parfois causer des problèmes, en particulier après des modifications de code ou de configuration. Effacer le cache est une opération courante pour résoudre ces problèmes. Voici comment effacer le cache :

    *   **Effacer le Cache (Environnement de Développement) :** Exécutez la commande `php bin/console cache:clear` pour effacer le cache de développement. C'est la commande la plus couramment utilisée pendant le développement. Elle efface le cache généré pour l'environnement `dev`.
    *   **Effacer le Cache pour un Environnement Spécifique :** Exécutez la commande `php bin/console cache:clear --env=<environnement>` pour effacer le cache d'un environnement spécifique. Remplacez `<environnement>` par le nom de l'environnement (par exemple, `prod` pour la production, `test` pour les tests). Cette commande est utile pour effacer le cache d'un environnement spécifique sans affecter les autres environnements.  Par exemple, `php bin/console cache:clear --env=prod` effacera le cache de production.

=== Autres Questions ===

==== Comment puis-je exporter des données ? ====

*   L'application WacitV2 fournit des fonctionnalités d'exportation de données dans différents formats.

    *   **Contrôleur d'Export :** Les fonctionnalités d'exportation sont gérées par le contrôleur `ExportController.php`.
    *   **Templates d'Export :** Les templates d'export sont stockés dans le répertoire `public/templates/`. Ces templates sont utilisés pour formater les données exportées dans les différents formats.
    *   **Formats d'Export Supportés :** Les formats d'export supportés incluent :
        *   CSV (valeurs séparées par des virgules)
        *   Excel (format `.xlsx`)
        *   PDF (potentiellement)
        *   D'autres formats pourraient être pris en charge à l'avenir.
    *   **Configuration des Exports :** Les exports sont générés à partir des données des entités Doctrine et sont paramétrables via l'interface d'administration. Vous pouvez configurer les colonnes à exporter, le format des données, les filtres, etc. Consultez la documentation de l'interface d'administration pour plus d'informations sur la configuration des exports.

==== Comment puis-je gérer les utilisateurs et les permissions ? ====

*   WacitV2 propose un système de gestion des utilisateurs et des permissions pour contrôler l'accès aux différentes fonctionnalités de l'application.

    *   **Interface d'Administration :** Le module de gestion des utilisateurs et des permissions est accessible via l'interface d'administration. Cette interface permet aux administrateurs de gérer les utilisateurs, les rôles et les permissions.
    *   **Code de Sécurité :** Le code gérant la sécurité et l'authentification se trouve dans le répertoire `src/Security/`. Ce répertoire contient les classes et les configurations liées à la sécurité de l'application, telles que les authentificateurs, les fournisseurs d'utilisateurs et les contrôleurs d'accès.
    *   **Gestion des Rôles et Permissions :** Les permissions sont gérées via des rôles. Les rôles définissent les droits d'accès des utilisateurs à des fonctionnalités spécifiques de l'application.
        *   Les rôles sont généralement définis dans les entités `Permission.php` et `User.php`.
    *   **Authentification et Autorisation :** L'accès aux fonctionnalités est contrôlé via des mécanismes d'authentification (vérification de l'identité de l'utilisateur) et d'autorisation (vérification des permissions de l'utilisateur).
        *   L'authentification est gérée par des authentificateurs personnalisés (par exemple, `src/Security/AppCustomAuthenticator.php`) et par la configuration de la sécurité de Symfony.

==== Où puis-je trouver de la documentation sur les API ? ====

*   Les API (Application Programming Interfaces) de WacitV2 sont conçues pour permettre l'interaction avec l'application depuis des clients externes (applications mobiles, autres systèmes, etc.). Les API permettent l'accès aux données et aux fonctionnalités de l'application de manière programmatique.

    *   **Localisation des Définitions des API :** Les définitions des API se trouvent généralement dans les contrôleurs. Les contrôleurs API sont généralement situés dans le répertoire `src/Controller/API/`.
    *   **Documentation des API (Swagger/OpenAPI) :** La documentation des API peut être générée via des outils tels que Swagger/OpenAPI. Si une documentation des API est disponible (par exemple, générée avec Swagger/OpenAPI), veuillez fournir le lien direct vers cette documentation.  Cela permet aux développeurs de comprendre comment utiliser les API et quels sont les endpoints disponibles.
    *   **Routes et Annotations :** Les routes des API sont configurées en utilisant des annotations dans les contrôleurs (par exemple, `@Route`). Les annotations définissent les URLs des endpoints, les méthodes HTTP supportées (GET, POST, PUT, DELETE, etc.), les paramètres et les formats de données (JSON, XML, etc.).

        *   [Lien vers la documentation des API, si disponible] Si une documentation des API est disponible (par exemple, générée avec Swagger/OpenAPI), veuillez fournir le lien direct vers cette documentation.
        *   Si une documentation formelle n'est pas disponible, référez-vous aux contrôleurs API dans le répertoire `src/Controller/API/` pour comprendre comment les endpoints sont définis et documentés.

=== Glossaire ===

*   **ORM** : Object-Relational Mapper. Dans le contexte de WacitV2, l'ORM utilisé est Doctrine. Doctrine permet de mapper les objets PHP aux tables de la base de données, facilitant ainsi la gestion des données et les interactions avec la base de données.
*   **MVC** : Model-View-Controller. Il s'agit d'un pattern architectural largement utilisé pour la conception d'applications web. Dans WacitV2, l'architecture MVC est mise en œuvre par le framework Symfony.
*   **API** : Application Programming Interface. Une API définit un ensemble de règles et de protocoles pour permettre à différentes applications de communiquer entre elles. Dans WacitV2, les API permettent aux applications clientes d'interagir avec les données et les fonctionnalités de l'application.
*   **CI/CD** : Continuous Integration/Continuous Delivery (Intégration et livraison continues). Il s'agit d'une pratique de développement logiciel qui consiste à automatiser l'intégration, les tests et le déploiement du code.
*   **JWT** : JSON Web Token. Un standard pour la création de tokens d'accès utilisés pour l'authentification et l'autorisation dans les applications web.

=== Contact ===

Pour toute question non traitée dans cette FAQ ou pour obtenir de l'aide supplémentaire, veuillez contacter l'équipe de support : [indiquez ici l'équipe de support, l'adresse email, ou le canal de communication]. Veuillez fournir autant de détails que possible concernant votre problème afin de faciliter la résolution de votre requête. Incluez des informations sur l'environnement, les étapes de reproduction du problème, les messages d'erreur rencontrés, etc.
```


---


---

*Fin de la Documentation*
