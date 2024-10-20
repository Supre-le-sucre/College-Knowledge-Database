## Stabilité explicite
Un schéma numérique explicite est qualifié de stable si: #!

Il existe une constante $C$ indépendante de $N$ telle que pour toute suite de vecteurs $(\eta_n)_{0 \leq n \leq N}$ les suites $(y_n)_{0 \leq n \leq N}$ et $(z_n)_{0 \leq n \leq N}$ de $\mathbb R^m$ définie respectivement par
$$y_0 \in \mathbb R^m \text{ et } y_{n+1} = y_n + hF(t_n, y_n, h) \text{ pour } 0 \leq n \leq N-1$$ $$z_0 = \eta_0 -y_0 \text{ et } z_{n+1} = z_n + h F(t_n, z_n, h)  \text{ pour } 0 \leq n \leq N-1$$sont telle que
$$\max_{0 \leq n \leq N}||z_n-y_n|| \leq C\sum^N_{n=0}||\eta_n||$$On qualifie alors $C$ de constante de stabilité du schéma.

Autrement dit: un schéma est stable si pour une perturbation $\eta_n$, le schéma ne s'écarte de la solution qu'un d'un rapport dépendant de $C$ et du module de la perturbation $||\eta_n||$