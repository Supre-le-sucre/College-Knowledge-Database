## Théorème de la décomposition de Dunford
On énonce le théorème suivant: #!

Soit $u \in \mathcal L(E)$, on suppose $\mathcal X_u$ scindé, alors $u$ s'écrit de manière unique sur la forme: $$u=d+n$$ où $d$ est diagonalisable et $n$ est nilpotent, avec en particulier $dn = nd$. Enfin, on a $d$ et $n$ des polynômes en $u$

### Preuve
On commence d'abord par montrer l'existence. On décompose $E$ en les sous-espaces caractéristiques. Ceci est possible d'après le théorème de [[Polynôme caractéristique#Théorème de Cayley-Hamilton|Cayley-Hamilton]] et le [[Polynômes d'endomorphismes#Lemme des noyaux|lemme des noyaux]]:
$$E = \bigoplus_{i=1}^s \ker((u- \lambda_iId_E)^{m_i}) = \bigoplus_{k=1}^sF_k$$
Chaque $F_k$ est stable par $u$, en outre on a que:
$$u_{|F_k} = \lambda_kId_{F_k} + (u-\lambda_kId_E)_{|F_k}$$ avec par définition
$$(u-\lambda_kId_{F_k})_{|F_k}^{m_k} = 0$$ d'où la décomposition en diagonalisable plus nilpotent qui commute. On définit alors $d$ et $n$ par: $$\forall k \in [1,s ], d_k := d_{|F_k} = \lambda_kId_{F_k}, \; n_k = n_{|F_k} = u_{|F_k} - \lambda_kId_{F_k}$$
Sur chaque $F_k$ on a que $d_k$ et $n_k$ commutent, donc $d$ et $n$ commutent sur $E =\bigoplus_{k=1}^sF_k$

On a en plus que $d$ est diagonalisable car elle l'est pour chaque $F_k$ (cf. [[Espaces stables et codiagonalisation#Lemme Conséquence de la stabilité sur la diagonalisation|lemme]]) et $n$ nilpotent comme il l'est pour chaque $F_k$
Enfin 