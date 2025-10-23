# Schéma de Chat

## Aperçu

Ce document décrit la structure du schéma pour une application de chat, incluant les utilisateurs, les messages et les métadonnées.

---

## Structure du Schéma

### 1. Détails du Chat

La racine du schéma de chat contient des informations générales sur la conversation :

```json
{
  "_id": "674decc9d37cf32c762132a9",
  "createdAt": 1733160129863,
  "userId": "630efe0d84ce02c3bd16a9ca",
  "userId2": "630f0c02f70397ad66d5fbdc"
}
```

- **`_id`** : Identifiant unique pour le chat.
- **`createdAt`** : Horodatage de la création du chat.
- **`userId`** : Identifiant du premier utilisateur.
- **`userId2`** : Identifiant du deuxième utilisateur.

---

### 2. Messages

Un tableau des messages échangés dans le chat :

```json
"messages": [
  {
    "_id": "Udd5m7BEYplZNbFwq51CAYYg",
    "txt": "bonjour",
    "userId": "630f0c02f70397ad66d5fbdc",
    "createdAt": 1733160138095
  },
  {
    "_id": "z3gMgS3Tlvcqad5rRBg8WGUa",
    "txt": "salut",
    "userId": "630f0c02f70397ad66d5fbdc",
    "createdAt": 1733247245880
  }
]
```

#### Champs :

- **`_id`** : Identifiant unique pour le message.
- **`txt`** : Contenu du message.
- **`userId`** : Identifiant de l'expéditeur du message.
- **`createdAt`** : Horodatage indiquant quand le message a été envoyé.

---

### 3. Utilisateurs

Un tableau des utilisateurs participant au chat :

```json
"users": [
  "Invité",
  null
]
```

#### Champs :

- **`users[0]`** : Nom ou identifiant du premier utilisateur.
- **`users[1]`** : Nom ou identifiant du deuxième utilisateur (peut être `null` si non spécifié).

---
