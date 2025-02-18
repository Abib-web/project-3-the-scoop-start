# The Scoop
![image](https://github.com/user-attachments/assets/33a4d7c8-39e6-4a4f-9c18-5964df629207)

## Aperçu du projet

Ce projet est une application web permettant la soumission et la gestion d'articles, développée en Node.js et Reacts.js dans le cardre de l'apprentissage codeacademy. 
L'application offre les fonctionnalités suivantes :

- Création et connexion avec un nom d'utilisateur personnalisé
- Soumission, modification et suppression d'articles contenant un lien et une description
- Système de vote (upvote/downvote) pour les articles
- Ajout, modification et suppression de commentaires sur les articles
- Système de vote (upvote/downvote) pour les commentaires
- Consultation des articles et commentaires d'un utilisateur spécifique

L'application repose sur une structure de base de données en mémoire et une API REST pour gérer les interactions entre les utilisateurs et le contenu.

## Fonctionnalités implémentées

### Gestion des utilisateurs
- Création d'un compte utilisateur avec un nom unique
- Authentification par nom d'utilisateur

### Gestion des articles
- Création d'un article avec un lien et une description
- Modification et suppression d'articles existants
- Upvote et downvote des articles

### Gestion des commentaires
- Ajout d'un commentaire sur un article
- Modification et suppression d'un commentaire
- Upvote et downvote des commentaires

## Structure du projet

L'implémentation repose sur deux objets principaux :

### `database`
Un objet JavaScript contenant les données stockées pour les utilisateurs, articles et commentaires. 
Chaque ressource est stockée sous forme d'objet avec un identifiant unique comme clé.

Exemple de structure :
```json
{
  "users": {
    "1": { "username": "JohnDoe" }
  },
  "articles": {
    "1": { "id": 1, "url": "https://exemple.com", "description": "Article exemple" }
  },
  "comments": {
    "1": { "id": 1, "body": "Super article !", "username": "JohnDoe", "articleId": 1 }
  }
}
```

### `routes`
Un objet JavaScript définissant les routes de l'API, associant chaque chemin aux méthodes HTTP correspondantes.

## Installation et exécution

1. Cloner le projet :
   ```sh
   git clone https://github.com/Abib-web/project-3-the-scoop-start.git
   cd project-3-the-scoop-start
   ```
2. Installer les dépendances :
   ```sh
   npm install
   ```
3. Démarrer le serveur :
   ```sh
   node server.js
   ```
4. Ouvrir `index.html` dans un navigateur (Google Chrome recommandé)

## Tests

Une suite de tests a été mise en place pour valider le bon fonctionnement des différentes fonctionnalités.

- Installation des dépendances de test :
  ```sh
  npm install
  ```
- Exécution des tests :
  ```sh
  npm test
  ```

## Améliorations futures

- Sauvegarde et chargement de la base de données en YAML
- Sécurisation de l'authentification des utilisateurs
- Interface utilisateur plus avancée

---

N'hésite pas à proposer des améliorations ou signaler des bugs ! 😊
