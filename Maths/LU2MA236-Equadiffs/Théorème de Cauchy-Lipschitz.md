# Solution maximale
On définit une solution maximale d'une EDO de la façon suivante: #!

Soit $x: I_x \to \mathbb R$ une solution à l'EDO $x' = f(t,x)$.
On dit que $x$ est solution maximale si, pour tout $y: J \to \mathbb R$ une autre solution de l'EDO et telle que $I_x \subseteq J$ et $x = y_{|I_x}$ alors on a que $I_x = J$
<!--ID: 1718736687580-->


# Théorème de Cauchy-Lipschitz
On énonce le théorème suivant: #!

Supposons $f: I \times U \to \mathbb R^d$ de classe $\mathcal C^1$.
Alors pour tout $(t_0, x_0) \in I \times U$ il existe ==une unique== solution maximale $x: I_x \to \mathbb R$ qui répond au problème de Cauchy: $$\begin{cases} x' = f(t,x) \\ x(t_0) = x_0\end{cases}$$De plus, toute solution non maximale au même problème de Cauchy est une restriction de la solution maximale sur un intervalle inclus sur $I_x$
<!--ID: 1718736687582-->


## Corollaire
Par le théorème de Cauchy-Lipschitz, on obtient l'observation suivante: #!

Les graphes des solutions maximales forment une partition de $I \times U$, car toutes les solutions doivent être disjointes.
<!--ID: 1718736687584-->

