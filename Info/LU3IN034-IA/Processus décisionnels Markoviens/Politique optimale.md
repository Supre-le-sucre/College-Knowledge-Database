## Valeur d'une politique
Une politique représente l'ensemble des décisions à chaque étape sur un horizon.
La valeur d'une politique en l'état $s$ à un instant $t$ se définit de la façon suivante correspond à l'**espérance de la récompense** à une certaine étape de décision

En posant l'état $1$ comme la dernière décision (elle est facile à choisir, car il n'y a plus d'incertitude d'état comparé aux autres états)
- **Dernière décision** $$V_{d,1}(s) = R(s, d_{1}(s))$$
- **Décision à l'étape t** $$V_{d,t}(s) = R(s, d_{t}(s)) + \sum_{s' \in S}T(s,a)(s')V_{d,t-1} (s')$$


## Première approche
On cherche à trouver une politique décisionnel capable de ==maximiser== la récompense. Pour établir une politique, on note $d^{*}$ la politique optimale avec $V^{*}$ sa valeur.

Pour calculer la politique optimale, on doit d'abord commencer par la dernière décision dans un horizon fini.

On pose alors
- Dernière décision dans un état $s$ 
$$
V_{1}^{*}(s) = \max_{a} R(s, a) \quad \quad d_{1}^* = \arg\max_{a}R(s, a)
$$
Autrement dit, on prends l'action avec la meilleur récompense.

- Décision à $t$ étapes de la fin (en posant un facteur de pondération $\gamma \in ]0, 1[$)
$$
V_{t}^{*}(s) = \max_{a} \left[ R(s, a) + \gamma \sum_{s' \in S} T(s, a)(s') V^{*}_{t-1}(s')\right] \quad \quad $$ $$
 d_{1}^* = \arg\max_{a}\left[ R(s, a) + \gamma \sum_{s' \in S} T(s, a)(s') V^{*}_{t-1}(s')\right]
$$
Autrement dit, on choisit l'action qui engendre la plus grande récompense, sachant l'espérance de la récompense à l'état suivant.


## Exemple
On considère une grille dans laquelle on place un robot.
