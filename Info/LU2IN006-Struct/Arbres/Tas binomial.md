## Définition d'arbre binomial
On énonce la définition suivante: #!

Un arbre binomial d'ordre $k$, noté $B_k$ est défini récursivement de la manière suivante:
- $B_0$ est composé d'un seul nœud
- $B_k$ est un arbre dont la racine possède $k$ fils, et ses fils sont les arbres binomiaux d'ordres $k-1, k-2, \dots, 0$ dans cet ordre (de gauche à droite)
![[Pasted image 20240510115257.png]]

**Remarque**: On peut aussi définir $B_k$ à partir de deux arbres $B_{k-1}$, en plaçant l'un comme fils le plus à gauche de la racine de l'autre

## Propriété de taille sur l'arbre binomial
On observe que: #!

Pour un arbre binomial $B_k$, on a exactement $2^k$ nœuds, et sa hauteur est égale à $k$

## Tas binomial
On définit un 