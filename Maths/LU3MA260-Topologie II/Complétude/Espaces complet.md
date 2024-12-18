#topo
## Définition
Un espace $(X,d)$ est qualifié de complet si et seulement si: #!

Pour tout suite $(x_n)_{n \in \mathbb N}$ de [[Suites de Cauchy|Cauchy]] sur $X$, on a que $(x_n)$ est convergente
<!--ID: 1729504820698-->



## Espace de Banach
On définit un espace de Banach de la façon suivante: #!

On considère l'espace métrique $(X, d)$ et l'espace $(E, ||\cdot||)$ normé tel que
$$d(x,y) = ||x-y||$$
Si $(E, ||\cdot||)$ est complet, alors c'est un espace de Banach.
<!--ID: 1729504820702-->




## Opérations sur les espaces complets
On observe 2 propriétés intéressantes sur les espaces complet: #!

- Soit $(X,d)$ un espace complet et $Y \subseteq X$, alors $(Y, d)$ est complet si et seulement si $Y$ est un fermé de $X$
- Le produit de deux espaces complets est complet
<!--ID: 1729504820704-->



### Preuve
1)
$\Rightarrow$ Soit $Y \subset X$ et $(Y,d)$ complet, montrons que $Y$ est un fermé de $X$

Soit $(y_n)_{n \in \mathbb N}$ une suite de $Y$ qui converge vers $y \in X$
On va montrer que $y \in Y$

Comme $(y_n)$ converge en $y$ dans $X$, la suite est de Cauchy. Mais comme $Y$ est complet, une suite de Cauchy converge dans son espace. donc $y \in Y$

$\Leftarrow$ Soit $Y \subseteq X$ est un fermé, montrons que $(Y, d)$ est complet

On prends à nouveau une suite $(y_n)_{n \in \mathbb N}$ de $Y$ qui est de Cauchy. Montrons que celle-ci converge.
Observons que $(y_n)$ est aussi une suite de $X$... Donc comme elle est de Cauchy et que $X$ est complet, la suite $(y_n)$ converge. Comme $Y$ est un espace fermé, la suite $(y_n)$ converge donc vers $y \in Y$
Donc $(Y, d)$ est complet

2)
On considère $(X_1, d_1)$ et $(X_2, d_2)$ deux espaces complets.

Nous utiliserons [[Produits d'espaces métriques#Propriété de distances équivalente|la définition]] de $d_\infty$
On considère $(x_n, y_n) \in X_1^\mathbb N \times X_2^\mathbb N$ une suite de Cauchy. Montrons qu'elle converge.
Comme elle est de Cauchy on a donc que
$$\forall \epsilon > 0, \exists N \in \mathbb N, \forall p, q \geq N, d_\infty((x_p, y_p), (x_q, y_q))$$
D'où
$$\forall \epsilon > 0, \exists N \in \mathbb N, \forall p, q \geq N, d_1(x_p, x_q) < \epsilon \text{ et } d_2(y_p,y_q) < \epsilon$$Or comme les espaces $X_1$ et $X_2$ sont complets, les suites $x_n$ et $y_n$ sont convergentes:
$$\forall \epsilon > 0, \exists N = \max(N_1, N2), \forall n > N, d_1(x_n, x) < \epsilon \text{ et } d_2(y_n, y) < \epsilon$$
D'où
$$\forall \epsilon > 0, \exists N, \forall n > N, d_\infty((x_n,y_n), (x,y)) < \epsilon$$
$$\tag*{$\blacksquare$}$$

## Propriété distances équivalentes sur la complétude
On observe que: #!

Si $d_1$ et $d_2$ sont deux [[Distances équivalentes]] alors $(X, d_1)$ est complet, si et seulement si, $(X, d_2)$ est complet
<!--ID: 1729504820707-->



### Preuve

Si $d_1$ et $d_2$ sont équivalente, alors $\exists c_1, c_2, \forall(x,y) \in X^2$
$$c_1d_1(x,y) \leq d_2(x,y) \leq c_2d_1(x,y)$$

Supposons $(X, d_1)$ complet et que $(x_n)_{n \in \mathbb N}$ est une suite de Cauchy sur $(X, d_2)$
Or puisque
$$c_1d_1(x,y) \leq d_2(x,y)$$
Elle est donc de Cauchy sur $(X, d_1)$, mais comme $(X, d_1)$ est complet, cette suite est convergente et puisque
$$d_2(x,y) \leq c_2d_1(x,y)$$
On a donc bien la convergence sur $(X, d_2)$.
Et vice-versa...
$$\tag*{$\blacksquare$}$$