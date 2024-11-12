# Définition
Pour $E$ et $F$ deux espaces vectoriels. On dit que $f: E \to F$ est différentiable au point $a$ si et seulement si: #!

Il existe application linéaire $L_{a} \in \mathcal L(E, F)$ tel que $$
f(a+h) = f(a) + L_{a}(h) + o(h)
$$
On dit alors que $L_{a}$ est le différentielle de $f$ au point $a$ et on note souvent $L_{a} = D_{f}(a)$

## Exemple
### Générique

Pour $f(x, y) = xe^{3y}$ a-t-on $f$ différentiable au point $(2, 1)$
On évalue donc la fonction avec
$$f(2 + h_{1}, 1 + h_{2}) = (2+h_{1})e^{3(1+h_{2})} = (2+h_{1})e^3\times e^{3h_{2}}$$
En effectuant un développement limité d'exponentiel, alors on obtient
$$f(2+h_{1}, 1+h_{2}) = (2+h_{1})e^3 \times[1 + 3h_{2} + o(h_{2})]$$
En posant $h = (h_{1}, h_{2})$, On a $o(h_{1}h_{2}) = o(h)$
$$
f(2+h_{1}, 1+h_{2}) = 2e^3 +h_{1}e^3 + 6h_{2} e^3 + o(h)
$$
 En posant $D_{f}(a)(h) = h_{1}e^3 + 6h_{2}e^3$ on obtient bien
$$f(2+h_{1}, 1+h_{2}) = f(2, 1) + D_{f}(a)(h) + o(h)$$

### Matricielle
On s'intéresse cette fois à la différentielle de $f: H \in B(0, 1) \mapsto (I+H)^{-1}$