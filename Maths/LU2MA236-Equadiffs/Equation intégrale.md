
# Propriété de la solution: équation intégrale
Soit le problème de Cauchy suivant: $$\begin{cases} x' = f(t,x) \\ x(t_0) = x_0\end{cases}$$On observe l'équivalence suivante, pour $x: I \to \mathbb R$ continue: #!
$$x \text{ est solution du problème} \Leftrightarrow \forall t\in I, \; x(t) =x_0+\int_{t_0}^tf(s,x(s))$$
<!--ID: 1719330123167-->


# Algorithme d'Emile Picard
Soit le problème de Cauchy suivant: $$\begin{cases} y' = f(t,y) \\ y(t_0) = y_0\end{cases}$$
On définit par récurrence la suite de fonction $(x_n)_{n \in \mathbb N}$ avec $x_n : I \to \mathbb R$: #!
$$x_0  = \begin{cases} I \to \mathbb R \\ t \mapsto y_0\end{cases}$$Autrement dit, $x_0$ est la fonction constante qui correspond à la valeur initiale. Et ensuite,
$$\forall t \in I, \; x_{n+1}(t) = x_0(t) + \int_{t_0}^tf(s, x_n(s))$$Si cette suite de fonction converge, le passage à la limite vérifie, l'[[#Propriété de la solution équation inétagrale|équation intégrale]] et donc le problème de Cauchy.
<!--ID: 1719330123171-->
