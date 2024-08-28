## Définition
Une variable aléatoire réelle absolument continue $Z$ est dite *"normale"* ou *"gaussienne"* standard (et on écrit $Z \sim \mathcal N(0,1)$) si elle a pour densité: #!
$$f_Z(x) = \frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}$$
<!--ID: 1715790676161-->


De manière générale une variable aléatoire suivant $X \sim \mathcal N(\mu, \sigma^2)$ admet pour densité: #!
$$f_X(x)=\frac{1}{\sqrt{2\pi\sigma^2}}e^{-\frac{(x- \mu)^2}{2\sigma^2}}$$Et elle admet pour espérance $\mathbb E(X)=\mu$ et comme variance $Var(X)=\sigma^2$. Notons que l'on peut se ramener à une loi normale standard $$X \sim \mathcal N(\mu, \sigma^2) \Leftrightarrow Z := \frac{X-\mu}{\sigma} \sim \mathcal N(0,1)$$
<!--ID: 1715790676164-->


## Transformation affine
Pour une variable aléatoire $X \sim \mathcal N(\mu, \sigma^2)$ on observe les propriétés suivantes: #!
$$\forall a,b \in \mathbb R,\; aX+b \sim \mathcal N(a\mu+b,\; a^2\sigma^2)$$
<!--ID: 1715790676167-->


## Fonction génératrice des moments
Pour $Z \sim \mathcal N(0,1)$ on observe que: #!
$$M_Z(t) = e^{\frac{t^2}{2}}$$
## Somme de normales indépendantes
On observe que pour $X \sim \mathcal N(\mu_1, \sigma_1^2)$ et $Y \sim \mathcal N(\mu_2, \sigma_2^2)$ on a alors: #!
$$X+Y \sim \mathcal N(\mu_1 + \mu_2, \;\sigma_1^2 + \sigma_2^2)$$
<!--ID: 1715790676169-->


### Corollaire
Soient $X_1, \dots, X_n$ des variables aléatoires normales indépendantes. On observe que toute combinaison linéaire de ces variables suivent une loi normale.