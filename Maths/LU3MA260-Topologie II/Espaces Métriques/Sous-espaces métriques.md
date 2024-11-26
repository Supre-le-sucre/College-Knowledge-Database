#topo
## Définition
On définit un sous-espace métrique de la façon suivante: #!

Soit $(X, d)$ et $Y \subset X$, on a $(Y, d)$ un sous-espace métrique de $(X, d)$
<!--ID: 1729504947025-->



## Propriété sur les sous-espaces métriques
On observe les deux propriétés fondamentales suivantes: #!

Les ouverts de $(Y, d)$ sont les intersections des ouverts de $(X,d)$. On a donc
$$\forall O \in X, O \cap Y \text{ est un ouvert de } Y$$
$$\forall \tilde O \in Y, \exists O \in X, \tilde O  = O \cap Y$$
Si $(y_n)_{n \in N}$ est une suite de $Y$ convergente en $Y$, si et seulement si, $(x_n)_{n \in \mathbb N}$ converge dans $X$ et sa limite est en $Y$
<!--ID: 1729504947027-->



### Preuve
1)
$\Rightarrow$
Soit $O$ un ouvert de $Y$, montrons alors qu'il existe $\tilde O$ ouvert de $X$ tel que $O = \tilde O \cap Y$ 
Comme $O$ est un ouvert, on a
$$\forall y \in O, \exists \epsilon_y > 0, B_Y(y, \epsilon_y) \subseteq O$$
Posons que $O = \bigcup_{y \in O}B_Y(y, \epsilon_y)$
On choisit alors $\tilde O = \bigcup_{y \in O}B_X(y, \epsilon_y)$

$\tilde O$ est bien un ouvert de $X$ car il s'agit d'une union d'ouvert.
Mais on a aussi que $B_X(y, \epsilon_y) \cap Y = B_Y(y, \epsilon_y)$ 
Donc $\tilde O \cap Y = O$

$\Leftarrow$
Soit $\tilde O$ un ouvert de $X$ et $O = \tilde O \cap Y$ 
Montrons alors que $O$ est un ouvert de $Y$

Soit $y \in \tilde O \cap Y$, on a $y \in \tilde O \implies \exists \epsilon > 0 B(y, \epsilon) \subseteq \tilde O$
Donc finalement $B_Y(y, \epsilon) \subseteq \tilde O \cap Y$ 

2)
$\Rightarrow$ Soit $(y_n)_{n \in \mathbb N}$ une suite de $(Y, d)$ qui converge dans $Y$

$$\exists y \in Y, \forall \epsilon > 0, \exists N \in \mathbb N, \forall n \geq N, y_n \in B_Y(y, \epsilon) \subseteq B_X(y, \epsilon)$$
Ainsi donc $(y_n)_{n \in \mathbb N}$ converge dans $X$ et $y \in Y$

$\Leftarrow$ Soit $(y_n)_{n \in \mathbb N}$ une suite de $Y$ converge dans $X$ et $y \in Y$
$$\forall \epsilon > 0, \exists N\in \mathbb N, \forall n \geq N, y_n \in B_X(y, \epsilon)$$
Mais comme $y \in Y$ et $y_n \in Y$ alors on a bien $y_n \to y$ dans $(Y, d)$
$$\tag*{$\blacksquare$}$$