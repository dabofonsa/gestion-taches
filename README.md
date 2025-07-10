# Gestionnaire de Tâches

## Description du projet

Ce projet est une application fullstack pour la gestion de tâches :  
- Frontend : Application React pour créer, modifier, supprimer et afficher des tâches.  
- Backend : API NestJS pour gérer les tâches, connectée à une base de données MySQL (MySQL Workbench) via Prisma.  

L’application permet de manipuler les tâches avec un CRUD complet et une interface utilisateur simple et intuitive.

---

## Installation et mise en place

### Prérequis
- Node.js & npm  
- MySQL 8.0

Cloner le dépôt  et vous aurez le backend et le frontend

### Backend 
1. Installer les dépendances avec `npm install`  
2. Configurer la base de données MySQL selon le fichier `.env` (hôte, utilisateur, mot de passe, nom de la base)  
3. Lancer MySQL localement 
4. Exécuter la migration Prisma avec la commande :  npm prisma migrate dev --name init
5. Démarrer le serveur backend : npm run start


### Frontend
1. Installer les dépendances avec: npm install
2. Démarrer l’application React : npm start



Choix techniques

### Backend
NestJS : Framework Node.js structuré, supportant TypeScript, et idéal pour API REST.
Prisma ORM : Pour gérer les migrations et les requêtes SQL avec MySQL de manière typée et simple.
MySQL 8.0 : Base de données relationnelle stable, facile à utiliser avec Prisma.
Structure modulaire : Organisation claire des modules, contrôleurs, et services pour faciliter la maintenance.
Gestion des erreurs et validation : Validation des données reçues pour sécuriser l’API.
Endpoints REST : CRUD complet pour les tâches, notamment création, édition, suppression, récupération.
Postman: Permet de tester les requetes HTTP CRUD.



### Frontend
React avec hooks pour gérer l’état et les effets (useState, useEffect).
Fetch API pour interagir avec le backend via les endpoints REST.
react-toastify pour afficher des notifications utilisateur (succès, erreurs).
Lucide-react pour une bibliothèque d’icônes moderne et légère.
Gestion de l’édition en ligne, ajout de tâches, suppression via appels API.




Fonctionnalités réalisées:
Récupération, affichage et filtrage des tâches.
Création et édition des tâches côté backend et frontend (implémentées dans les zones @todo).
Suppression des tâches côté frontend, utilisant le point API backend existant.
Notifications pour confirmer les actions utilisateurs.
Ajout de données en base avant démarrage pour faciliter les tests.



Difficultés et points d’attention:
Comprendre la structure NestJS et Prisma pour la gestion des migrations et des modèles.
La synchronisation des données entre frontend et backend, notamment lors de la modification inline.
Configuration CORS entre frontend et backend pour éviter les erreurs de requêtes.
Respecter la consigne d’utiliser uniquement yarn et non npm.


Bonus réalisé
Ajout d’un système de tri par date de création et un filtre par priorité des tâches.
