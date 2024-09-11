## Définition
Soit $X$ une [[Variable aléatoires à densité]]. On dit qu'elle suit une loi exponentielle de paramètre $\lambda$, noté $X \sim \epsilon(\lambda)$ si elle a pour densité: #!
$$f_X(x) = \lambda e^{-\lambda x}\mathbb 1_{[0, +\infty[(x)}$$
Et en particulier on a
$$F_X(t) = \int_{-\infty}^t f_X(x)dx = \int_0^t\lambda e^{-\lambda x}dx = 1-e^{-\lambda t}$$
<!--ID: 1713391707584-->


## Absence de mémoire
La loi exponentielle discrète n'a pas de mémoire, c'est à dire que: #!
$$X \sim \epsilon(\lambda) \implies \mathbb P(X > s+t\; |\; X> s) = \mathbb P(X > t)$$
La démonstration est purement calculatoire
<!--ID: 1713391707589-->
