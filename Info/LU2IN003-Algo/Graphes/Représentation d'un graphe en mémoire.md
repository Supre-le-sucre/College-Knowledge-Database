Il y a différentes façon de représenter le graphe $G = (V, E)$ [[Graphes non orientés|orienté]] ou [[Graphes non orientés|non]] 

## Matrice sommet-arête (sommet-arcs)
On définit la matrice sommet-arête $M$ comme: #!

Pour tout couple $(i,j) \in V \times E$
- $M[i,j] = 1$ si $i$ est incident à $j$ (i.e si $j$ arrive sur le sommet $i$)
- $M[i,j] = 0$ s'il n'y pas de lien entre $i$ et $j$
- $M[i,j] = -1$ si $j$ est issue de $i$ (seulement pour les [[Graphes non orientés]])
<!--ID: 1715702538617-->


## Matrice sommet-sommet
On définit la matrice sommet-sommet $M$ comme: #!

Pour tout couple $(i,j) \in V \times V$
- $M[i,j] = 1$ si de $i$ on peut rejoindre $j$
- $M[i,j] = 0$ s'il n'y pas d'accès direct de $i$ vers $j$
<!--ID: 1715702538620-->


## Listes d'adjacences
On définit la liste d'adjacence de la façon suivante: #!

Pour $i \in V$, on a $L[i]$ la liste des sommets adjacents à $i$
<!--ID: 1715702538622-->



## Tableau de comparaison

### Taille mémoire
On observe pour différentes représentations d'un graphe en mémoire, les tailles suivantes: #!

|                                    | Taille mémoire               |
| ---------------------------------- | ---------------------------- |
| Matrice sommet-arête (sommet-arcs) | $\Theta(\|V\| \times \|E\|)$ |
| Matrice sommet-sommet              | $\Theta(\|V\|^2)$            |
| Liste d'adjacance                  | $\Theta(\max(\|V\|, \|E\|))$ |
<!--ID: 1715702538625-->


### Complexité
On cherche à évaluer la complexité de primitive simple:
- `existeArete(i,j)` (ou `existeArc(i,j)`) vérifie l'existence d'un arête $\set{i,j}$ (ou d'un arc $(i,j)$)
- `adjacent(i)` (ou `successeur(i)`) qui renvoie les sommets adjacents de `i` 
- `predecesseur(i)` qui renvoie les prédécesseurs de $i$ (dans le cas d'un graphe orienté)

|                                    | existence      | adjacence      | prédécesseurs   |
| ---------------------------------- | -------------- | -------------- | --------------- |
| Matrice sommet-arête (sommet-arcs) | $O(m)$         | $O(m\times n)$ | $O(m \times n)$ |
| Matrice sommet-sommet              | $\Theta(1)$    | $\Theta(n)$    | $\Theta(n)$     |
| Liste d'adjacance                  | $\Theta(d(i))$ | $\Theta(1)$    | $\Theta(m)$     |

