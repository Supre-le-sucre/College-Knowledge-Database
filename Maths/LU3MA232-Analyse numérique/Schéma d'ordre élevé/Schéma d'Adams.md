## Schéma à pas multiples
Les schéma d'Adams sont des schéma à pas multiples c'est à dire que le schéma est de la forme: #!

Dans la cas explicite:
$$y_{n+1} = y_{n} + h F(t_{n}, y_{n-k}, y_{n-k+1}, \dots, y_{n}, h) $$
Dans le cas implicite:
$$
y_{n+1} = y_{n} + h F(t_{n}, y_{n-k}, y_{n-k+1}, \dots, y_{n}, y_{n+1},h) 
$$

## Définition du schéma d'Adams-Bashfourth 
On définit le schéma de la façon suivante: #!

$$
y_{n+1} = y_{n} + h \sum_{k=0}^{p-1} \alpha_{k}f(t_{n-k}, y_{n-k})
$$
Où $\alpha_{k}$ sont les poids tels que la méthode de quadrature $\int_{0}^1 \phi(u)du = \sum_{k=0}^{p-1} \alpha_{k} \phi(-k)$ soit d'ordre au moins $p-1$

**Remarque**: L'idée viens du fait que $y(t_{n+1}) = y(t_{n}) + \int_{t_{n}}^{t_{n+1}} y'(s)\, ds$ et que $y'(s)= f(s, y(s))$
Car dans ce cas, par changement de variable: $$
y(t_{n+1}) = y(t_{n}) +h \int_{0} ^1 f(t_{n} +hu, y(t_{n} + hu))du
$$

### Observations
On observe que
- Si $p=1$ alors cette méthode est la même qu'Euler explicite
- Si $p=2$ alors $$
y_{n+1} = y_{n} + \frac{3}{2}hf(t_{n}, y_{n}) -\frac{1}{2}hf(t_{n-1}, y_{n-1})
$$
	Il s'agit d'un schéma d'ordre $2$


## Théorème sur l'ordre du schéma d'Adams-Bashfourth 
On observe que: #!

Le schéma d'Adams-Bashfourth à $p$ est d'ordre $p$


## Schéma d'Adams-Moulton
On définit le schéma suivant: #!

$$
y_{n+1} = y_{n} +h \sum_{k=-1}^{p-2} \beta_{k}f(t_{n-k}, y_{n-k})
$$
Avec les $\beta$ les poids de la quadrature $\int_{0}^1 \phi(u)du = \sum_{k=-1}^{p-2} \beta_{k} \phi(-k)$ soit d'ordre au moins $p-1$

### Observations
On observe que
- Si $p=1$ alors cette méthode est la même qu'Euler implicite