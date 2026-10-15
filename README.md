# Pour toi — Lettre d’amour cinématique

Application statique en français, adaptée aux téléphones. Aucun compte, aucune dépendance et aucune compilation nécessaires.

## Lancer

Ouvrir ce dossier dans Visual Studio Code, puis ouvrir `index.html` dans un navigateur.
Pour un serveur local, depuis ce dossier :

```sh
python3 -m http.server 8000
```

Ouvrir http://localhost:8000. Le chargement des polices Google nécessite Internet ; des polices de secours sont prévues.

## Personnaliser avant l’envoi

1. Ouvrir `config.js` et remplacer le texte de démonstration dans `text` par la lettre complète.
2. Déposer la musique dans `assets/musique.mp3`, puis mettre `music: "assets/musique.mp3"`.
3. Régler `duration` (secondes). Enregistrer et actualiser.
4. Tester « Oui, je suis prête » : la musique démarre au clic, puis la lettre s’écrit caractère par caractère. Les ponctuations ralentissent l’écriture. Le texte remonte pour garder les nouvelles lignes visibles.
5. Tester les boutons Pause, Reprendre, Son, Recommencer et Fermer.

Le bouton de préparation apparaît uniquement avec `?edition=1` à la fin de l’adresse. Il permet un aperçu et la copie d’un lien personnalisé. Ses changements restent dans le navigateur ou le lien ; pour modifier durablement la lettre du site, modifier `config.js`.
Un fichier audio local sélectionné dans la préparation sert uniquement à l’aperçu. Pour l’envoi, utiliser le fichier audio publié dans `assets` ou une URL audio directe. Les liens Spotify/YouTube ne sont pas pris en charge.

## Fichiers

- `index.html` : structure et écrans.
- `style.css` : couleurs, typographie et présentation responsive.
- `script.js` : écriture cinématique, musique et commandes.
- `config.js` : lettre, musique et durée.
- `assets/` : musique et autres fichiers.

## GitHub Pages

Pousser les fichiers à la racine du dépôt. Dans les paramètres du dépôt, ouvrir Pages, choisir la publication depuis une branche, puis sélectionner la branche et le dossier racine. Utiliser l’adresse indiquée par GitHub après publication.

La lettre et la musique sont accessibles aux visiteurs du site et peuvent être visibles dans un dépôt public. Un lien personnalisé contient son texte dans le fragment de l’URL ; toute personne qui possède ce lien peut le lire.
