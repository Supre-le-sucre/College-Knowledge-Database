## Valeur d'une politique
Une [[Processus décisionnel Markovien#Politique|Politique]] représente l'ensemble des décisions à chaque étape sur un horizon.
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
 d_{t}^* = \arg\max_{a}\left[ R(s, a) + \gamma \sum_{s' \in S} T(s, a)(s') V^{*}_{t-1}(s')\right]
$$
Autrement dit, on choisit l'action qui engendre la plus grande récompense, sachant l'espérance de la récompense à l'état suivant.


## Exemple
On considère une grille dans laquelle on place un robot. La grille peut être obstruée, empêchant le robot de passer sur une case.

Le robot **peut choisir** de se déplacer **vers la droite ou vers le bas**. 
Si la case directement adjacente au robot est **obstruée**, il ne peut pas choisir ce déplacement. 

Le robot **ne peut pas choisir avec certitude sa trajectoire**, cela signifie donc, qu'il peut soit **avancer tout droit**, soit **partir en diagonal**.
La loi de déplacement change en fonction de l'obstruction comme suit:
![[Pasted image 20241208202615.png]]
Autrement dit:
Dans le premier cas, s'il n'y a pas d'obstruction, le robot ira **tout droit** dans **la direction souhaitée** (vers la droite ou vers le bas) dans **60% des cas**, mais il ira en **diagonale** (vers la droite ou vers le bas, cela dépendra de l'action choisie) dans **20% des cas**.

Si une seule case est obstruée sur le chemin choisi, il aura **70% de chance d'avancer tout droit**, et **30% de chance d'avancer en diagonal**.

Si les deux cases sont obstruées, le robot **avancera forcément dans la bonne direction**.

Le diagramme suivant représente l'état initial du robot.
![[Pasted image 20241208203810.png]]
Au bout de **3 décisions**, le robot sera récompensé s'il se trouve sur une **case marquée** d'un $G$
La récompense dépend de la case, elle est indiquée sur le coin supérieur gauche.
Les cases qui ne sont **pas marquées**, n'apporte **pas de récompense** (la récompense **est nulle**)

On représente le graphe de décision/hasard du problème comme suit.
![[Pasted image 20241208204132.png]]
Un **état** est marqué par un **nœud carré**, une **décision** par un **nœud circulaire**.
Les **espérances de gain** sont indiquée en bleu, au dessus de chaque nœud.

A chaque état, on voit qu'il existe un *arc* vers un nœud d'action. Cet arc représente l'action de se diriger *vers la droite ou vers le bas*. Parfois, il n'y a qu'un seul arc, c'est parce qu'il n'y a qu'une seule décision à prendre pour cet état.

La politique optimale est indiquée par les flèches jaunes. C'est à dire, qu'à chaque état, le meilleur choix est de suivre la direction indiquée par la flèche. 