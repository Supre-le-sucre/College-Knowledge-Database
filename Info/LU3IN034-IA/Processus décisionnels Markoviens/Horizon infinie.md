
## Politique stationnaire
On dit qu'une politique est *stationnaire* si et seulement si: #!

$$V_{d}(s) = R(s, d(s)) + \sum_{s' \in S}T(s,a)(s')V_{d,t-1} (s') \quad \quad \forall s \in S$$

## Théorème de Harvard
On énonce le théorème suivant: #!

Il existe une politique optimale stationnaire et elle est optimale pour tout été initiale. Sa valeur est donné par

$$V^*(s) = \max \left[R(s, d(s)) + \sum_{s' \in S}T(s,a)(s')V_{d,t-1} (s')\right] \quad \quad \forall s \in S$$


## Formulation vectorielle et approche itérative

$\forall s \in S$ posons $LV(s) = \max_{a \in  A}\left[ R(s, d(s)) + \sum_{s' \in S}T(s,a)(s')V(s')  \right]$

Le vecteur $LV$ est alors obtenu avec chaque état du système Et on pose

$LV = \max \left\{ R_{\pi} + \gamma T_{\pi}V \right\}$
L'équation de Bellman devient $V = LV$


## Proposition j'ai abandonné là

$$
||LV - LV'|| \leq \gamma ||V -V'||
$$


## Proposition 2 la deuxième t'as capté
La suite est définie par $V_{0} = 0$ et $V_{t} = LV_{t-1}$

Si $|V_{t-1}(s) - V_{t}(s)| < \varepsilon$
Alors $\max_{s \in S} |V_{d(V(t))}(S) -V^*(S)| < 2 \varepsilon \frac{\gamma}{1 - \gamma}$