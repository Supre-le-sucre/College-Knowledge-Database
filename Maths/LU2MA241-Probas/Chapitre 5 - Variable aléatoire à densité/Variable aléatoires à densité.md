## Définition
Soit $X$ une [[Variable aléatoire réelle]]. On dit que cette variable aléatoire est *absolument continue* ou *à densité* si et seulement si: #!
Il existe une fonction positive $f_x: \mathbb R \to [0, +\infty[$ intégrable sur $\mathbb R$ telle que la [[Fonctions de répartition]] de $X$ peut s'écrire de la façon suivante: $$F_X(t) = \mathbb P(X \leq t) = \int_{-\infty}^t f_x(x)dx$$ ==Attention:== $f_x$ n'est **PAS** une probabilité

## Remarque sur la fonction de répartition
Si $X$ est une variable aléatoire à densité alors $F_X$ est continue en tout point

## Formules sur intervalle
Observons que pour une variable aléatoire à densité $X$, on a que $\mathbb P(X=k) =0$ par définition. Ceci nous permettant donc d'établir une formule de probabilité lorsque $X$ est dans n'importe quel type d'intervalle entre $a$ et $b$: #!
$$\mathbb P(X \in [a,b]) = \mathbb P(X \in ]a,b[) = \mathbb P(X \in ]a,b]) = \mathbb P(X \in [a,b[) = F_X(b) - F_X(a) = \int_a^b$$