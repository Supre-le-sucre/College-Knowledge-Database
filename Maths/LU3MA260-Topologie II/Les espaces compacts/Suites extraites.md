#topo
## Définition d'une suite extraite
Soit $(X,d)$ et $(x_n)_{n \in \mathbb N}$ une suite de $X$ #!

On appelle suite extraite de $(x_n)_{n \in \mathbb N}$ une suite de la forme$(x_{n_1}, x_{n_2}, \dots)$ avec $n_1 < n_2 < \dots$
On peut aussi dire que $(y_n)_{n \in \mathbb N}$ est une sous-suite extraite de $(x_n)$ si et seulement si il existe $\phi: \mathbb N \to \mathbb N$ strictement croissante, telle que $y_n =x_{\phi(n)}$ 
<!--ID: 1729505040447-->



On définit alors une valeur d'adhérence d'une suite $(x_n)$ un nombre $\rho$ tel que:
Il existe une sous-suite de $(x_n)$ qui converge vers $\rho$

## Intersection de compacts
On observe le phénomène suivant: #!
Soit $(X,d)$ un espace avec $(K_n)_{n \in \mathbb N}$ une suite de compact non vide décroissante, alors
$$\bigcap_{n \in \mathbb N}K_n \not = \emptyset$$
<!--ID: 1729505040449-->


**Remarque**: Si $(K_n)_{n \in \mathbb N}$ sont fermés, alors on pourrait prendre $K_n = \set{n, n+1, \dots}$ et donc $\bigcap_{n \in \mathbb N}K_n = \emptyset$

### Preuve
Comme $\forall n \in \mathbb N, K_n \not = \emptyset$ alors on peut récupérer un élément $x_n \in K_n, \forall n \in \mathbb N$ 
Et comme $K_{n+1} \subseteq K_n$, on a que $x_n \in K_j, \forall n \geq j$

En particulier alors, $(x_n)_{n \in \mathbb N}$ est une suite du compact $K_0$, donc on a $\phi$ tel que $x_{\phi(n)} \to x \in K_0$
Et $\forall j \in \mathbb N$, la suite $(x_n)_{n \geq j}$ est une suite de $K_j \subseteq K_0$, donc $x_\phi(n)$ converge dans $K_j$
Donc finalement $x \in \bigcap_{n \in \mathbb N}K_n$
$$\tag*{$\blacksquare$}$$