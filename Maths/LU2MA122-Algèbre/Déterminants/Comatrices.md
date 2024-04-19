## Définition
Soit $M \in M_n(A)$, on définit la comatrice de $M$ la matrice $Com(M)$ telle que: #!

$$\forall(i,j) \in [1,n]^2, Com(M)_{i,j} = (-1)^{i+j}M_{ij}$$
Où $M_{ij}$ est le déterminant de la matrice $M$ auquel on a retiré la ligne $i$ et la colonne $j$.
On appelle le nombre $(-1)^{i+j}M_{ij}$ le ==cofacteur== de $M$ d'indice $(i,j)$. La comatrice de $M$ est alors, plus sobrement, la matrice de ses cofacteurs.

## Transposition
On peut constater l'égalité suivante: #!
$$Com(^tM) = \:^tCom(M)$$

### Preuve
Cette propriété est triviale si l'on admets le [[Déterminant matriciel#Théorèmes sur le déterminant d'une matrice|2e point sur le théorème du déterminant]]: $det(A) = det(^tA)$. La transposition ne faisant qu'inverser les lignes et les colonnes.

## Théorème du développement du déterminant
On a les égalité suivante qui permettent de simplifier le calcul du déterminant: #!

Considérant $M_{ij}$ est le déterminant de la matrice $M$ auquel on a retiré la ligne $i$ et la colonne $j$.
1. Le développement par rapport à la j-eme colonne est tel que: $$\forall j \in [1,n], det(M) = \sum^n_{i=1}m_{i,j}M_{ij}$$
2. Le développement par rapport à la i-eme ligne est tel que: $$\forall i \in [1,n], det(M) = \sum^n_{j=1}m_{i,j}M_{ij}$$

### Preuve
On considère $(C_1, \dots, C_n)$ les colonnes de la matrice $M=(m_{i,j})$. Et considérons aussi une base canonique $(E_1, \dots, E_n)$ constitué de vecteurs de dimension $n$.

Pour un $k$ fixé, il est normal d'obtenir alors que $C_k = \sum^n_{i=1} m_{ik}E_i$, car $C_k$ est une combinaison linéaire dans la base $(E_1, \dots, E_n)$.
D'après la [[Multi linéarité du déterminant|n-linéarité du déterminant]] on a que:
$$\det(M) = \det(C_1, \dots, C_n) = \sum_{i=1}^nm_{ik}\det(C_1, \dots, C_{k-1}, E_i, C_{k+1}, \dots, C_n)$$

Soit la [[Cycle|permutation]] $\sigma = (1 \cdots k)$ de [[Signature]] $\epsilon(\sigma) = (-1)^{k-1}$. En appliquant $\sigma$ au déterminant, on a alors:
$$\det(C_1, \dots, C_{k-1}, E_i, C_{k+1}, \dots, C_n) = (-1)^{k-1}\det(E_i, C_1, \dots, C_{k-1}, C_{k+1}, \dots, C_n)$$

Observons maintenant les lignes. N'oublions pas l'égalité matricielle suivante:
$$(E_i, )$$
