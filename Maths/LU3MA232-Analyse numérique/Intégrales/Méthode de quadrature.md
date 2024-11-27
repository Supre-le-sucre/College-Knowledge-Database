## Définition
Une méthode de quadrature est une approximation de la forme: #!

$$
\int_{0}^{1}f(x)dx \approx \sum_{i=1}^{n} \lambda_{i}f(y_{i})
$$
Avec $y_{i}$ des réels distincts et $\lambda_{i}$ des réels appelés "poids"
Une méthode de quadrature fournies une méthode pour tout intégrale entre $a$ et $b$ en effectuant le changement de variable classique $x = ta + (1-t)b$ 

## Propriété
Etant données des points distincts $y_{1}, \cdots, y_{n}$, il existe un unique $\lambda \in \mathbb{R}^n$ tel que: #!

$$
\int_{0}^1f(x)dx=\sum_{i=1}^{n} \lambda_{i}f(y_{i})
$$

## Méthodes classiques
On distingue les méthodes de quadrature de base
