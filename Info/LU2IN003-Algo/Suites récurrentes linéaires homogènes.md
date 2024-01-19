#algo 
## Définition
On définit une suite récurrente linéaire homogène comme une suite d'élément sur $\mathbb{N}$ telle que
$$\forall n \geq 2, u_n = au_{n-1} + bu_{n-2}$$ Où $(a,b) \in \mathbb{R}^2$
Remarquons que la suite de Fibonacci est une suite récurrente linéaire homogène

## Polynôme caractéristique
On détermine le polynôme caractéristique d'une telle suite
$$P(r) = r^2 - ar - b $$

Avec $r$ la racine de ce polynôme. La suite $r^n$ satisfait $\forall n \geq 2$ la relation de récurrence $u_n = r^n$
### Preuve
$$r^n = r^{n-2} \times r^2 = r^{(n-2)}(ar - b)$$
Ainsi par exemple, pour la suite de Fibonacci, le polynôme caractéristique