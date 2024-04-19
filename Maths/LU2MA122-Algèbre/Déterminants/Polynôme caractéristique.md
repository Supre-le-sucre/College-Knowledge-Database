## Définition
Soit $M \in M_n(A)$, on considère le polynôme caractéristique de $M$ comme étant: #!
$$\mathcal X_M(X) = \det(XI_n-M)$$

## Proposition sur la forme du polynôme caractéristique
Soit $M\in M_n(A)$ alors $\mathcal X_M$ est unitaire de degré $n$ avec en particulier: #!
$$\mathcal X_M(X) = X^n - Tr(M)X^{n-1} + \cdots +(-1)^n\det(A)$$

## Proposition sur les valeurs propres de $M$
Soit $\mathbb K$ un corps et $M \in M_n(\mathbb K)$, alors $\lambda \in \mathbb K$ est une valeur propre de $M$: #!
si et seulement si $\lambda$ est une racine de $\mathcal X_M$. En particulier, $M$ admet donc au plus $n$ valeurs propres.

### Preuve
$\Rightarrow$
Si $\lambda \in \mathbb K$ est une valeur propre, alors il existe $x \in \mathbb K^n$ tel que $Mx = \lambda x$, soit alors:
$$Mx = \lambda x \Leftrightarrow Mx - \lambda x = 0 \Leftrightarrow (MId - \lambda Id)x =0 \Leftrightarrow (M - \lambda Id)x = 0$$
Ainsi donc on que:
$$\det((M-\lambda Id)x)  =0 \Leftrightarrow \det(M-\lambda Id)\det(x) =0$$
Puisque $x$ est un vecteur non nul, son déterminant est non nul. D'où finalement
$$\det(M -\lambda Id) = 0$$
Ceci implique que $\lambda$ est une racine de $\mathcal X_M$

$\Leftarrow$
Soit $\lambda$ une racine de $\mathcal X_M$ tel que, donc, $\det(M -\lambda Id) = 0$
On a alors que la matrice $M- \lambda Id$ n'est pas inversible