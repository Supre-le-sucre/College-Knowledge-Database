#probas 
## Définition
On dit que $X$ est une variable aléatoire discrète si $X:  \Omega \to E$ une application respectant les conditions suivantes:

1. $X(\Omega)$ est un ensemble dénombrable
2. $\forall a \in X(\Omega), \set{X=a} = \set{\omega \in \Omega, X(\omega)=a} \in \mathcal{F}$
## Opérations
### Espace produit
Soit $X_1, \cdots, X_n$ des variable aléatoires discrètes dans $E_1, \cdots, E_n$

Dans ce cas:
$Z : \Omega \to E_1 \times \cdots E_n$ tel que $\omega \mapsto (X_1(\omega), \cdots, X_n(\omega))$
est une variable aléatoire discrètes.

## Vocabulaire

- Pour chaque $X_i$, on a une [[Loi de X|loi]] $\mu_{X_i}$, appelée loi marginale sur $E_i$ et une [[Maths/LU2MA241-Probas/Densité discrète]] $p_{X_i}$ appelée densité discrète marginale
- Pour $Z$, en considérant [[Variables aléatoires discrètes#Espace produit|l'espace produit]]. On a une [[Loi de X|loi]] $\mu_{Z}$, appelée ==loi jointe== sur $E$ et une [[Maths/LU2MA241-Probas/Densité discrète]] $p_{Z}$ appelée ==densité jointe.==