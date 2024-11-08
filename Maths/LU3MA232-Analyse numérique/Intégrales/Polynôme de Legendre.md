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
$$\left\langle \frac{(2n)!}{n!} Q_{n}, \frac{(2m)!}{m!}Q_{m}\right\rangle = \int_{-1}^1 \left(   \left( x^2 -1 \right)^n\right)^{(n)}\left(   \left( x^2 -1 \right)^m\right)^{(m)} dx = I_{m,n}$$

On effectue alors $m+1$ intégrations par partie
Pour la première on a que $$
I_{m,n}= \left[ \left(   \left( x^2 -1 \right)^n\right)^{(n-1)}  \left(\left( x^2 -1 \right)^m\right)^{(m)} \right]_{-1}^1 - \int_{-1}^1 \left(   \left( x^2 -1 \right)^m\right)^{(m+1)} \left(   \left( x^2 -1 \right)^n\right)^{(n-1)}   
$$
Or $$
\left[ \left(   \left( x^2 -1 \right)^n\right)^{(n-1)}  \left(\left( x^2 -1 \right)^m\right)^{(m)} \right]_{-1}^1 = 0
$$
Car $-1$ et $1$ sont les racines de multiplicités $1$ d'un tel polynôme
Et donc en continuant
$$- \int_{-1}^1 \left(   \left( x^2 -1 \right)^m\right)^{(m+1)} \left(   \left( x^2 -1 \right)^n\right)^{(n-1)}  = \int_{-1}^1 \left(   \left( x^2 -1 \right)^m\right)^{(m+2)} \left(   \left( x^2 -1 \right)^n\right)^{(n-2)} \cdots  $$
D'où finalement
$$
I_{{m,n}} = (-1)^{m+1} \int_{-1}^1 \left(   \left( x^2 -1 \right)^m\right)^{(2m+1)} \left(   \left( x^2 -1 \right)^n\right)^{(n-m-1)}dx
$$
Or $\left(   \left( x^2 -1 \right)^m\right)^{(2m+1)} = 0$ car dérivée une fois de plus que son degré et $n-m-1 \geq 0$
Donc $I_{m,n} = 0$

On a donc bien $P_{n} = Q_{n}$

## Racines de $P_{n}$
On observe que: #!

Le polynôme $P_{n}$ admet $n$ racines simples, toutes situés dans $]-1, 1[$

### Preuve
Montrons un résultat plus général

#### Lemme
Soit $0 \leq k \leq n$ alors 