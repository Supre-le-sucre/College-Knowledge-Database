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

## Définition d'un tas binomial
On définit un tas binomial de la façon suivante: #!

Il s'agit d'une liste d'arbre binomiaux telle que:
- Dans chaque arbre binomial, la clé d'un nœud est toujours inférieur à celle de ses fils
- Tous les arbres sont d'ordres différents

### Conséquence de la définition
On observe que pour un tas binomial: #!

- Le plus petit élément est une des racines des arbres binomiaux
- Un tas binomial contenant $n$ éléments possède au plus $\lfloor \log(n) +1\rfloor$ arbre binomiaux. Plus précisément le nombre et l'ordre de ces arbres est unique et déterminé par la représentation binaire de $n$.
	 *Par exemple, un tas binomial de 11 éléments sera constitué d'arbre binomial d'ordre 3, 1 et 0 car on représente 11 par 1011

## Fusion de tas binomiaux
La fusion se déroule de la façon suivante: #!

Pour fusionner deux tas binomiaux $F_1$ et $F_2$, on parcourt leur listes d'arbres binomiaux en même temps, en commençant par ceux de plus petits ordre.
- Si $F_1$ et $F_2$ possèdent tous deux un arbre d'ordre $k$, on créer un arbre d'ordre $k+1$ tel que, la plus grande des deux racines devient le premier fils de la plus petite racine