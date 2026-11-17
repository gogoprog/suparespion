# 🕵️ Supar Espion

Jeu d'ambiance en HTML5 pour jouer à l'espion à plusieurs, sur **un seul appareil** (PC ou smartphone) que l'on se passe de main en main.

Tout le monde reçoit le même mot secret… sauf l'espion. À tour de rôle, chacun évoque son mot sans être trop précis, puis on vote pour démasquer l'espion.

## Jouer

Aucune installation : ouvrir `index.html` dans un navigateur.

Pour jouer sur smartphone, héberger le fichier n'importe où (GitHub Pages, serveur local…) ou le copier directement sur le téléphone.

## Déroulement

1. **Joueurs** : ajouter au moins 3 joueurs (ils sont enregistrés dans le navigateur, avec leurs scores).
2. **Distribution** : l'appareil passe de joueur en joueur ; chacun touche l'écran pour voir son mot, puis le cache avant de passer.
3. **Discussion** : un joueur tiré au sort commence. Chrono optionnel (3 ou 5 min).
4. **Vote** : on vote à voix haute et on touche le joueur éliminé. Son rôle est révélé.
5. **Fin** : les civils gagnent quand tous les espions sont éliminés ; les espions gagnent s'ils sont aussi nombreux que les civils restants.

## Options

- **Nombre d'espions** : de 1 jusqu'à moins de la moitié des joueurs.
- **L'espion reçoit** :
  - *Rien* : l'espion sait qu'il est espion. S'il est démasqué, il peut encore gagner en devinant le mot des civils.
  - *Mot proche* : l'espion reçoit un mot voisin (ex. Pizza / Tarte flambée) et ne sait pas qu'il est l'espion.
- **Catégories** : 13 catégories activables, environ 100 paires de mots chacune (≈ 1 350 paires au total).

## Scores

- Civil gagnant : +1 point
- Espion gagnant : +2 points

## Ajouter des mots

Le dictionnaire est l'objet `DICT` en haut du script dans `index.html` : chaque catégorie est une liste de paires `["mot des civils", "mot proche"]`. Les paires sont tirées dans les deux sens.
