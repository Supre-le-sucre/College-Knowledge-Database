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

- Méthode du triangle à droite $$
\int_{0}^{1}f(x)dx = \lambda_{1}f(1)
$$Avec $\lambda_{1}$ choisi pour être exact avec toute fonction constante (donc $\lambda_{1} = 1$)

- Méthode du point milieu
$$
\int_{0}^{1}f(x)dx = \lambda_{1}f\left( \frac{1}{2} \right)
$$
Cette méthode est par ailleurs exact pour tout polynôme de degré 1 ou inférieur
