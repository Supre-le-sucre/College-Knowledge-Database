## Définition
On définit les polynôme de Legendre de la façon suivante: #!

En posant l'espace vectoriel des polynômes généré par $Vect(1, X, X^2, \dots, X^n)$ muni du produit scalaire $\langle P, Q \rangle = \int _{-1}^1P(x)Q(x) \, dx$ En appliquant le procédé d'[[Orthogonalisation de Gram-Schmidt]] on obtient une base composée de $P_{n}$ appelé polynôme de Legendre 

## Propriété
Les polynômes de Legendre sont toujours de la forme suivante: #!
$$
P_{n} = \frac{n!}{(2n)!} \left( \left( x^2-1 \right)^n  \right)^{(n)} 
$$

**Remarque** Les polynômes sont uniques à un scalaire près. Ces polynômes sont aussi orthogonaux et de degré $n$. C'est ce qui nous servirai pour le prouver
### Preuve
Pour la preuve on suppose que les $P_{n}$ sont unitaires
Montrons que $Q_{n} - P_{n} = 0$ en posant $Q_{n} = \frac{n!}{(2n)!} \left( \left( x^2-1 \right)^n  \right)^{(n)}$

Observons que $Q_{n}$ est bien de degré $n$ car le terme $(x^2 - 1)^n$ est de degré $2n$ mais elle est dérivée $n$ fois, et $2n - n =n$ d'où le degré $n$.

De plus $Q_{n}$ est unitaire. En effet
$$\left( x^2 -1 \right)^n = x^{2n} + (\dots \text{degré < 2n)}$$
$$
\left(   \left( x^2 -1 \right)^n\right)' = 2nx^{2n-1} + (\dots \text{degré < 2n-1)}
$$
Si on répète ça $n$ fois
$$\left(   \left( x^2 -1 \right)^n\right)^{(n)} = 2n(2n-1)\cdots (n+1)x^{n} + (\dots \text{degré < n)}$$
Ce qui est exactement
$$
\left(   \left( x^2 -1 \right)^n\right)^{(n)} = \frac{(2n)!}{n!}x^{n} + (\dots \text{degré < n)}
$$

Il reste maintenant à montrer que les $(Q_{n})_{n \in \mathbb{N}}$ sont orthogonaux entre eux.
Soit $m < n$