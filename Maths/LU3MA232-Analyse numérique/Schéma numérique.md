
# Stabilité
## Stabilité explicite
Un schéma numérique explicite est qualifié de stable si: #!

Il existe une constante $C$ indépendante de $N$ telle que pour toute suite de vecteurs $(\eta_n)_{0 \leq n \leq N}$ les suites $(y_n)_{0 \leq n \leq N}$ et $(z_n)_{0 \leq n \leq N}$ de $\mathbb R^m$ définie respectivement par
$$y_0 \in \mathbb R^m \text{ et } y_{n+1} = y_n + hF(t_n, y_n, h) \text{ pour } 0 \leq n \leq N-1$$ $$z_0 = \eta_0 -y_0 \text{ et } z_{n+1} = z_n + h F(t_n, z_n, h)  \text{ pour } 0 \leq n \leq N-1$$sont telle que
$$\max_{0 \leq n \leq N}||z_n-y_n|| \leq C\sum^N_{n=0}||\eta_n||$$On qualifie alors $C$ de constante de stabilité du schéma.

Autrement dit: un schéma est stable si pour une perturbation $\eta_n$, le schéma ne s'écarte de la solution qu'un d'un rapport dépendant de $C$ et du module de la perturbation $||\eta_n||$

## Propriété sur la stabilité
On peut aussi prouver la stabilité d'un schéma d'une autre manière: #!

D'après le [[Lemme de Grönwall]]. Pour qu'un schéma soit stable, il faut que $F$ soit lipchitzienne par rapport à sa deuxième variable.
Pour le schéma explicite, cela implique qu'elle soit lipchitzienne sur $y_n$, pour le schéma implicite, qu'elle le soit sur $y_{n+1}$

# Consistance

## Erreur de consistance ou de discrétisation locale
On donne la définition suivante: #!

On appelle erreur de consistance ou de discrétisation locale du schéma la quantité $\epsilon_n \in \mathbb R^m$ définie par $$\epsilon_n  = y(t_{n+1}) -y(t_n) - hF(t_n, y(t_n), h)$$où $y$ est la solution de l'équation différentielle ordinaire.

## Consistance d'un schéma
On dit qu'un schéma est consistant avec l'équation différentielle ordinaire si: #!

Pour tout solution $y$, l'erreur de discrétisation $\epsilon_n$ est telle que
$$\lim_{h \to 0 } \sum_{n=0}^{N-1}||\epsilon_n|| = 0$$

## Propriété sur la consistance d'un schéma
pour montrer qu'un schéma est consistant, on peut aussi dire que: #!
$$F(t, y, 0) = f(t,y)$$
Pour un schéma implicite, on vérifie plutôt:
$$F(t, y, t,y, 0) = f(t,y)$$

# Théorème de Lax
On énonce le théorème suivant: #!

Un schéma stable et consistant est convergent

# Ordre d'un schéma

## Définition
On définit l'ordre d'un schéma comme suit: #!

Le schéma est dit d'ordre au moins $p \in \mathbb N^*$ si, pour tout solution $y$ de l'EDO, il existe une constante $C$ indépendante de $h$ telle que
$$\forall N, \sum_{n=0}^{N-1}||\epsilon_n|| \leq Ch^p$$==Il est donc d'ordre p s'il n'est pas d'ordre au moins p+1==

## Précision asymptotique d'un schéma par son ordre
On observe que pour un schéma stable d'ordre $p \geq 1$ #!

S'il existe $C$ une constante telle que $||y_0 - y(0)|| \leq C h^p$. Alors il existe $\tilde C > 0$ telle que
$$\max_{0 \leq n \leq N}||y(t_n) - y_n|| \leq \tilde Ch^p$$
Un schéma d'ordre $p' < p$ a donc une précision asymptotiquement inférieur au schéma d'ordre $p$ à pas égaux.

## Propriété sur l'ordre d'un schéma
On peut trouver l'ordre d'un schéma plus simplement: #!

Si pour tout solution $y$, il existe une constante $C'$ indépendant de $h$ telle que l'erreur de consistance du schéma vérifie: $$\forall n \leq N, ||\epsilon_n|| \leq C'h^{p+1}$$Alors le schéma est d'ordre ==au moins== $p$. Si de plus $\forall n \leq N$, on a que $||\epsilon_n|| \leq C''h^{p+1}$ avec $C''$ indépendante de $h$, alors le schéma est d'ordre $p$