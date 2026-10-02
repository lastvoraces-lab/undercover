# Jeux entre amis

Collection de jeux d'ambiance en français. La page d'accueil (`index.html`) présente les jeux ; chaque jeu vit dans son propre dossier.

## Undercover (`undercover/`)

Jeu d'ambiance Undercover, de 3 à 10 joueurs.

- **Un seul téléphone** : on se passe l'appareil.
- **En ligne** : chacun joue sur son téléphone. La partie est stockée dans une base Firebase Realtime Database : on peut rejoindre même si le téléphone de celui qui a créé la partie est en veille, et le créateur de la partie lance les manches.

## Fichiers

- `index.html` : page d'accueil de la collection.
- `undercover/index.html` : le jeu Undercover ; `undercover/pairs.js` : paires de mots ; `undercover/definitions.js` : définitions.
- `shared/firebase-db.js` : SDK Firebase 12.19.0 (app + Realtime Database) regroupé en un seul fichier. Licence Apache-2.0, © Google LLC.
- `database.rules.json` : règles d'accès à copier dans la console Firebase (Realtime Database → Rules).

## Mise en ligne

GitHub Pages : Settings → Pages → Source *Deploy from a branch* → `main`, dossier `/ (root)`.

## Limites connues

- Les mots de toute la manche sont stockés dans la base : un joueur qui fouille les outils de développement de son navigateur pourrait les voir. Le jeu compte sur la confiance entre amis.
- Toute personne qui connaît le code d'une partie peut y agir.

## Trait suspect (`draw/`)

Dessin commun, un trait par joueur et par tour (deux tours). Tout le monde connaît le sujet sauf l'imposteur, qui ne connaît que la catégorie. Vote pour le démasquer ; s'il est démasqué, il peut encore deviner le sujet.

- `draw/index.html` : le jeu ; `draw/words.js` : sujets à dessiner par catégorie.
- Les parties en ligne utilisent la même base Firebase (`games/<CODE>`, avec `type: "draw"`).
