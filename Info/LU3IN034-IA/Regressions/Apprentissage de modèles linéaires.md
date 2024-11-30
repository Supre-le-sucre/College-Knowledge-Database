Le problème est d'établir un modèle linéaire $$
y = \beta_{0} + \beta_{1}x_{1} + \cdots + \beta_{p}x_{p} 
$$
Pour lequel, les coefficient $\beta$ ne sont pas connus, mais dont on a des informations un ensemble de $n > p$ observations.
Si on détermine $\beta$, on aura alors un moyen de prédire le résultat $y$ pour toutes valeurs de $x$

Il y a plusieurs manière de résoudre ce problème. On s'attends déjà à minimiser l'erreur:
$$
\min_{\beta} ||Y -X\beta||
$$
On peut déterminer $||\cdot||$ de plusieurs façon différentes:
- Le critère de moindre carré, ou on prends la norme carré
$$
\sum_{i=1}^{p}\left( y_{i} -\sum_{j=0}^{p}\beta_{j}x_{ij}  \right)^2
$$
Dans ce cas $\beta$ est résolu par optimisation convexe

- Le critère de LAD qui prends la norme de Manhattan
$$
\sum_{i=1}^{p}\left| y_{i} -\sum_{j=0}^{p}\beta_{j}x_{ij}  \right|
$$
Dans ce cas $\beta$ est obtenu par [[Problème Linéaire d'optimisation|programmation linéaire]]
