## Propriété de distances équivalente
On se donne 2 espaces métriques $(X, d_X), (Y, d_Y)$ et on considère $X \times Y$
Alors les 3 distances sur cette espace sont équivalentes: #!

$$d_1((x,y), (x', y')) = d_X(x, x') + d_Y(y, y')$$ $$d_2((x,y), (x', y')) = \sqrt{(d_X(x,x'))^2 + d_Y(y, y')^2}$$ $$d_\infty((x,y), (x',y')) = \sup(d_X(x,x'), d_Y(y,y'))$$
### Preuve
L'équivalence est maintenue dans le produit cartésien, d'où
$$d_\infty(x,y) \leq d_2(x,y) \leq d_1(x,y) \leq \sqrt 2 d_2(x,y) \leq 2d_\infty(x,y)$$
<!--ID: 1727636167116-->


## Pavé ouvert
Un pavé ouvert de $X \times Y$ est défini comme suit: #!

C'est un ensemble de type $U \times V$ où $U$ et $V$ sont respectivement des ouverts de $X$ et $Y$
<!--ID: 1727636167122-->


## Propriétés
On observe des propriétés importantes sur les produits d'espaces métriques: #!

1) $(x_n, y_n)_{n \in \mathbb N}$ suite de $X \times Y$ converge vers $(x,y)$ si et seulement si $x_n \to x, y_n \to y$
2) Les ouverts de $X \times Y$ sont les réunions des pavés ouverts qu'ils contiennents
<!--ID: 1727636167124-->


### Preuve
1)
$\Rightarrow$: Soit $(x_n, y_n) \to (x,y)$ dans $X \times Y$
On a alors que
$$d_\infty((x_n, y_n), (x,y)) = \sup(d_X(x_n,x), d(y_n,y)) < \epsilon$$
Donc on a que $d_X(x_n, x) < \epsilon$ et $d_Y(y_n, y) < \epsilon$
d'où $x_n \to x$ et $y_n \to y$

$\Leftarrow$: Soit $x_n \to x$ et $y_n \to y$
On a donc
$$\forall \epsilon > 0, \exists N = \max(N_1, N_2), \forall n > N, d_X(x_n, x) < \epsilon \text { et } d_Y(y_n, y) < \epsilon$$
Donc...
$$d_\infty((x_n, y_n), (x,y)) < \epsilon$$
$$\tag*{$\blacksquare$}$$

2)
$\Rightarrow$:  Soit $U \times V$ un pavé ouvert de $X \times Y$.
Montrons qu'il s'agit bien d'un ouvert de $X \times Y$

Soit $(x,y) \in U \times V$
On considère $B_{X \times Y}((x,y), \epsilon)$
$$B_{X \times Y}((x,y), \epsilon) = \set{(x',y'), d_\infty((x,y), (x',y')) < \epsilon}$$
$$ = \set{(x', y'), d_X(x,x') < \epsilon \text{ et } d_Y(y, y') < \epsilon}$$
$$=B_X(x, \epsilon) \times B_Y(y, \epsilon)$$
Donc $U \times V$ est un ouvert de $X \times Y$
Une union de pavé ouvert est donc ouvert

$\Leftarrow$: Soit $O$ un ouvert de $X \times Y$
Alors $\forall (x,y) \in O, \exists \epsilon_{(x,y)}, B_{X \times Y}((x,y), \epsilon_{(x,y)}) \subseteq O$
Donc $$O = \bigcup_{(x,y) \in O}B_{X \times Y}((x,y), \epsilon_{(x,y)}) = \bigcup_{(x,y) \in O} B_{X}((x,y), \epsilon_{(x,y)}) \times  B_{Y}((x,y), \epsilon_{(x,y)})$$
Et $O$ est donc un pavé ouvert