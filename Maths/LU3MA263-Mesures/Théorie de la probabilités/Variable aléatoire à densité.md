## Définition
Soit $X: \Omega \to \mathbb{R}$ une variable aléatoire avec $l$ la [[La mesure de Lebesgue]]. On dit que $X$ admet une densité $f$ par rapport à $l$ lorsque: #!

Pour $f$ une fonction mesurable positive, la [[Variable aléatoire|loi]] de $X$ admet la densité $f$ par rapport à $l$ soit alors $$
\forall A \in \mathcal B(\mathbb{R}), \mu_{X}(A) = \mathbb{P}(X \in A) = \int_{A} f \ dl
$$
Avec nécessairement que $\int_{\mathbb{R}}f  \ dl = 1$
<!--ID: 1735577943243-->



## Propriété de la formule de transfert
Dans le cas d'une variable aléatoire $X$ de densité $f$ par rapport à $l$, observons que: #!

Soit $g: \mathbb{R} \to [0, \infty]$, une fonction mesurable. Alors on a que $$
\mathbb{E}(g(X)) = \int_{\mathbb{R}}g \ d\mu_{X} = \int_{\mathbb{R}} gf dl 
$$
De même si $g$ est à valeur dans $\mathbb{C}$, tant qu'on a que $\mathbb{E}(|g(X)|) <\infty$
<!--ID: 1735577943244-->

