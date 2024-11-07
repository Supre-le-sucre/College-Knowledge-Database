## Définition
Un tas peut être défini de la façon suivante: #!

Un tas est un [[Arbres parfait]] croissant, c'est à dire que toutes les étiquettes fils de $x$ doivent être plus grande que $x$
<!--ID: 1715690724149-->


## Insertion
Dans un tas, on insère un élément de la façon suivante: #!

On l'ajoute à la fin du tas comme dans un [[Arbres parfait]], sauf que l'on fait les permutations nécessaires entre père et fils pour conserver son intégrité. 
La complexité d'une insertion est donc de $O(\log(n))$
<!--ID: 1715690724151-->


## Suppression du minimum
Dans un tas, on supprime le minimum de la façon suivante: #!

Le minimum est toujours à la racine, on fait passer la racine vers la feuille du sous arbre gauche la plus à droite en faisant toutes les permutations nécessaire, et on supprime cette feuille. 
La complexité de suppression est en $O(\log(n))$
<!--ID: 1715690724152-->


