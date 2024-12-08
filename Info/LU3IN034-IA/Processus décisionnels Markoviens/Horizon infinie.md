Dans un horizon infini, on considère un facteur d'actualisation $\gamma \in ]0, 1[$ (cf. [[Processus décisionnel Markovien]])
## Politique stationnaire
On dit qu'une politique est *stationnaire* si et seulement si: #!

$$V_{d, t}(s) = R(s, d(s)) + \gamma\sum_{s' \in S}T(s,a)(s')V_{d, t-1} (s') \quad \quad \forall s \in S$$
Autrement dit, une politique stationnaire, est une politique qui **ne dépend pas de la temporalité du problème**

## Théorème de Howard
On énonce le théorème suivant: #!

Il existe une politique stationnaire optimale pour tout état initial d'un problème d'horizon infini. Sa valeur est donné par le système (qui admet une solution unique) suivant
$$V^*(s) = \max_{a} \left[R(s, d(s)) + \gamma\sum_{s' \in S}T(s,a)(s')V^{*} (s')\right] \quad \quad \forall s \in S$$
Ce système d'équation est appelé: Equation de Bellman

# Formulation vectorielle et approche itérative

$\forall s \in S$ posons $$LV(s) = \max_{a \in  A}\left[ R(s, d(s)) + \gamma\sum_{s' \in S}T(s,a)(s')V(s')  \right]$$
$$LV = \max_{\pi} \left\{ R_{\pi} + \gamma T_{\pi}V \right\}$$
L'équation de Bellman devient $V = LV$

## Proposition sur la lipchitzianité de LV
Pour tout état $s$, on peut établir l'inégalité suivante
$$
||LV - LV'|| \leq \gamma ||V -V'||
$$


## Théorème du point fixe
Comme $LV$ est lipchitzienne, alors la suite définie par $V_{0} = 0$ et $V_{t} = LV_{t-1}$
est convergente vers $V^*$ tel que $V^* = LV^{*}$

## Borne de l'erreur (Williams et Baird)
Ainsi donc, on peut calculer jusqu'à $|V_{t-1}(s) - V_{t}(s)| < \varepsilon$ et obtenir une approximation de $V^*$
On aura en effet, une borne sur l'erreur tel que
$$\max_{s \in S} |V_{d(V(t))}(S) -V^*(S)| < 2 \varepsilon \frac{\gamma}{1 - \gamma}$$


# Formulation en [[Problème Linéaire d'optimisation|programmation linéaire]]

## Proposition
On observe que
$$
V \geq LV \implies V \geq V^{*}
$$

## Formulation du PL
Par rapport à la proposition précédente, on cherche donc à minimiser les $V$ tout en conserver l'inégalité du membre de gauche. D'où
$$
\begin{align*}
\min \sum_{s \in S} V(s) \\
\forall s \in S, V(s) \geq LV(s)
\end{align*}
$$
L'optimum du PL ci-dessus est alors $V^*$