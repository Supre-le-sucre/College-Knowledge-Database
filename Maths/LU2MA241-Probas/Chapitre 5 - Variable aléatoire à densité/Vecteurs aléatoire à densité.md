## Définition
Un vecteur aléatoire $(X, Y)$ à valeurs dans $\mathbb R^2$ est dit *"absolument continu*" ou *"à densité"*, si: #!

Il existe une fonction $f_{X, Y}: \mathbb R^2 \to [0, +\infty[$ intégrable sur $\mathbb R^2$ telle que, pour tout intervalle $I, J$ de $\mathbb R$ on vérifie: $$\mathbb P((X, Y) \in I \times J) = \mathbb P(X \in I,\; Y\in J) = \int_{I \times J}f_{X, Y}(x,y)dxdy$$On appelle la fonction $f_{X,Y}$ la densité du vecteur aléatoire $(X, Y)$

## Loi uniforme multidimensionnel
En dimension deux, il est possible de déterminer $(X, Y) \sim \mathcal U(C)$ où $C$ un ensemble quelconque ayant pour densité: #!
$$f_{X, Y}(x,y) = \frac{1}{mes(C)}\mathbb 1_C(x,y)$$ 
## Densité jointe et marginale
Si $(X, Y)$ un vecteur aléatoire à densité de $\mathbb R^2$ de densité $f_{X, Y}$ on observe que: #!

Ses composantes $X$ et $Y$ sont aussi des variables aléatoires à densité, de densité: $$f_X(x) = \int_\mathbb Rf_{X,Y}(x,y)dy \text{ \;et\; }f_Y(y) = \int_\mathbb Rf_{X,Y}(x,y)dx$$Notons que $f_{X, Y}$ est communément appelée *"densité jointe"* de $X, Y$ et les densités $f_X$ et $f_Y$ sont appelées *"densité marginale"*

## Indépendance
Soit $(X, Y)$ un vecteur aléatoire absolument continu pour lequel on a: #!
$$f_{X, Y}(x,y) = f_X(x)f_Y(y)$$pour tout $(x,y) \in \mathbb R^2\setminus C$ où $C$ est un ensemble de mesure bidimensionnel nulle. Alors dans ce cas $X, Y$ sont des variables aléatoires indépendantes.

Réciproquement si $X, Y$ deux variables aléatoires à densité indépendantes, alors $(X, Y)$ admet la densité jointe: #!
$$f_{X, Y}(x, y) = f_X(x)f_Y(y)$$

## Densité de la somme des composantes
Soit $(X, Y)$ un vecteur aléatoire de densité $f_{X, Y}$. Alors la somme de ses composantes $X+Y$ est absolument continue et admet pour densité: #!
$$f_{X+Y} = \int_{\mathbb R}f_{X,Y}(x, z-x)dx = \int_\mathbb R f_{X, Y}(z-x, x)dx$$à condition que $x \mapsto f_{X,Y}(x, z-x)$ et $x \mapsto f_{X,Y}(z-x, x)$ soient intégrables sur $\mathbb R$

### Cas particulier d'indépendances
Soit $X$ et $Y$ deux variables aléatoires absolument continues indépendantes, de densité respective $f_X$ et $f_Y$. Alors la variable $X+Y$ est une variable aléatoire absolument continue de densité: #!
$$f_{X+Y}(z) = f_X*f_Y(z)=\int_\mathbb Rf_X(x)f_Y(z-x)dx = \int_ \mathbb R f_X(z-x)f_Y(x)dx$$
Où la fonction $f_X*f_Y$ est appelé [[Produit de convolution]] de $f_X$ et $f_Y$
