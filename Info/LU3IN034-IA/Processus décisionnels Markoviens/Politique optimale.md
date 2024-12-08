## Première approche
On cherche à trouver une politique décisionnel capable de ==maximiser== la récompense. Pour établir une politique, on note $d^{*}$ la politique optimale avec $V^{*}$ sa valeur.

Pour calculer la politique optimale, on doit d'abord commencer par la dernière décision dans un horizon fini. En effet, la dernière action est facile à choisir, car il n'y a plus d'incertitude d'état.

On pose alors
- Dernière décision dans un état $s$ 
$$
V_{1}^{*}(s) = \max_{a} R(s, a) \quad \quad 
$$