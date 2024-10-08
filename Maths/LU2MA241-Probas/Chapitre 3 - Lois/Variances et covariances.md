#probas

## Définition
Soit $X$ une variable aléatoire définie sur $(\Omega, \mathcal F, \mathbb P)$. Si $X$ admet un [[Moments]] d'ordre 2 on appelle la variance de $X$ la quantité: #!
$$Var(X) = \mathbb E((X - \mathbb E(X))^2) = \mathbb E(X^2) - \mathbb E(X)^2 \geq 0$$
<!--ID: 1713305360727-->


Soit $X$ et $Y$ deux variables aléatoires définies sur $(\Omega, \mathcal F, \mathbb P)$ admettant un moment d'ordre 2. On appelle la covariance de $X$ et $Y$ la quantité: 
$$Cov(X, Y) = \mathbb E((X - \mathbb E(X))(Y - \mathbb E(Y))) = \mathbb E(XY) - \mathbb E(X)\mathbb E(Y)$$

## Propriété de la covariance
La covariance peut être considéré comme le produit scalaire probabiliste. #!
En effet, la covariance est une forme ==symétrique== et ==bilinéaire==, c'est à dire que pour tout variable aléatoires $X, Y, Z$ admettant un [[Moments]] d'ordre 2 et pour tout $\alpha, \beta \in \mathbb R$ on a: 
$$Cov(X, Y) = Cov(Y, X)$$$$Cov(\alpha X + \beta Y, Z) = \alpha Cov(X, Z) + \beta Cov(Y, Z)$$
<!--ID: 1713305360731-->


Lorsque $X$ et $Y$ sont presque sûrement constante, alors il est possible d'en déuire ce fait sur la covariance: #!
$$Cov(X, Y) = 0$$
Ceci venant du fait que cette forme est symétrique.
<!--ID: 1713305360734-->


## Propriété de la variance
Soit $X$ une variable aléatoire admettant un [[Moments]] d'ordre 2. On a alors les faits suivants: #!

- $\forall a,b \in \mathbb R, Var(aX + b) = a^2Var(X)$
- $Var(X) = 0$ si et seulement si $X$ est constante presque partout
- Si $X_1, \dots X_n$ sont des variables aléatoires admettant un moment d'ordre 2 fini on a $$Var\left(\sum_{i=1}^nX_i\right) = \sum_{i=1}^nVar(X_i) + \sum_{1 \leq i ,j\leq n, i \not = j} Cov(X_i, X_j) =  \sum_{i=1}^nVar(X_i) + 2\sum_{1 \leq i<j\leq n} Cov(X_i, X_j) $$
<!--ID: 1713305360737-->


## Indépendance sur la variance
Si $X_1, \dots, X_n$ sont des variables aléatoires indépendantes admettant un moment d'ordre 2 alors on a: #!
$$Var\left(\sum_{i=1}^nX _i\right) = \sum_{i=1}^nVar(X_i)$$
## Variances des lois classiques
On se souviendra des variances suivantes: #!

- Loi Uniforme: $X \sim Unif(n), Var(X) = \frac{n^2 - 1}{12}$
- [[Loi de Bernoulli]]: $X \sim Bern(p), Var(X) = p(1-p)$
- [[Loi binomiale]]: $X \sim Bin(n, p), Var(X) = np(1-p)$
- [[Loi de Poisson]]:  $X \sim Poi(\lambda), Var(X) = \lambda$
- [[Loi géométrique]]: $X \sim Geo(p), Var(X) = \frac{1-p}{p^2}$ 
<!--ID: 1713305360741-->
