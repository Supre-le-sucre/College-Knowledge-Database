Considérons le problème de décision suivant
- Un ensemble d'était $S$
- Un ensemble fini de conséquence $X = \{ x_{1}, \dots, x_{m} \}$
- Des actes $X^{S}$
- Une préférence globale, c'est à dire, une relation d'ordre entre les actes

# Critère de Wald
Le critère de Wald repose sur le principe de prudence.
Elle consiste à choisir l'acte dont la pire conséquence est la meilleure, soit
$$
\arg\max_{f \in X^{S}}\left(\min_{s \in S} f(s)\right)
$$
Le problème de ce critère, c'est qu'il pousse souvent à l'inaction (ne rien gagner est toujours mieux que de risquer de perdre)

## Exemples
![[Pasted image 20241208223129.png]]
On choisit ici $f_{3}$

![[Pasted image 20241208223209.png]]
On choisit ici $f_{2}$

# Critère de Hurwicz
Le critère de Hurwicz cherche à trouver un compromis entre une décision prudente et optimiste.

Elle consiste à choisir l'acte ayant le meilleur compromis entre la meilleure et la pire conséquence. Ce compromis est modélisé par le facteur $\alpha \in [0, 1]$ tel que
$$
\arg \max_{f \in X^S} \left(\alpha \min_{s \in S} f(s) + (1-\alpha) \max_{s \in S} f(s) \right) 
$$
Si $\alpha$ est proche $1$, alors le choix est *prudent*, si $\alpha$ est proche de $0$ alors le choix est *optimiste*

## Exemple
L'exemple ci-dessous témoigne de la limite de ce critère
![[Pasted image 20241208223645.png]]
En effet, ici, les deux actes se valent, mais l'acte $f_{1}$ sera préféré à $f_{2}$ car la pire conséquence de ce dernier est plus mauvaise que $f_{1}$

# Critère min-max regret
Ce critère consiste à minimiser le regret, c'est en général celui le plus utilisé
On qualifie de regret la fonction $R: X^{S} \times S \to \mathbb R$ de la forme $R(f, s)$qui renvoie le plus grand regret que l'on pourrait avoir en choisissant l'acte $f$ à l'état $s$ soit
$$
R(f, s) = \max_{g \in X^{S}} (g(s) - f(s))
$$

Le critère de min-max regret est alors donné par
$$
\arg \min_{f \in X ^S} \max_{s \in S} R(f, s)
$$

## Exemple
![[Pasted image 20241208224153.png]]
Le tableau des actes est indiqué à gauche, celui des regrets à droite.
On va ici choisir l'acte $f_{3}$ car le regret est minimal.

# Critère de Laplace
L'idée de ce critère est de lever l'incertain en supposant que tous les éléments sont équiprobable.
On choisit donc l'acte ayant la conséquence moyenne la plus élevé
$$
\arg \max_{ f \in X^S} \sum_{s \in S} \frac{1}{|S|}f(s)
$$
Ce critère est souvent inapproprié, étant donné que l'incertain est bien trop souvent non équiprobable