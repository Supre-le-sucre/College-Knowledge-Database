# Définition
Pour $E$ et $F$ deux espaces vectoriels. On dit que $f: E \to F$ est différentiable au point $a$ si et seulement si: #!

Il existe application linéaire $L_{a} \in \mathcal L(E, F)$ tel que $$
f(a+h) = f(a) + L_{a}(h) + o(h)
$$
On dit alors que $L_{a}$ est le différentielle de $f$ au point $a$ et on note souvent $L_{a} = D_{f}(a)$

**Exemple**:
Pour $f(x, y) = xe^{3y}$ a-t-on $f$ différentiable au point $(2, 1)$
On évalue donc la fonction avec
$$f(2 + h_{1}, 1 + h_{2}) = (2+h_{1})e^{3(1+h_{2})} = (2+h_{1})e^3\times e^{3h_{2}}$$
En effectuant un développement limité 