## Définition
Soit $(X, d_X)$ et $(Y, d_Y)$ et $f:(X, d_X) \to (Y, d_Y)$, on dit que $f$ est continue en $x_o \in X$ si et seulement si: #!

$$\forall \epsilon > 0, \exists\eta >0, d_X(x_0, x)< \eta \implies d_Y(f(x_0), f(x)) < \epsilon$$

## Proposition sur les ouverts et la continuité
Soit $f: X \to Y$ avec $(X, d_X)$ et $(Y, d_Y)$ on observe que: #!

$f$ est continue sur $X$ si et seulement si $$\forall O \subseteq Y \text{ un ouvert}, f^{-1}(O) \text{ est aussi un ouvert}$$
### Preuve
$\Rightarrow$: Supposons $f$ continue

Soit $O$ un ouvert de $Y$, montrons que $f^{-1}(O)$ est un ouvert de $X$
Soit $x  \in f^{-1}(O)$, montrons que $\exists \eta > 0$ tel que $B(x, \eta) \subseteq f^{-1}(O)$

On sait par hypothèse que $f(x) \in O$
Comme $O$ est un ouvert, alors $\exists \epsilon > 0,  B(f(x), \epsilon) \subseteq O$
De plus étant donné que $f$ est continue, $\exists \eta > 0$ tel que $y \in B(x, \eta) \implies f(y) \in B(f(x), \epsilon)$

