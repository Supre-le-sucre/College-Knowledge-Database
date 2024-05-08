Un arbre rouge noir est une variante aux [[Arbres AVL]] nécessitant moins de rotations en pratique

## Définition
Un arbre rouge-noir (ou bicolore) est un arbre respectant les propriétés suivantes: #!

- Il s'agit d'un [[ABR ou Arbre binaire de recherche]]
- Chaque nœud est de couleur noire ou rouge
- la racine est toujours de couleurs noire
- les fils d'un nœud rouge sont toujours de couleur noire
- si un nœud a moins de deux fils, on lui ajoute un nœud fictif noir
- le nombre de nœuds noirs sur un chemin de la racine vers une feuille est toujours le même et on l'appelle "hauteur noire"

## Observation sur la longueur d'un chemin
Dans un arbre rouge-noir on peut observer que: #!
Le plus long chemin de la racine vers une feuille est au plus deux fois plus long que le plus petit chemin. De plus la haute $h$ est donc au plus égale à $2h_N$

### Preuve
Chaque chemin passe exactement, par définition, par $h_N$ nœuds noirs. Le plus petit chemin possède donc ==au moins== $h_N$ nœuds.
De plus par définition, il n'est pas possible sur un même chemin d'avoir 2 nœuds rouges consécutifs, donc le plus long chemin alterne les nœuds rouges et noirs et a donc une taille de $2h_N$

## Hauteur d'un arbre rouge-noir
On observe que: #!
La hauteur d'un arbre rouge noir est de l'ordre de $O(log(n))$

### Preuve
On montre ceci par récurrence.
$\Pi(n)$: "Un arbre rouge noir de de hauteur noire $h_N = n$ vérifie $n \geq 2^{h_N}-1$"

Pour $h_N = 0$ alors on a forcément que $n=0$ car la racine est forcément noire

Pour un arbre tel que $h_N = n$, observons que comme la racine est forcément noire, les sous-arbres gauche et droit ont forcément une hauteur noire diminuée de 1.
Par hypothèse de récurrence ces sous-arbres possède au moins $2^{h_N - 1} - 1$ nœuds 