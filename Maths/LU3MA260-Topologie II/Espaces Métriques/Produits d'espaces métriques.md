## Propriété de distances équivalente
On se donne 2 espaces métriques $(X, d_X), (Y, d_Y)$ et on considère $X \times Y$
Alors les 3 distances sur cette espace sont équivalentes: #!

$$d_1((x,y), (x', y')) = d_X(x, x') + d_Y(y, y')$$ $$d_2((x,y), (x', y')) = \sqrt{(d_X(x,x'))^2 + d_Y(y, y')^2}$$ $$d_\infty((x,y), (x',y')) = \sup(d_X(x,x'), d_Y(y,y'))$$
### Preuve
L'équivalence est maintenue dans le produit cartésien, d'où
$$d_\infty(x,y) \leq d_2(x,y) \leq d_1(x,y) \leq \sqrt 2 d_2(x,y) \leq 2d_\infty(x,y)$$