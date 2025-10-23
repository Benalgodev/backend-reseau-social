# Schéma de la Collection Utilisateur

La collection `user` représente les utilisateurs dans l'application de médias sociaux. Voici une explication détaillée de sa structure et de ses champs :

## Structure du Schéma

### Champs

1. **`username`** (String)
   - Le nom d'utilisateur unique de l'utilisateur.

2. **`password`** (String)
   - Le mot de passe hashé de l'utilisateur.

3. **`profession`** (String)
   - La profession ou le titre professionnel de l'utilisateur.

4. **`fullname`** (String)
   - Le nom complet de l'utilisateur.

5. **`isAdmin`** (Boolean)
   - Indique si l'utilisateur a des privilèges administratifs.

6. **`age`** (Number)
   - L'âge de l'utilisateur.

7. **`createdAt`** (Number)
   - Horodatage indiquant quand l'utilisateur a été créé.

8. **`connections`** (Tableau d'Objets)
   - Représente les connexions de l'utilisateur avec d'autres utilisateurs.
   - Chaque objet contient :
     - `userId` (String) : L'ID de l'utilisateur connecté.
     - `fullname` (String) : Le nom complet de l'utilisateur connecté.
     - `connected` (Number) : Horodatage indiquant quand la connexion a été établie.

9. **`following`** (Array)
   - Liste des IDs des utilisateurs que l'utilisateur suit.

10. **`followers`** (Array)
    - Liste des IDs des utilisateurs qui suivent l'utilisateur.

11. **`gender`** (String)
    - Le genre de l'utilisateur (ex: "male", "female", "homme", "femme").

12. **`phone`** (String)
    - Le numéro de téléphone de l'utilisateur.

13. **`birthDate`** (String)
    - La date de naissance de l'utilisateur au format ISO (AAAA-MM-JJ).

14. **`email`** (String)
    - L'adresse email de l'utilisateur.

15. **`bg`** (String)
    - URL de l'image de fond de l'utilisateur.

16. **`imgUrl`** (String)
    - URL de l'image de profil de l'utilisateur.

---

## Exemple de Document

```json
{
  "username": "benalgodev123",
  "password": "$2b$10$fgsK0Yomf8Vdw3.bfIXJuOd/axCVx38HuYX9E.Bh7KS2Ik4kLd2zu",
  "profession": "Développeur Full-Stack",
  "fullname": "Benjamin Algodev",
  "isAdmin": false,
  "age": 28,
  "createdAt": 1659507323661,
  "connections": [
    {
      "userId": "62f138ee9f531ee7a0a6f276",
      "fullname": "Alice Martin",
      "connected": 4235353
    },
    {
      "userId": "62f1fd355e2c0e39215035bb",
      "fullname": "Pierre Dubois",
      "connected": 42353353
    }
  ],
  "following": [],
  "followers": [],
  "gender": "male",
  "phone": "0612345678",
  "birthDate": "1995-05-15",
  "email": "contact@benalgodev.com",
  "bg": "https://images.unsplash.com/photo-1556262298-e85892643712?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80",
  "imgUrl": "http://res.cloudinary.com/duajg3ah1/image/upload/v1660763357/benalgodev_profile.jpg"
}
```
