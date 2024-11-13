
## Politique stationnaire
On dit qu'une politique est *stationnaire* si et seulement si: #!

$$V_{d}(s) = R(s, d(s)) + \sum_{s' \in S}T(s,a)(s')V_{d,t-1} (s') \quad \quad \forall s \in S$$

## Théorème de Harvard
On énonce le théorème suivant: #!

Il existe une politique optimale stationnaire et elle est optimale pour tout été initiale. Sa valeur est donné par

$$V^*(s) = \max \left[R(s, d(s)) + \sum_{s' \in S}T(s,a)(s')V_{d,t-1} (s')\right] \quad \quad \forall s \in S$$


## Formulation vectorielle et approche itérative

$\forall s \in S$ posons $LV(s) = \max_{a \in  A}\left[ R(s, d(s)) + \sum_{s' \in S}T(s,a)(s')V(s')  \right]$
