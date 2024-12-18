## Définition
Une méthode de quadrature est une approximation de la forme: #!

$$
\int_{0}^{1}f(x)dx \approx \sum_{i=1}^{n} \lambda_{i}f(y_{i})
$$
Avec $y_{i}$ des réels distincts et $\lambda_{i}$ des réels appelés "poids"
Une méthode de quadrature fournies une méthode pour tout intégrale entre $a$ et $b$ en effectuant le changement de variable classique $x = ta + (1-t)b$ 
<!--ID: 1734268137915-->


## Propriété
Etant données des points distincts $y_{1}, \cdots, y_{n}$, il existe un unique $\lambda \in \mathbb{R}^n$ tel que: #!

$$
\int_{0}^1f(x)dx=\sum_{i=1}^{n} \lambda_{i}f(y_{i})
$$
<!--ID: 1734268137917-->


## Méthodes classiques
On distingue les méthodes de quadrature de base

- Méthode du triangle à droite $$
\int_{0}^{1}f(x)dx = \lambda_{1}f(1)
$$Avec $\lambda_{1}$ choisi pour être exact avec toute fonction constante (donc $\lambda_{1} = 1$)

- Méthode du point milieu
$$
\int_{0}^{1}f(x)dx = \lambda_{1}f\left( \frac{1}{2} \right)
$$
Cette méthode est par ailleurs exact pour tout polynôme de degré 1 ou inférieur (et $\lambda_{1} = 1$)

- Méthode des trapèzes $$
\int _{0}^{1}f(x)dx = \lambda f(0)+\mu f(1)
$$Cette méthode est exacte pour les polynôme de degré 1 (et $\lambda = \mu = \frac{1}{2}$)

# Ordre d'une méthode de quadrature

## Définition
Une méthode de quadrature est dit ==au moins== d'ordre $k$ si et seulement si: #!

Elle est exacte pour les polynômes de degré $\leq k$
<!--ID: 1734268137919-->



## Caractérisation de l'erreur d'une méthode de quadrature
Si $I$ est une méthode de quadrature d'ordre $k$, alors il existe $c > 0$ telle que pour tout $f$ de classe $\mathcal C^{k+1}$, on ait: #!

$$
\left| \int_{0}^{1}f(x)dx - I(f) \right| \leq c \sup_{[0,1]}\left| f^{k+1} \right| 
$$
<!--ID: 1734268137922-->


## Généralisation de la caractérisation de l'erreur
Si $I$ est une méthode de quadrature d'ordre $k$ sur $[0,1]$, alors il existe $c > 0$ telle que pour tout $f$ de classe $\mathcal C^{k+1}$, on ait: #!

$$
\left| \int_{a}^{b}f(x)dx - I_{a,b}(f) \right| \leq c (b-a)^{k+2}\sup_{[a,b]}\left| f^{k+1} \right| 
$$
Cette propriété est bien utile, notamment quand il s'agit de décomposer les intervalles en subdivision plus petites, pour maximiser la précision
<!--ID: 1734268137924-->



## Corollaire sur la généralisation de l'erreur


# Méthode de Newton-Cotes
On donne la méthode suivante: #!

En posant $y_{i} = \frac{i}{n}$, la méthode de quadrature associé au poids tels qu'elle soit bien définie pour des polynôme de degré $n-1$, la méthode est d'ordre $n$ si $n$ est impair et $n+1$ si $n$ ets impair 
<!--ID: 1734268137925-->


## Corollaire
Comme la méthode de Newton-Cotes noté $J_{n}$ reviens à considérer les subdivisions de fermé sur $[a,b]$ alors on a que: #!

$$
\left| \int_{a}^{b} f(x) - J_{n}(f) \right| \leq 2\left( \frac{b-a}{n} \right) ^{{n+1}}\sup_{[a,b]} |f^{(n+1)}|
$$
<!--ID: 1734268137927-->
