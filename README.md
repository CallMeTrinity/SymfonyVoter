Créons un projet Symfony qui met en œuvre le système de Voter pour gérer les autorisations de manière granulaire. Le projet consistera en une application de gestion de projets où les utilisateurs peuvent créer des projets, les assigner à d'autres utilisateurs et gérer des tâches au sein de ces projets.

### Projet : Application de Gestion de Projets

**Objectif** : Permettre aux utilisateurs de créer, visualiser, modifier et supprimer des projets et des tâches, avec des droits d'accès spécifiques basés sur leur rôle dans chaque projet.

#### User Journeys & Tickets

1. **Inscription et Authentification des Utilisateurs**
   - As a user, I want to be able to register an account so that I can login and access the project management features.
   - As a user, I want to be able to login with my credentials to access my projects and tasks.

2. **Création de Projets**
   - As a project owner, I want to create a new project so that I can manage tasks and assignees within this project.
   - As a project owner, I want to assign users to my project so that they can work on the tasks.

3. **Gestion des Projets**
   - As a project owner, I want to edit project details so that I can update its name, description, or assignees.
   - As a project owner, I want to delete a project when it's no longer needed.

4. **Création et Gestion des Tâches**
   - As a project member, I want to create tasks within the project so that I can track the work to be done.
   - As a task owner or a project owner, I want to edit task details so that I can update its description, status, or assignee.
   - As a task owner or a project owner, I want to delete a task when it's completed or no longer needed.

5. **Visualisation des Projets et des Tâches**
   - As a user, I want to view a list of projects I'm part of so that I can select a project to work on.
   - As a project member, I want to view a list of tasks within a project so that I know what work needs to be done.

#### Utilisation des Voters Symfony

Pour chaque action (création, visualisation, modification, suppression de projets ou de tâches), vous allez implémenter un Voter Symfony qui déterminera si l'utilisateur courant a les autorisations nécessaires pour effectuer l'action demandée. Voici quelques exemples d'implémentations des Voters :

- **ProjectVoter**: Vérifie si l'utilisateur peut créer, voir, modifier ou supprimer un projet.
- **TaskVoter**: Vérifie si l'utilisateur peut créer, voir, modifier ou supprimer une tâche au sein d'un projet spécifique.

### Notes Techniques

- Utilisez Symfony Security pour gérer l'authentification et les autorisations.
- Implémentez des Voters pour gérer finement les droits d'accès aux projets et aux tâches en fonction du rôle de l'utilisateur (propriétaire du projet, membre du projet, propriétaire de la tâche).
- Mettez en place une base de données pour stocker les utilisateurs, les projets, les assignations de projets et les tâches.

Ce projet vous permettra de pratiquer l'implémentation du système de Voter de Symfony dans un contexte réaliste, en gérant les droits d'accès complexes dans une application de gestion de projets.
