# Gestionnaire de Tâches 

## Description du projet
Ce projet est une application fullstack pour la gestion de tâches.  
- **Frontend** : Application React permettant de créer, afficher, modifier, supprimer et filtrer des tâches.  
- **Backend** : API REST en NestJS fournissant les endpoints pour manipuler les tâches stockées dans une base de données MYSQL Wokbench.

---

## Partie Backend

### Choix techniques

- **Node.js avec NestJS** :  
  J’ai utilisé Node.js pour sa simplicité et son intégration facile avec JavaScript côté frontend. NestJS a été privilégié pour sa structure modulaire et ses fonctionnalités avancées, mais Express peut aussi être utilisé pour un backend plus léger.

- **Base de données** :  
  Utilisation d’une base de données relationnelleMySQL pour stocker les tâches.  
  Les tâches ont des champs typiques : id, titre, description, priorité, statut, date de création, etc.

- **Architecture RESTful** :  
  Le backend expose des routes claires :  
  - GET `/api/tasks` : récupérer toutes les tâches  
  - POST `/api/tasks` : créer une nouvelle tâche  
  - PUT `/api/tasks/:id` : modifier une tâche  
  - DELETE `/api/tasks/:id` : supprimer une tâche

### Points rencontrés

- **Gestion des erreurs** :  
  J’ai mis en place un système de gestion des erreurs HTTP (400, 404, 500) avec des messages clairs.

- **Validation des données** :  
  Validation côté backend des champs reçus pour éviter les données invalides.

- **CORS** :  
  Configuration CORS pour autoriser les requêtes depuis le frontend React sur un autre port.

- **Déploiement** :  
  Prévoir un déploiement possible en mode production avec gestion des variables d’environnement.

---

## Partie Frontend

### Choix techniques

- **React avec hooks (useState, useEffect)**  
- **react-toastify pour notifications**  
- **Lucide-react pour les icônes**  
- **Fetch API pour communiquer avec le backend**

### Fonctionnalités

- Liste des tâches avec possibilité de filtre par priorité et statut  
- Recherche textuelle  
- Ajout / modification / suppression des tâches  
- Confirmation avant suppression  
- Gestion des erreurs de communication avec le backend (affichage de messages d’erreur ou fallback)

### Difficultés rencontrées

- Gestion de l’état d’édition inline dans les listes  
- Synchronisation des données avec le backend pour éviter les conflits  
- Gestion des erreurs réseau et affichage d’un fallback

---

## Structure du projet

