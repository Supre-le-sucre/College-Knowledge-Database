## Formule de transfert
### Cas positif
Soit $X$ une [[Variable aléatoires à densité]] avec pour densité $f_x$. On définit la formule de transfert dans le cas positif comme suit: #!

Soit $g: \mathbb R \to [0, +\infty[$ une fonction **positive** et **continue par morceaux**. L'espérance de la variable aléatoire de $g(X)$ est ==toujours== un élément bien défini de $[0, +\infty]$ et est donnée par: $$\mathbb E(g(X)) = \int_{-\infty}^{+\infty}g(x)f_X(x)dx$$ Ainsi donc, lorsque $X$ est ==positif==, son espérance est bien défini et vaut $$ \mathbb E(X) = \int_{-\infty}^{+\infty}xf_x(x)dx$$
<!--ID: 1713391707598-->


Observons que la [[Fonctions génératrices des moments]] de $X$ une variable à densité est donc donnée par: #!
$$M_X(t) = \mathbb E\left(e^{tX}\right) = \int_{-\infty}^{+\infty}e^{tx}f_X(x)dx$$
<!--ID: 1713391707602-->



### Cas intégrable
Soit $X$ une [[Variable aléatoires à densité]] avec pour densité $f_x$. On définit la formule de transfert dans le cas intégrable comme suit: #!

Soit $g: \mathbb R \to \mathbb R$ une fonction continue par morceaux. La variable aléatoire $g(X)$ admet une espérance finie si et seulement si la fonction $|g(x)|f_X(x)$ est intégrable sur $\mathbb R$ i.e 
$$\mathbb E(|g(X)|) < +\infty \Leftrightarrow \int_{-\infty}^{+\infty}|g(x)|f_X(x)|dx < +\infty$$
<!--ID: 1713391707605-->


## Corollaire: définition du moment à densité
Une [[Variable aléatoires à densité]] $X$ de densité $f_X$, admet un moment d'ordre $k$ si et seulement si: #!
On a que $\mathbb E(|X|^k) = \int_{-\infty}^{+\infty}|x|^kf_X(x)dx < +\infty$ dans ce cas, le moment d'ordre $k$ de $X$ est donnée par l'intégrale: $$\mathbb E(X^k) = \int_{-\infty}^{+\infty}x^kf_X(x)dx$$
<!--ID: 1713391707609-->
