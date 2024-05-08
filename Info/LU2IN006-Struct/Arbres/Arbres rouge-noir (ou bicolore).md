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

## Hauteur d'un arbre 