# Undercover

Jeu d'ambiance Undercover, de 3 à 5 joueurs, en français.

- **Un seul téléphone** : on se passe l'appareil.
- **En ligne** : chacun joue sur son téléphone. La partie est stockée dans une base Firebase Realtime Database : on peut rejoindre même si le téléphone de celui qui a créé la partie est en veille, et n'importe quel joueur peut faire avancer la partie.

## Fichiers

- `index.html` : tout le jeu (page, styles et code).
- `firebase-db.js` : SDK Firebase 12.19.0 (app + Realtime Database) regroupé en un seul fichier. Licence Apache-2.0, © Google LLC.
- `database.rules.json` : règles d'accès à copier dans la console Firebase (Realtime Database → Rules).

## Mise en ligne

GitHub Pages : Settings → Pages → Source *Deploy from a branch* → `main`, dossier `/ (root)`.

## Limites connues

- Les mots de toute la manche sont stockés dans la base : un joueur qui fouille les outils de développement de son navigateur pourrait les voir. Le jeu compte sur la confiance entre amis.
- Toute personne qui connaît le code d'une partie peut y agir.
