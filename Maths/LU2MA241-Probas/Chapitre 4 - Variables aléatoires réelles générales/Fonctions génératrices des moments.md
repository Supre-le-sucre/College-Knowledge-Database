## Définition
Soit une [[Variable aléatoire réelle]] $X$. On définit la fonction $M_X$ génératrice des moments de $X$ telle que: #!

Pour $M_X: \mathbb R \to \mathbb R \cup \{+\infty\}$ on a:
$$M_X(t) = \mathbb E(e^{tX})$$
<!--ID: 1713353114523-->


## DSE de la fonction génératrice des moments
Pour une [[Variable aléatoire réelle]] $X$, alors il est possible d'effectuer un développement en série entière de $M_X$ si: #!

Il existe $a$ tel que, $\forall t \in ]-a, a[, M_X(t) < +\infty$. Dans ce cas on a: $$M_X(t) = \sum^{+\infty}_{k=0}\mathbb E(X^k)\frac{t^k}{k!}$$ De fait, s'il existe un tel $a$ on aura que $M_X$ infiniment dérivable en $]-a, a[$ avec
$$\mathbb E(X^k) = M_X^{(k)}(0)$$
<!--ID: 1713353114526-->


## Indépendance
Soit $X$ et $Y$ deux [[Variable aléatoire réelle]] indépendante. On peut déduire que la fonction génératrice de moment de $X+Y$ sera telle que: #!
$$\forall t \in \mathbb R, M_{X+Y}(t) = M_X(t)M_Y(t)$$
<!--ID: 1713353114530-->

