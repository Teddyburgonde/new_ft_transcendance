# new_ft_transcendance

# Installation d'un backend avec Fastify

## Prérequis
- Node.js et npm installés sur votre machine.
- Un éditeur de texte (ex. Visual Studio Code).

## Étapes de configuration

1. **Installer Node.js et npm**  
   Téléchargez et installez Node.js depuis le site officiel : [https://nodejs.org/](https://nodejs.org/).

2. **Créer un dossier pour le projet**  
   ```bash
   mkdir mon-projet-backend
   cd mon-projet-backend
   ```

3. **Initialiser le projet avec `npm init`**  
   ```bash
   npm init -y
   ```

4. **Installer Fastify**  
   ```bash
   npm install fastify
   ```

5. **Créer le fichier d'entrée `server.js`**  
   Créez un fichier nommé `server.js` à la racine de votre projet.

6. **Configurer le serveur de base avec Fastify**  
   Exemple de configuration de base :
   ```javascript
   const fastify = require('fastify')();

   fastify.get('/api/hello', async (request, reply) => {
       return { message: 'Hello, world!' };
   });

   fastify.listen(3000, (err, address) => {
       if (err) {
           console.error(err);
           process.exit(1);
       }
       console.log(`Server running at ${address}`);
   });
   ```

7. **Ajouter les routes nécessaires**
   - Ajoutez vos routes API pour les différentes fonctionnalités.

8. **Installer et configurer une base de données**  
   - Exemple : installer SQLite ou MongoDB selon les besoins.
   ```bash
   npm install sqlite3   # Pour SQLite
   ```

9. **Configurer les middlewares (si besoin)**  
   - Ajoutez des middlewares pour la gestion des requêtes (ex. CORS, JSON parsing).

10. **Ajouter la gestion des erreurs**
    - Gérez les erreurs globales dans le serveur.

11. **Tester le serveur localement**  
    ```bash
    node server.js
    ```

12. **Ajouter les fonctionnalités supplémentaires**  
    - Exemple : connexion à la base de données, authentification, validation des données, etc.

13. **Configurer les variables d'environnement**  
    - Créez un fichier `.env` pour stocker les variables sensibles.

14. **Tester et optimiser le backend**
    - Effectuez des tests unitaires et fonctionnels.

15. **Préparer le déploiement (si nécessaire)**  
    - Préparez votre backend pour le déploiement (ex. Docker, configuration serveur).

## Lancer le serveur
```bash
node server.js
```

## Félicitations ! 🎉
Vous avez maintenant un backend fonctionnel avec Fastify !
