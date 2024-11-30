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

## Exemple où $p=1$
On souhaite faire l'apprentissage d'une droite d'équation $y = \beta_{0} + \beta_{1}x$ en fonction $n$ observations: $(x_{i}, y_{i})$
Donc on a l'objectif suivant
$$
\text{minimiser } \quad \sum_{i= 1}^n \left| y_{i} -\beta_{0} - \beta_{1}x_{
} \right| 
$$
En posant l'écart de l'observation $i$ tel que $$e_{i} = y_{i} - \beta_{0} -\beta_{1}x_{i}$$Cette valeur $e_{i}$ peut être positive ou négative.

Or il est possible de trouver deux nombres $u_{i}, v_{i}$ ==positifs ou nuls== tel que
$$
\begin{cases}
e_{i} &=& u_{i} - v_{i} \\
|e_{i}| & = & u_{i} + v_{i}
\end{cases}
$$
En effet en résolvant le système on a bien que
$$
\begin{cases}
e_{i} &=& u_{i} - v_{i} \\
|e_{i}| & = & u_{i} + v_{i}
\end{cases} \quad \Leftrightarrow \quad 
\begin{cases}
u_{i} &=&  \frac{|e_{i}|+e_{i}}{2} \\
v_{i} & = & \frac{|e_{i}|-e_{i}}{2}
\end{cases}
$$

Comme on cherche à minimiser $|e_{i}|$ on peut poser le programme linéaire suivant:
$$
\begin{align}
&\min |e_{i}| \\
e_{i} =\; & y_{i} - \beta_{0} -\beta_{1}x_{i}
\end{align}
$$
D'où, en posant cela avec $u_{i}$ et $v_{i}$ ==positive== on a
$$
\begin{align}
\min \sum_{i=1}^{n} (u_{i} + v_{i})  \\
u_{i} - v_{i} = y_{i} - \beta_{0} -\beta_{1}x_{i}
\end{align}
$$

## Régression linéaire multiple avec le critère LAD
Souvent $p > 1$, il faut donc trouver un critère viable en tout temps
Posons $n$ le nombre d'observations de la forme $(x_{i,1}, \cdots, x_{i,p}, y_{i})$

Cette fois-ci, observons que $|x| = \max(x, -x)$. On a donc que $|x|$ est le plus petit majorant entre $x$ et $-x$
Pour minimiser $|x|$ on peut poser $z=|x|$ avec 
$$
\begin{cases} 
\min z \\
z\geq x \\
z \geq -x
\end{cases}
$$
En posant l'écart de l'observation $i$ tel que $$e_{i} = y_{i} - \beta_{0} -\beta_{1}x_{i}$$
Et en étudiant sa valeur $|e_{i}|$ et $e_{i}$, on peut donc écrire la régression linéaire comme le PL de la forme suivante
$$
	\begin{cases}
	\end{cases}
$