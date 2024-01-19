#algo 
## Définition
On définit une suite récurrente linéaire homogène comme une suite d'élément sur $\mathbb{N}$ telle que
$$\forall n \geq 2, u_n = au_{n-1} + bu_{n-2}$$ Où $(a,b) \in \mathbb{R}^2$
Remarquons que la suite de Fibonacci est une suite récurrente linéaire homogène

## Polynôme caractéristique
On détermine le polynôme caractéristique d'une telle suite
$$P(r) = r^2 - ar - b $$

Avec $r$ la racine de ce polynôme. 
Il y a alors 2 cas:
### 2 racines
La solution générale de la récurrence est de la forme
$$u_n = \alpha_1 r_1^n + \alpha_2 r_2^n$$
Avec $\alpha_1$ et $\alpha_2$ satisfaisant le système suivant
$$\begin{cases} 
      \alpha_1 + \alpha_2 = u_0\\
      1 & x \in A 
   \end{cases}
$$

Ainsi par exemple, pour la suite de Fibonacci, le polynôme caractéristique