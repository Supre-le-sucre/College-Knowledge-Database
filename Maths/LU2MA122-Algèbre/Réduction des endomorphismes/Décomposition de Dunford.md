## Théorème de la décomposition de Dunford
On énonce le théorème suivant: #!

Soit $u \in \mathcal L(E)$, on suppose $\mathcal X_u$ scindé, alors $u$ s'écrit de manière unique sur la forme: $$u=d+n$$ où $d$ est diagonalisable et $n$ est nilpotent, avec en particulier $dn = nd$. Enfin, on a $d$ et $n$ des polynômes en $u$
<!--ID: 1715537862427-->


### Preuve
On commence d'abord par montrer l'existence. On décompose $E$ en les sous-espaces caractéristiques. Ceci est possible d'après le théorème de [[Polynôme caractéristique#Théorème de Cayley-Hamilton|Cayley-Hamilton]] et le [[Polynômes d'endomorphismes#Lemme des noyaux|lemme des noyaux]]:
$$E = \bigoplus_{i=1}^s \ker((u- \lambda_iId_E)^{m_i}) = \bigoplus_{k=1}^sF_k$$
Chaque $F_k$ est stable par $u$, en outre on a que:
$$u_{|F_k} = \lambda_kId_{F_k} + (u-\lambda_kId_E)_{|F_k}$$ avec par définition
$$(u-\lambda_kId_{F_k})_{|F_k}^{m_k} = 0$$ d'où la décomposition en diagonalisable plus nilpotent qui commute. On définit alors $d$ et $n$ par: $$\forall k \in [1,s ], d_k := d_{|F_k} = \lambda_kId_{F_k}, \; n_k = n_{|F_k} = u_{|F_k} - \lambda_kId_{F_k}$$
Sur chaque $F_k$ on a que $d_k$ et $n_k$ commutent, donc $d$ et $n$ commutent sur $E =\bigoplus_{k=1}^sF_k$

On a en plus que $d$ est diagonalisable car elle l'est pour chaque $F_k$ (cf. [[Espaces stables et codiagonalisation#Lemme Conséquence de la stabilité sur la diagonalisation|lemme]]) et $n$ nilpotent comme il l'est pour chaque $F_k$
Enfin d'après [[Polynômes d'endomorphismes#Corollaire|ce corollaire]] les projections sur les espaces caractéristiques sont des polynômes en $u$, on obtient que $d$ est donc un polynôme en $u$, mais $n$ également comme $u = d+n$

On montre enfin l'unicité
Supposons que l'on a $d+n = d'+n'$ alors $d-d' = n-n'$. Comme $f = d'+n'$ et que $d'$ et $n'$ commutent avec $f$, ils commutent donc avec $n$ et $d$ comme ils s'agit de polynôme en $f$.
Ainsi $d$ et $d'$ sont codiagonalisables d'après [[Espaces stables et codiagonalisation#Théorème de codiagonalisation|ce théorème là]] et $n, n'$ cotrigonalisable d'après [[Critère de trigonalisation#Théorème de cotrigonalisation|ce théorème ci]]. Ainsi $n-n' = d-d'$ est nilpotent est diagonalisable, donc nul d'après [[Diagonalisation#Corollaire conséquence de la nilpotence et de la diagonalisation|ce corrollaire]], ainsi $n=n'$ et $d=d'$
$$\tag*{$\blacksquare$}$$

### Corollaire sur les corps algébriquement clos
Le théorème de Dunford implique l'équivalence suivante: #!

Si $\mathbb K$ est algébriquement clos alors tout endomorphisme de $u \in \mathcal L(E)$ admet une décomposition de Dunford
<!--ID: 1715537862429-->


#### Preuve
Cela vient du fait que comme $\mathbb K$ est algébriquement clos, on a que $\mathcal X_u$ est scindé

### Corollaire de Jordan-Chevalley
On énonce le corollaire sur Dunford suivant: #!

Soit $\gamma \in GL(E)$ sur un corps $\mathbb K$ algébriquement clos, alors on a une décomposition unique: $\gamma = \gamma_s\gamma_u$ en diagonalisable et unipotent qui commutent
<!--ID: 1715537862431-->


#### Preuve
on fait la décomposition de Dunford: $\gamma = s + n$. Comme on a que $\gamma$ est inversible, on a que $s = \gamma - n$ est somme d'un inversible et d'un nilpotent qui commutent.
On a donc que $s$ est un inversible.

Posons alors que $\gamma_u = Id+s^{-1}n$, alors on a bien que $\gamma_u$ est bien unipotent comme on a que $s$ et $n$ commutent. Et il commutent à $s$ donc en posant $\gamma_s = s$ on obtient bien que $\gamma = \gamma_u\gamma_s$

Pour l'unicité, c'est analogue à la preuve de Dunford, en utilisant qu'une matrice diagonalisable et unipotent est l'identité, ainsi que le fait que $\gamma_u$ est aussi polynôme de $\gamma$ puisque $s^{-1}$ est un polynôme en $s$