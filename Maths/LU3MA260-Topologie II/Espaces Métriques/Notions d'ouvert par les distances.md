## Définition d'une distance
Pour $X$ un ensemble, on dit que $d: X^2 \to \mathbb R^+$ est une distance de $X$ lorsque:

- $d(x, y) = 0 \Leftrightarrow x=y$ (Séparation)
- $d(x,y) = d(y,x)$ (Symétrie)
- $d(x,y) \leq d(x, z) + d(z, y)$ (Inégalité triangulaire)
Le couple $(X, d)$ est alors qualifié d'espace métrique

## Boule ouverte
On définit une boule ouverte de centre $x$ de rayon $\epsilon$ sur un espace métrique $(X, d)$ tel que: #!
$$B(x, \epsilon) = \set{y \in X, d(x,y) < \epsilon}$$
## Ouvert
On dit que $O$ ouvert de $(X, d)$ si et seulement si: #!
$$\forall x \in O, \exists \epsilon > 0, B(x, \epsilon) \subseteq O$$

### Montrons que $B(y, \alpha)$ est un ouvert
On montre cela de la façon suivante: #!

Soit $x \in B(y, \alpha)$, Posons $\epsilon = \alpha - d(x,y) > 0$
Posons $z \in B(x, \epsilon)$ et on a que $$d(z, y) \leq d(z, x) + d(x,y) \leq \epsilon +d(x,y)$$ $$
d(z, y)\leq \alpha - d(x,y) +d(x, y) \leq \alpha$$
Donc $y \in B(y, \alpha)$
$$\tag*{$\blacksquare$}$$

## Intersection et union d'ouverts
Soit $(X,d)$ un espace métrique, alors: #!

- Une union finie ou infinie d'ouvert est un ouvert
- Une ==intersection finie== d'ouvert est un ouvert

### Preuve
Soit $(O_\lambda)_{\lambda \in \Lambda}$ des ouverts de $X$.

$O = \bigcup_{\lambda \in \Lambda}O_\lambda$ est un ouvert ?
Soit $x \in O$, alors $\exists \lambda \in \Lambda, x \in O_\lambda$. Et comme $O_\lambda$ est un ouvert, on a $B(x, \epsilon) \subseteq O_\lambda \subseteq O$

Soit $\Lambda$ un ensemble dénombrable fini, a-t-on $O = \bigcap_{\lambda \in \Lambda}O_\lambda$
Soit $x \in O$. Alors $\forall \lambda \in \Lambda$, $x \in O_\lambda$, et comme $O_\lambda$ est un ouvert on a que
$$\forall \lambda \in \Lambda, \exists \epsilon_\lambda > 0, B(x,  \epsilon_\lambda)$$