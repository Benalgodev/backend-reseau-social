# Guide d'Intégration MongoDB Atlas

Ce guide explique comment configurer et intégrer MongoDB Atlas dans votre projet.

---

## Étape 1 : Créer un Compte et Se Connecter

1. Allez sur [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).
2. Créez un nouveau compte ou connectez-vous si vous en avez déjà un.

---

## Étape 2 : Créer un Cluster

1. Une fois connecté, cliquez sur **"Create a New Cluster"**.
2. Sélectionnez un fournisseur cloud (AWS, GCP, Azure) et une région géographique.
3. Choisissez le **Free Tier** pour les besoins de développement.
4. Cliquez sur **"Create Cluster"** et attendez que le processus se termine.

---

## Étape 3 : Configurer l'Accès Réseau

1. Allez dans **"Network Access"** depuis le menu de gauche.
2. Cliquez sur **"Add IP Address"**.
   - Pour autoriser l'accès depuis n'importe où (non recommandé pour la production), entrez `0.0.0.0/0`.
   - Alternativement, ajoutez votre adresse IP spécifique.
3. Cliquez sur **"Confirm"** pour sauvegarder les paramètres.

---

## Étape 4 : Créer un Utilisateur de Base de Données

1. Naviguez vers **"Database Access"** depuis le menu.
2. Cliquez sur **"Add New Database User"**.
3. Entrez un nom d'utilisateur et un mot de passe forts.
4. Sous **"Database User Privileges"**, sélectionnez **"Read and write to any database"**.
5. Cliquez sur **"Add User"** pour créer l'utilisateur de base de données.

---

## Étape 5 : Obtenir la Chaîne de Connexion (URI)

1. Allez dans **"Clusters"** dans le menu.
2. Cliquez sur **"Connect"** à côté de votre cluster.
3. Sélectionnez **"Connect your application"**.
4. Choisissez **"Node.js"** comme driver et la version appropriée.
5. Copiez la chaîne de connexion. Elle devrait ressembler à ceci :
   ```
   mongodb+srv://<username>:<password>@<cluster-address>/<dbname>?retryWrites=true&w=majority
   ```
6. Remplacez les espaces réservés :
   - `<username>` : Votre nom d'utilisateur de base de données.
   - `<password>` : Votre mot de passe de base de données.
   - `<cluster-address>` : L'adresse de votre cluster (ex : `cluster0.mongodb.net`).
   - `<dbname>` : Le nom de votre base de données (si nécessaire).

---

## Étape 6 : Ajouter l'URI à Votre Projet

1. Localisez le fichier de configuration dans votre projet où la chaîne de connexion MongoDB est utilisée.
2. Remplacez la chaîne de connexion d'espace réservé par l'URI que vous avez obtenue à l'étape 5.
3. Utilisez des variables d'environnement pour gérer de manière sécurisée les informations sensibles comme les identifiants, si ce n'est pas déjà implémenté dans le projet.

---

## Notes Additionnelles

- **Sécurité** : Évitez d'utiliser `0.0.0.0/0` dans les environnements de production. Restreignez l'accès aux adresses IP de confiance uniquement.
- **Variables d'Environnement** : Utilisez des variables d'environnement pour stocker les informations sensibles comme les identifiants de base de données.
- **Test** : Testez toujours la connexion localement avant de déployer en production.

---

Vous avez maintenant intégré avec succès MongoDB Atlas dans votre projet !
