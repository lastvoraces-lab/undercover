# Undercover

Jeu d'ambiance Undercover, de 3 à 5 joueurs, en français.

- **Un seul téléphone** : on se passe l'appareil.
- **En ligne** : chacun joue sur son téléphone. Le téléphone de l'hôte fait tourner la partie ; les autres s'y connectent directement (WebRTC) grâce à [PeerJS](https://peerjs.com). Le service public gratuit de PeerJS sert seulement à mettre les téléphones en relation.

## Fichiers

- `index.html` : tout le jeu (page, styles et code).
- `peerjs.min.js` : bibliothèque PeerJS 1.5.5 (licence MIT, voir `PEERJS-LICENSE`).

## Mise en ligne avec GitHub Pages

Settings → Pages → Source : *Deploy from a branch* → branche `main`, dossier `/ (root)` → Save.
Le jeu est ensuite disponible à l'adresse `https://<utilisateur>.github.io/<nom-du-dépôt>/`.

## Limites connues

- Le téléphone de l'hôte doit garder la page ouverte et l'écran allumé.
- La connexion directe entre téléphones peut échouer sur certains réseaux mobiles (pas de serveur relais TURN).
- Le service public PeerJS est gratuit et sans garantie de disponibilité.
