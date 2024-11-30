Le problème est d'établir un modèle linéaire $$
y = \beta_{0} + \beta_{1}x_{1} + \cdots + \beta_{p}x_{p} 
$$
Pour lequel, les coefficient $\beta$ ne sont pas connus, mais dont on a des informations un ensemble de $n > p$ observations.
Si on détermine $\beta$, on aura alors un moyen de prédire le résultat $y$ pour toutes valeurs de $x$

Il y a plusieurs manière de résoudre ce problème. On s'attends déjà à le faire avec une [[Problème Linéaire d'optimisation|programmation linéaire]] dans lequel on souhaite minimiser l'erreur:
$$
\min_{\beta} ||Y -X\beta||
$$

