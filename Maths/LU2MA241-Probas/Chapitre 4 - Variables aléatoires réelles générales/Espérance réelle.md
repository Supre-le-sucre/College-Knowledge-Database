## Définition
Soit une [[Variable aléatoire réelle]] $X$ dans un espace probabilisé $(\Omega, \mathcal F, \mathbb P)$. Il y a différentes conditions pour définir l'espérance d'une telle variable aléatoire: #!

- Si $X \geq 0$, on définit alors la [[Variables aléatoires discrètes]] $X_n = 2^{-n}\lfloor2^nX\rfloor$ On a alors que $$E(X) = \lim_{n \to +\infty} \mathbb E(X_n) \in [0, +\infty]$$
- En général, on dit que $X$ admet une espérance si au moins une des espérances $\mathbb E(X^+)$ ou $\mathbb E(X^-)$ est finie. On aura alors que: $$\mathbb E(X) = \mathbb E(X^+) - \mathbb E(X^-) \in [-\infty, +\infty]$$
<!--ID: 1713353114547-->


## Propriété sur l'espérance
On observe les même propriétés de l'espérance discrète sur l'espérance réelle: #!

- Si $X \leq Y$ alors $\mathbb E(X) \leq \mathbb E(Y)$ pourvu que $X, Y$ admettent une espérance
- Si $X$ admet une espérance alors, $|\mathbb E(X)| \leq \mathbb E(|X|)$
- $\forall X,Y$ des [[Variable aléatoire réelle]] et $\forall a,b \in \mathbb R$ on a: $\mathbb E(aX + bY) = \mathbb a\mathbb E(X) + b\mathbb E(Y)$
- Si $X$ et $Y$ sont indépendantes, alors $\mathbb E(XY) = \mathbb E(X)\mathbb E(Y)$ si $X, Y$ positifs ou admettant une espérance finie
<!--ID: 1713353114550-->
