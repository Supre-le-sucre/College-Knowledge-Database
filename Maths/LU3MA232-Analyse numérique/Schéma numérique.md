## Stabilité explicite
Un schéma numérique explicite est qualifié de stable si: #!

Il existe une constante $C$ indépendante de $N$ telle que pour toute suite de vecteurs $(\eta_n)_{0 \leq n \leq N}$ les suites $(y_n)_{0 \leq n \leq N}$ et $(z_n)_{0 \leq n \leq N}$ de $\mathbb R^m$ définie respectivement par
$$y_0 \in \mathbb R^m \text{ et } y_{n+1} = y_n + hF(t_n, y_n, h) \text{ pour } 0 \leq n \leq N-1$$ $$z_0 = \eta_0 -y_0 \text{ et } z_{n+1} = z_n + h F(t_n, z_n, h)  \text{ pour } 0 \leq n \leq N-1$$sont telle que
$$\max_{0 \leq n \leq N}||z_n-y_n|| \leq C\sum^N_{n=0}||\eta_n||$$On qualifie alors $C$ de constante de stabilité du schéma.

Autrement dit: un schéma est stable si pour une perturbation $\eta_n$, le schéma ne s'écarte de la solution qu'un d'un rapport dépendant de $C$ et du module de la perturbation $||\eta_n||$

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


# Théorème de Lax
On énonce le théorème suivant: #!

Un schéma stable et consistant est convergent
