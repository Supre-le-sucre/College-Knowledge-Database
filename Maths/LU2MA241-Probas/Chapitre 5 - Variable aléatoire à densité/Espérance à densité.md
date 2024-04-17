## Formule de transfert
### Cas positif
Soit $X$ une [[Variable aléatoires à densité]] avec pour densité $f_x$. On définit la formule de transfert dans le cas positif comme suit: #!

Soit $g: \mathbb R \to [0, +\infty[$ une fonction **positive** et **continue par morceaux**. L'espérance de la variable aléatoire de $g(X)$ est ==toujours== un élément bien défini de $[0, +\infty]$ et est donnée par: $$\mathbb E(g(X)) = \int_{-\infty}^{+\infty}g(x)f_X(x)dx$$ Ainsi donc, lorsque $X$ est ==positif==, son espérance est bien défini et vaut $$ \mathbb E(X) = \int_{-\infty}^{+\infty}xf_x(x)dx$$

Observons que la [[Fonctions génératrices des moments]] de $X$ une variable à densité est donc donnée par: #!
$$M_X(t) = \mathbb E\left(e^{tX}\right) = \int_{-\infty}^{+\infty}e^{tx}f_X(x)dx$$


### Cas intégrable
Soit $X$ une [[Variable aléatoires à densité]] avec pour densité $f_x$. On définit la formule de transfert dans le cas intégrable comme suit: