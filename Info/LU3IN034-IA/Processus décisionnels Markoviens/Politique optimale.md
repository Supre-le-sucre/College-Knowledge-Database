## Valeur d'une politique
Une politique représente l'ensemble des décisions à chaque étape sur un horizon.
La valeur d'une politique en l'état $s$ à un instant $t$ se définit de la façon suivante correspond à l'**espérance de la récompense** à une certaine étape de décision

En posant l'état $1$ comme la dernière décision
- **Dernière décision** $$V_{d,1}(s) = R(s, d_{1}(s))$$
- **Décision à l'étape t** $$V_{d,t}(s) = R(s, d_{t}(s)) + \sum_{s' \in S}T(s,a)(s')V_{d,t-1} (s')$$


## Première approche
On cherche à trouver une politique décisionnel capable de ==maximiser== la récompense. Pour établir une politique, on note $d^{*}$ la politique optimale avec $V^{*}$ sa valeur.

Pour calculer la politique optimale, on doit d'abord commencer par la dernière décision dans un horizon fini. En effet, la dernière action est facile à choisir, car il n'y a plus d'incertitude d'état.

On pose alors
- Dernière décision dans un état $s$ 
$$
V_{1}^{*}(s) = \max_{a} R(s, a) \quad \quad 
$$