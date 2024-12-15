## Définition
On définit une méthode composite de quadrature de la façon suivante: #!

Soit $I$ une [[Méthode de quadrature]] dans l'intervalle $[0, 1]$, alors on parle de méthode composite lorsque on utilise la propriété de l'intégrale suivante $$
\int_{0}^{1}f(x)dx = \sum_{i=1}^{N} \int_{\frac{i-1}{n}}^{\frac{i}{N}} f(y)dy
$$Auquel cas on écrit donc 
$$
\int_{0}^{1}f(x)dx = \sum_{i=1}^N I_{\frac{i-1}{N}, \frac{i}{N}}(f)
$$
<!--ID: 1734268137929-->


## Méthode composite courante
En se basant sur les [[Méthode de quadrature#Méthodes classiques|méthodes de quadrature classiques]]

- Composite des rectangles à droites
$$
\frac{1}{N}\sum ^N_{i=1}f\left( \frac{i}{N} \right)
$$
- Point milieu
$$
\frac{1}{N}\sum ^N_{i=1}f\left( \frac{i-\frac{1}{2}}{N} \right)
$$

- Trapèzes
$$
\frac{1}{2N}\left(   f(0) + f(1) +\sum ^{N-1}_{i=1}f\left( \frac{i}{N} \right)\right)
$$

## Propriété de convergence des méthodes composites
On observe le phénomène suivant: #!

Pour une [[Méthode de quadrature]] $I$ subdivisé en $\frac{1}{N}$, la méthode de quadrature composite, converge en $\frac{1}{N^{k+1}}$ si $f$ est une fonction de classe $\mathcal C^{{k+1}}$
<!--ID: 1734268137931-->
