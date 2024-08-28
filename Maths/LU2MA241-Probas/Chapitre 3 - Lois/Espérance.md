#probas
## Définition
$X$ est une variable aléatoire discrète $X: \Omega \to \mathbb R$ avec $X(\Omega)$ un ensemble dénombrable.
$X$ admet une espérance si et seulement si #!
la somme $\sum_{x \in X(\Omega)} xp_X(x)$ est bien définie. Si c'est le cas alors cette somme est appelée espérance de $X$ et notée $\mathbb E[X]$ 
<!--ID: 1707733777453-->

## Différents cas d'espérance

### Dans $\mathbb{R}^+$ 
Soit $X(\Omega) \subset \mathbb R^+$, On pose la série $S = \sum_{x \in X(\Omega)} xp_X(x)$... Alors dans ce cas #!
La série $S$ est à termes positifs, et tends vers son supremum.
- Si la série diverge alors $\mathbb E[X] = +\infty$
- Si la série converge vers $l$, alors $\mathbb E[X]=l$ 
<!--ID: 1707735177466-->


### Au delà de $\mathbb{R}^+$ 
Soit $X(\Omega) \not\subset \mathbb R^+$. Soit $x^+ = \max{(x, 0)}, x^- = \max{(-x, 0)}$. On pose les séries $$S_+ = \sum_{x \in X(\Omega)} x^+p_X(x)$$ $$S_- = \sum_{x \in X(\Omega)} x^-p_X(x)$$Alors on a, en considérant $S = S_+ -  S_-$ #!

| S_- \ S_+ | $l \in \mathbb{R^+}$ | $+\infty$ |
|-----------|----------------------|-----------|
| $l' \in \mathbb{R^+}$          | $S = l-l'$                    | $S = +\infty$         |
| $+\infty$          | $S = - \infty$                     | undef          |
L'espérance n'existe pas dans une seule condition
<!--ID: 1707735177474-->

### Critères d'existence
On peut généraliser l'existence de l'espérance en 2 critères: #!
- On a que $X(\Omega) \subset \mathbb R ^+$ 
- L'espérance est finie $\Leftrightarrow$ $\sum_{x\in X(\Omega)} |x| p_X(x) < +\infty$  
<!--ID: 1707735584292-->


## Exemple fondamental
$X = \mathbb{1}_A$ avec $A$ un événement de $\mathcal{F}$ on a alors que: $p_X(1) = \mathbb P(A), p_X(0) = \mathbb{P}(A^c)$
L'espérance d'une telle loi existe car elle est dans $\mathbb{R^+}$ et celle-ci vaut: #!
$$\mathbb E [X] =  0 \times \mathbb P(A^c) + 1 \times \mathbb P(A)$$
$$\mathbb E [\mathbb 1_A] = \mathbb P(A)$$ 
<!--ID: 1707735632446-->

## Formule de transfert
$X$ est une [[Variables aléatoires discrètes]] avec $X:\Omega \to E$, Soit $g: E \to \mathbb R$, on note $Y = \text{"}g(X)\text{"} = g \circ X$. $Y$ admet une espérance si et seulement si #!

$$\sum_{x \in X(\Omega)} = g(x)p_X(x)$$ bien définie. Et on pose alors $\mathbb{E}(Y)$ la valeur de cette somme.
<!--ID: 1707735934438-->


### Preuve

1. Cas n°1: $g: E \to \mathbb{R}^+$ 
On a alors $Y(\Omega) \subset \mathbb R ^+$ et donc son espérance existe d'après [[#Critères d'existence|le premier critère d'existence]].
On a que $\mathbb E[Y] = \sum_{y \in Y(\Omega)} y p_Y(y)$.

$$ \set{Y =y} = \set{\omega \in \Omega, g(X(\omega)) = y}$$
$$= \set{\omega \in \Omega, X(\omega) \in g^{-1}(\set{y})}$$ $$ = \bigcup \set{\omega \in \Omega, X(\omega)= a} $$
Cette union est disjointe, et de plus, $a \in g^{-1}(\set{y}) \cap X(\Omega)$ un ensemble dénombrable, on a donc...
$$\mathbb E[Y] = \sum_{y \in Y(\Omega)} \sum_{a \in g^{-1}(\set{y}) \cap X(\Omega)} y p_X(a)$$
$$= \sum_{y \in Y(\Omega)} \sum_{a \in g^{-1}(\set{y}) \cap X(\Omega)} g(a) p_X(a)$$
$$= \sum_{a \in X(\Omega)} g(a) p_X(a)$$
$$\tag*{$\blacksquare$}$$
2. Cas n°2: $g: E \to \mathbb R$
En posant $g = g_+ - g_-$ on obtient le même raisonnement$$\tag*{$\blacksquare$}$$
## Propriétés de l'espérance
L'espérance respecte 3 différentes propriétés principales. Soit $X, Y$ deux [[Variables aléatoires discrètes]] admettant une espérance: #!

1. <u>Monotonie</u> Si $\forall \omega \in \Omega, X(\omega) \leq Y(\omega)$ alors $\mathbb E[X] \leq \mathbb E[Y]$
2. <u>Inégalité triangulaire</u> $|\mathbb E[X]| \leq \mathbb E[|X|]$
3. <u>Linéarité</u> Si l'espérance de $X,Y$ est finie, alors $\forall (a,b) \in \mathbb R ^2, \mathbb E[aX + bY] = a\mathbb E[X] + b \mathbb E[Y]$
<!--ID: 1707737809042-->

## Remarque sur l'espérance nulle
Si l'espérance d'une variable aléatoire $X$ est nulle alors #!
$X$ est nulle presque sûrement, i.e: $\mathbb P(X =0) = 1$
<!--ID: 1713305360772-->


## Indépendance sur l'espérance
Soit $X$ et $Y$, deux variables aléatoires indépendantes, alors on a que: #!
$$\mathbb E(XY) = \mathbb E(X)\mathbb E(Y)$$Pour $X$ et $Y$ positif, ou s'ils ont tout deux une espérance finie.
On observe alors que, si celle-ci est définie alors la [[Variances et covariances|Covariance]] $Cov(X, Y) = 0$ !
<!--ID: 1713305360776-->



## Espérance des lois classiques
On se souviendra des espérances suivantes: #!

- Loi Uniforme: $X \sim Unif(n), \mathbb E(X) = \frac{n+1}{2}$
- [[Loi de Bernoulli]]: $X \sim Bern(p), \mathbb E(X) = p$
- [[Loi binomiale]]: $X \sim Bin(n, p), \mathbb E(X) = np$
- [[Loi de Poisson]]:  $X \sim Poi(\lambda), \mathbb E(X) = \lambda$
- [[Loi géométrique]]: $X \sim Geo(p), \mathbb E(X) = \frac{1}{p}$
<!--ID: 1713305360779-->
