
## Définition
Soit $X$ une [[Variable aléatoire]] réel avec $X: \Omega \to \mathbb{R}$ et soit $\mu_{X}: \mathcal B(\mathbb{R}) \to [0, 1]$ sa [[Variable aléatoire|loi]]. On appelle sa fonction de répartition, notée $F_{X}$ comme étant: #!

$$
\forall y \in \mathbb{R}, F_{X}(y) =\mathbb{P}(X \leq y) = \mu_{X}(]-\infty; y])
$$
<!--ID: 1735577784404-->


## Propriété de base sur la fonction de répartition
On observe que: #!

- La fonction $F_{X}$ est croissante, continue ==à droite== et que $$
\lim_{ y \to -\infty } F_{X}(y) = 0 \text{ et } \lim_{ y \to +\infty } F_{X}(y) = 1
$$
- $\forall x \in \mathbb{R}$ on a que $$
\begin{align}
F_{X}(x^-) = \lim_{ y \to x^{-} } F_{X}(y) = \mu_{X}(]-\infty; x[)  \\
\text{ donc...} \\
F_{X}(x) - F_{X}(x^{-}) = \mu_{X}(\{ x\}) = \mathbb{P}(X =x)
\end{align}
$$
<!--ID: 1735577784407-->


## Propriété, équivalence des lois
Soit $(\Omega, \mathcal F, \mathbb{P})$ et $(\Omega', \mathcal F', \mathbb{P}')$ deux espaces de probabilités et $X: \Omega \to \mathbb{R}$, $Y: \Omega' \to \mathbb{R}$ deux variables aléatoires réelles. Alors elles suivent la même loi si et seulement si: #!
$$
F_{X} =  F_{Y}
$$
<!--ID: 1735577784409-->


## Propriété sur les variables à densité
Soit $X$ une [[Variable aléatoires à densité|variable aléatoire de densité]] $f$ par rapport à $l$. Alors observons ces propriétés sur sa fonctions de répartition: #!

$$
F_{X}(y) = \mu_{X}(]-\infty; y]) = \int_{]-\infty; y]} f \ dl
$$
De plus la fonction de répartition est de classe $\mathcal C^{1}$ et la densité $f$ est continue ==si et seulement si== $$
F_{X}' =f
$$
<!--ID: 1735577784411-->
