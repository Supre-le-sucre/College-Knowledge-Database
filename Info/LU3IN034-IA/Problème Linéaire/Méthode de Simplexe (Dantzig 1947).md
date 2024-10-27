L'algorithme de simplexe est utilisé pour résoudre des [[Problème Linéaire d'optimisation|programmes linéaires]]. Il consiste à se déplacer de sommet en sommet pour atteindre un **optimum**

## Variables d'écart
Dans la méthode simplexe, on introduit des variables d'écart comme suit: #!

Chacune de ces variables transforment les inégalités du problèmes en égalité. L'objectif étant de se déplacer de sommet en sommet voisins.

### Exemple
![[Pasted image 20241027175940.png]]

### Observations
Un problème ayant $m$ contraintes aura alors $m$ variables d'écarts et on a aussi que si le problèmes est composé de $(x_{1}, \dots, x_{n})$ variables, alors à chaque sommet: #!

Il y aura $n$ variables (d'écart ou non) qui seront nulles.

#### Exemple
![[Pasted image 20241027180309.png]]