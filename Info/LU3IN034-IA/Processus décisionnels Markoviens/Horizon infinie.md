Dans un horizon infini, on considère un facteur d'actualisation $\gamma \in ]0, 1[$ (cf. [[Processus décisionnel Markovien]])
## Politique stationnaire
On dit qu'une politique est *stationnaire* si et seulement si: #!

$$V_{d, t}(s) = R(s, d(s)) + \gamma\sum_{s' \in S}T(s,a)(s')V_{d, t-1} (s') \quad \quad \forall s \in S$$
Autrement dit, une politique stationnaire, est une politique qui **ne dépend pas de la temporalité du problème**

## Théorème de Howard
On énonce le théorème suivant: #!

Il existe une politique stationnaire optimale pour tout état initial d'un problème d'horizon infini. Sa valeur est donné par le système (qui admet une solution unique) suivant
$$V^*(s) = \max_{a} \left[R(s, d(s)) + \sum_{s' \in S}T(s,a)(s')V^{*} (s')\right] \quad \quad \forall s \in S$$
Ce système d'équation est appelé: Equation de Bellman

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


## Propriété sur l'itération de la politique
Soit $\Pi$ une politique stationnaire de valeur $V_{\gamma}^\pi$. Alors toute politique $\pi'$ choisie dans
$$
\arg \max_{\gamma} \{ R_{\delta} + \gamma T_{\gamma}V_{\gamma}^\pi \}
$$
vérifie l'inégalité $V_{\gamma}^{\pi'} \geq V_{\gamma}^\pi$
