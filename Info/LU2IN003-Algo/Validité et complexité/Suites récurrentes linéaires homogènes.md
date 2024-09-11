#algo 
## Définition
On définit une suite récurrente linéaire homogène comme une suite d'élément sur $\mathbb{N}$ telle que #!
$$\forall n \geq k, u_n = \lambda_1u_{n-1} + \lambda_2u_{n-2} + \cdots + \lambda_k u_{n-k}$$ Où $(\lambda_1, \cdots, \lambda_k) \in \mathbb{R}^k$
Remarquons que la suite de Fibonacci est une suite récurrente linéaire homogène
<!--ID: 1715690724092-->


## Polynôme caractéristique

On détermine une suite récurrente linéaire homogène d'ordre 2
On détermine le polynôme caractéristique d'une telle suite: #!
$$P(r) = r^2 - ar - b $$
<!--ID: 1715690724094-->


Il y a alors 2 cas:
### 2 racines
On a que $\forall r \in \mathbb{R}$
La relation de récurrence $\forall n \in \mathbb{N}, n \geq 2$ suivante
$v_n = r^n = av_{n-1} + bv_{n-2}$

La solution générale de la récurrence est de la forme
$$u_n = \alpha_1 r_1^n + \alpha_2 r_2^n$$
Avec $\alpha_1$ et $\alpha_2$ satisfaisant le système suivant
$$\begin{cases} 
      \alpha_1 + \alpha_2 = u_0\\
      r_1\alpha_1 + r_2\alpha_2 =u_1
   \end{cases}
$$

### 1 racine double
On a que $\forall r \in \mathbb{R}$
La relation de récurrence $\forall n \in \mathbb{N}, n \geq 2$ suivante
$v_n = nr^n = av_{n-1} + bv_{n-2}$

La solution générale de la récurrence est de la forme
$$u_n = r_1^n (\alpha_1+\alpha_2n)$$
Avec $\alpha_1$ et $\alpha_2$ satisfaisant le système suivant
$$\begin{cases} 
      \alpha_1 + \alpha_2 = u_0\\
      r_1(\alpha_1 + \alpha_2) =u_1
   \end{cases}
$$
