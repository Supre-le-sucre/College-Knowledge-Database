Soit $\Pi(n), n \in \mathbb{N}$ un propriété à démontrer
## Récurrence faible

*Cas de base:* Montrer que pour un $k \in \mathbb{N}, \Pi(k)$ est vraie (généralement $k=0$)
*Induction:* Montrer que 
$$ \forall n \in \mathbb{N}, (\Pi(n) \Rightarrow \Pi(n+1)) $$
### Exemple
Montrer $\forall n \in \mathbb{N}, \Pi(n): \sum_{i=0}^n i = \frac{n(n+1)}{2}$

*Initialisation:*
$$ \sum_{i=0}^0 i = 0 = \frac{0(0+1)}{2}$$
On a donc que $\Pi(0)$ est vraie

*Hérédité:* Soit $n \in \mathbb{N}$ avec $\Pi(n)$ vraie
$$ \sum_{i=0}^{n+1} i = \sum_{i=0}^{n} i + (n+1) $$
Comme $\Pi(n)$ vraie, on a donc que
$$  \sum_{i=0}^{n+1} i = \frac{n(n+1)}{2} + (n+1)  = \frac{(n+1)(n+2)}{2}$$
donc $\Pi(n+1)$ est vraie

Par récurrence, on conclut
$$ \forall n \in \mathbb{N}, \sum^n_{i=0} i = \frac{n(n+1)}{2} $$


## Récurrence forte

*Cas de base:* Montrer que pour un $k \in \mathbb{N}, \Pi(k)$ est vraie (généralement $k=0$)
*Induction:* Montrer que
$$ \forall n_0 \geq k, (\forall n \leq n_0, \Pi(n)) \Rightarrow \Pi(n+1) $$
### Exemple
Montrer $\forall n \in \mathbb{N}, n \geq 2, \Pi(n):$ $n$ admet au moins un diviseur premier

*Initialisation:* 2 divise 2, et 2 est premier, donc 2 admet au moins un diviseur premier, $\Pi(2)$ est vraie

*Hérédité*
Soit $n \in \mathbb{N}$ tel que $\forall k \in [2, n], \Pi(k)$ vraie.
Montrons $\Pi(n+1)$ est vraie

Il existe 2 différents cas possible:
- Si $n+1$ est premier, comme il se divise lui même on a que $\Pi(n+1)$ est vraie
- Si $n$ n'est pas premier, alors par définition, il admet un autre diviseur $k \neq 1$ et $k \neq n$
	Ainsi donc, $k \in [2, n]$, or par $\Pi(k)$, on sait que $k$ admet un diviseur premier, ce diviseur premier divise donc aussi $n+1$, donc $\Pi(n+1)$ est vraie

Par récurrence on a que $\forall n \in \mathbb{N}, n \geq 2, \Pi(n)$ est vraie