## Définition
On définit une loi de poisson $X \sim Poi(\lambda)$ comme étant #!
La limite de la probabilité lorsque $n \to + \infty$ d'une variable aléatoire $X_n$ suivant une [[Loi binomiale]] de paramètre $Bin(n, \frac{\lambda}{n})$. Autrement dit
$$\mathbb P(X =k) = \lim_{n \to +\infty} \mathbb P(X_n = k)=\frac{\lambda^k}{k!}e^\lambda$$
<!--ID: 1713305360748-->


## Propriété de composition
Si $X \sim Poi(\lambda)$ et $Y \sim Poi(\mu)$ deux variables aléatoires indépendantes, alors on peut dire que leur somme est telle que: #!
$$X +Y \sim Poi(\lambda + \mu)$$
Cette propriété se démontre sobrement de manière calculatoire
<!--ID: 1713305360751-->
