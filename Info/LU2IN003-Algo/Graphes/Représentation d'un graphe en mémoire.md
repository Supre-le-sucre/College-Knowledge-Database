Il y a différentes façon de représenter le graphe $G = (V, E)$ [[Graphes non orientés|orienté]] ou [[Graphes non orientés|non]] 

## Matrice sommet-arête
On définit la matrice sommet-arête $M$ comme: #!

Pour tout couple $(i,j) \in V \times E$
- $M[i,j] = 1$ si $i$ est incident à $j$ (i.e si $j$ arrive sur le sommet $i$)
- $M[i,j] = 0$ s'il n'y pas de lien entre $i$ et $j$
- $M[i,j] = -1$ si $j$ est issue de $i$ (seulement pour les [[Graphes non orientés]])

## Matrice sommet-sommet
On définit la matrice sommet-sommet $M$ comme: #!

Pour tout couple $(i,j) \in V \times V$
- $M[i,j] = 1$ si de $i$ on peut rejoindre $j$
- $M[i,j] = 0$ s'il n'y pas d'accès direct de $i$ vers $j$

## Listes d'adjacences
On définit la liste d'adjacence de la façon suivante: #!

Pour $i \in V$, on a $L[i]$ la liste des sommets adjacents à $i$


## Tableau de comparaison

### Taille mémoire
