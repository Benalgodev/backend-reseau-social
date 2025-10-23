# Schéma de la Collection Post

La collection `post` représente les publications de médias sociaux dans la base de données. Voici une explication détaillée de sa structure et de ses champs :

## Structure du Schéma

### Champs

1. **`userId`** (String)
   - L'ID de l'utilisateur qui a créé la publication.

2. **`title`** (String)
   - Le titre de la publication (optionnel).

3. **`body`** (String)
   - Le contenu principal de la publication.

4. **`reactions`** (Tableau d'Objets)
   - Représente les réactions des utilisateurs à la publication.
   - Chaque objet contient :
     - `userId` (String) : L'ID de l'utilisateur qui a réagi.
     - `fullname` (String) : Le nom complet de l'utilisateur qui a réagi.
     - `reaction` (String) : Type de réaction (ex: "like", "j'aime").

5. **`createdAt`** (Number)
   - Horodatage indiquant quand la publication a été créée.

6. **`imgBodyUrl`** (String)
   - URL de l'image jointe à la publication (optionnel).

7. **`shares`** (Array)
   - Liste des IDs des utilisateurs qui ont partagé la publication.

8. **`comments`** (Tableau d'Objets)
   - Représente les commentaires sur la publication.
   - Chaque objet contient :
     - `_id` (String) : ID unique du commentaire.
     - `userId` (String) : L'ID de l'utilisateur qui a fait le commentaire.
     - `postId` (String) : L'ID de la publication à laquelle le commentaire appartient.
     - `txt` (String) : Contenu textuel du commentaire.
     - `reactions` (Tableau d'Objets) : Réactions au commentaire, similaire au champ `reactions`.
     - `replies` (Tableau d'Objets) : Réponses au commentaire, chacune avec des champs comme `_id`, `userId`, `txt` et `createdAt`.
     - `createdAt` (Number) : Horodatage de la création du commentaire.

---

## Exemple de Document
```json
{
  "userId": "62ea127beb6ee5f8058fd56e",
  "title": "",
  "body": "Contenu d'exemple de publication",
  "reactions": [
    {"userId": "62f1fd355e2c0e39215035bb", "fullname": "Jean Dupont", "reaction": "like"}
  ],
  "createdAt": 1660681023611,
  "imgBodyUrl": "",
  "shares": [],
  "comments": [
    {
      "_id": "comment123",
      "userId": "62ea127beb6ee5f8058fd56e",
      "postId": "post123",
      "txt": "Ceci est un commentaire",
      "reactions": [
        {"userId": "62f201535e2c0e39215035bf", "fullname": "Marie Martin", "reaction": "like"}
      ],
      "replies": [],
      "createdAt": 1660724533161
    }
  ]
}
```
