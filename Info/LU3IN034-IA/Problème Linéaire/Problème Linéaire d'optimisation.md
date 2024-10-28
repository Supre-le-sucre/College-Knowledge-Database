Etant donné un ensemble de variables, on souhaite affecter des valeurs réelles qui satisfont les contraintes linéaires et maximise ou minimise un objectif linéaire

## Définitions en programmation linéaire
On donne les mots de vocabulaire suivante sur un programme linéaire: #!

- Une **fonction objectif linéaire**: est la fonction sur les variables $x_{1}, \dots, x_{n}$ qui doit être maximisée ou minimisée
- Il est constitué d'un ensemble de **contraintes linéaires** sur les variables $x_{1}, \dots, x_{n}$ qui doivent être satisfaites
- Une **équation linéaire** (donc une contrainte par égalité) impliquant les $x_{i}$ définit un **hyperplan** (une ligne avec 2 variables, un plan avec 3 variables…)
- Une **inégalité linéaire** constitue quant à lui **demi-espace**
- La **région réalisable** est l'intersection de tous les demi-espaces et/ou hyperplans, il forme un **polyèdre convexe**. S'il est borné et non vide, on dit alors que c'est un **polytope**
- Un **sommet** est l'unique point sur lequel se rencontrent un sous-ensemble d'hyperplans. Il est caractérisée par $n$ inégalités
- Deux sommets sont dis **voisins** s'ils partagent $n-1$ inégalités communes dans leur définition
Notons que ces définitions ont un aspect très géométrique. En effet, les programmes linéaires simples peuvent être facilement assimilé à des problèmes géométriques évidents
<!--ID: 1730114115905-->


## Forme standard d'un programme linéaire
En cherchant les variables $(x_{1}, \dots, x_{n})$ on obtient alors deux types de programme linéaire: #!

- Les programmes de maximisation $$\begin{cases}
\max(c_{1}x_{1} + \dots + c_{n}x_{n})  \\ \\
\sum_{j=1}^n a_{ij}x_{j} \leq b_{j} & i = 1,2,\dots, m \\ \\
x_{j} \geq 0 & j= 1, 2, \dots, n 
\end{cases}$$
- Les programmes de minimisation $$\begin{cases}
\min(c_{1}x_{1} + \dots + c_{n}x_{n})  \\ \\
\sum_{j=1}^n a_{ij}x_{j} \leq b_{j} & i = 1,2,\dots, m \\ \\
x_{j} \geq 0 & j= 1, 2, \dots, n 
\end{cases}$$Notons alors la tournure matricielle que peuvent avoir ces problèmes. Cela nous permettra de les résoudre plus simplement ultérieurement.
<!--ID: 1730114115907-->


## Observations rudimentaire
On observe que dans un programme linéaire: #!

- L'**optimum** que l'on cherche est un sommet de la région réalisable
- Si la ligne de maximisation ou minimisation est parallèle à une contrainte, il existe alors plusieurs points **optimaux**
- Dans la région réalisable, il n'y a qu'un nombre de sommets finis
Ces observations rencontrent des exceptions:
- Si le programme linéaire est irréalisable (des contraintes sont contradictoires) 
- Si la région réalisable n'est pas bornée (les contraintes ne suffisent pas pour borner la région)
<!--ID: 1730114115909-->

