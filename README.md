# Projet API Social Media avec Node.js & Express

## Table des Matières

- [README](README.md)
- [Guide d'Intégration MongoDB Atlas](DATABASE.md)
- [Schéma de la Collection Post](POST.md)
- [Schéma de la Collection Chat](CHAT.md)
- [Schéma de la Collection Utilisateur](USER.md)
- [Schéma de la Collection Activité](ACTIVTY.md)

---

## Aperçu

Ce projet est un backend de médias sociaux construit avec Node.js et Express. Il inclut des API RESTful pour la gestion des utilisateurs, des publications, des commentaires et plus encore. Le projet est conçu pour supporter une application de médias sociaux dynamique avec des fonctionnalités backend essentielles telles que l'authentification des utilisateurs, le téléchargement de médias et le contrôle d'accès basé sur les rôles.

---

## Fonctionnalités

- **Authentification Utilisateur** : Inscription, connexion et authentification basée sur JWT.
- **Publications & Commentaires** : Les utilisateurs peuvent créer, lire, mettre à jour et supprimer des publications et des commentaires.
- **Middleware** : Middleware personnalisé pour l'authentification, la gestion des erreurs et la journalisation des requêtes.
- **Journalisation** : Les logs sont maintenus pour les activités du serveur.
- **Modération de Contenu** : Intégration de l'API Google Vision et Cloudinary WebPurify pour détecter et empêcher le téléchargement de contenu inapproprié.
- **Documentation API** : Endpoints d'API bien documentés pour une intégration facile.

---

## Structure du Projet

- `api/` - Contient les définitions des routes pour les utilisateurs, les publications et autres fonctionnalités.
- `config/` - Fichiers de configuration pour les connexions à la base de données et les variables d'environnement.
- `middlewares/` - Logique middleware pour l'authentification, la gestion des erreurs, etc.
- `services/` - Logique métier abstraite en services.
- `data/` - Espace réservé pour les opérations liées aux données.
- `logs/` - Fichiers de logs du serveur.
- `public/` - Assets statiques.
- `server.js` - Le fichier serveur principal pour démarrer l'application Express.

---

## Pour Commencer

1. Cloner le dépôt :

   ```sh
   git clone https://github.com/benalgodev/React-Social-Media-App-.git
   ```

2. Naviguer dans le répertoire du projet :

   ```sh
   cd Social-Network-Backend
   ```

3. Installer les dépendances :
   ```sh
   npm install
   ```

---

## Configuration

- Créer un fichier `.env` dans le répertoire racine et fournir les variables d'environnement suivantes :

  ```env
  DB_URI=votre_uri_mongodb_ici
  REACT_APP_GOOGLE_MAP_KEY=
  TOKEN_SECRET=votre_secret_jwt
  CLOUD_NAME=votre_nom_cloud
  CLOUD_API_KEY=votre_cle_api
  CLOUD_API_SECRET=votre_secret_api
  
  GOOGLE_PRIVATE_KEY=
  GOOGLE_CLIENT_EMAIL=
  GOOGLE_PROJECT_ID=
  ```

---

## Démarrage du Serveur

Pour démarrer le serveur en mode développement :

```sh
npm run dev
```

Pour démarrer le serveur en mode production :

```sh
npm start
```

---

## Endpoints de l'API

### Routes des Activités

- **GET /** - Récupérer toutes les activités
- **POST /** - Ajouter une nouvelle activité
- **PUT /:id** - Mettre à jour une activité par ID
- **GET /length** - Obtenir le nombre d'activités

### Routes d'Authentification

- **POST /login** - Connexion utilisateur
- **POST /signup** - Inscription utilisateur
- **POST /logout** - Déconnexion utilisateur

### Routes de Chat

- **GET /** - Récupérer tous les chats
- **GET /:id** - Récupérer un chat par ID
- **POST /** - Créer un nouveau chat
- **PUT /:id** - Mettre à jour un chat par ID
- **DELETE /:id** - Supprimer un chat par ID

### Routes des Commentaires

- **GET /** - Récupérer tous les commentaires
- **GET /:id** - Récupérer un commentaire par ID
- **POST /** - Ajouter un nouveau commentaire
- **PUT /:id** - Mettre à jour un commentaire par ID
- **DELETE /:id** - Supprimer un commentaire par ID

### Routes des Publications

- **GET /** - Récupérer toutes les publications
- **GET /length** - Récupérer le nombre de publications
- **GET /:id** - Récupérer une publication par ID
- **POST /** - Créer une nouvelle publication
- **PUT /:id** - Mettre à jour une publication par ID
- **DELETE /:id** - Supprimer une publication par ID

### Routes des Utilisateurs

- **GET /** - Récupérer tous les utilisateurs
- **GET /:id** - Récupérer un utilisateur par ID
- **POST /** - Ajouter un nouvel utilisateur
- **PUT /:id** - Mettre à jour un utilisateur par ID
- **DELETE /:id** - Supprimer un utilisateur par ID

---

## Frontend

Le frontend pour ce projet peut être trouvé [ici](https://github.com/benalgodev/React-Social-Media-App-).

---

## Contributions

N'hésitez pas à soumettre des pull requests pour de nouvelles fonctionnalités, des corrections de bugs ou des améliorations. Veuillez vous assurer que tous les tests passent avant de soumettre.

---

