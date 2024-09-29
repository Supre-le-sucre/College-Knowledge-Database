## Définition
Un espace $(X,d)$ est qualifié de complet si et seulement si: #!

Pour tout suite $(x_n)_{n \in \mathbb N}$ de [[Suites de Cauchy|Cauchy]] sur $X$, on a que $(x_n)$ est convergente

## Espace de Banach
On définit un espace de Banach de la façon suivante: #!

On considère l'espace métrique $(X, d)$ et l'espace $(E, ||\cdot||)$ normé tel que
$$d(x,y) = ||x-y||$$
Si $(E, ||\cdot||)$ est complet, alors c'est un espace de Banach.


## Opérations sur les espaces complets
On observe 2 propriétés intéressantes sur les espaces complet: #!

- Soit $(X,d)$ un espace complet et $Y \subseteq X$, alors $(Y, d)$ est complet si et seulement si $Y$ est un fermé de $X$
- Le produit de deux espaces complets est complet

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
Et donc d'après $d_\infty$ on aura bien que $(x_n, y_n) \to (x,y)$

