## Définition
Soit $f: \Omega \to \mathbb{R}^p$ et $f: x \mapsto (f_{1}(x), \dots, f_{{n}}(x))$ et $a \in \Omega$ on dit que $f$ admet une dérivée partielle au point $a$ à la $i$ ème variable si et seulement si: #!

La fonction $t \mapsto f(a+te_{i})$, où $e_{i}$ le $i$ ème vecteur de la base canonique de l'espace $\Omega$, est [[Différentiabilité|différentiable]] en $0$. On note cette dérivée $$\frac{\partial f}{\partial x_{i}}(a) = \lim_{ t \to 0} \frac{f(a+te_{i})-f(a)}{t}$$

## Proposition sur la différentiabilité
Soit $f: \Omega \to \mathbb{R}^p$ et $a \in \Omega$ tel que $f$ est différentiable au point $a$ alors dans ce cas: #!

La différentielle est donnée par $D_{f}(a)(e_{i}) = \frac{\partial f}{\partial x_{i}}(a)$, la représentation matricielle de $D_{f}(a)$ dans la base canonique est donc donnée par $J_{f}(a)$ appelé jacobienne de $f$ au point $a$.