#lebesgue 
# Théorème de la continuité sous domination
On définit le théorème comme suit: #!

Si on réunit les assertions suivantes
1. $\forall t \in \Lambda, x \mapsto f(t,x)$ est intégrable
2. Pour presque tout $x \in A, t \mapsto f(t,x)$ est continue
3. $\exists g \in L^1(A, \mathbb R^+)$ telle que $\forall t, \forall x |f(t,x)| \leq g(x)$
Alors on a que $$t \mapsto F(t) = \int_Af(t,x)dx \text{ continue sur } \Lambda$$
<!--ID: 1710449411679-->


# Théorème de la dérivabilité sous domination
On définit le théorème comme suit: #!

Soit $\Lambda$ un intervalle de $\mathbb R$ avec les assertions suivantes réunies:
1. $\forall t \in \Lambda, x \mapsto f(t,x)$ est intégrable sur $\Lambda$ 
2. Pour presque tout $x \in A, t \mapsto f(t,x)$ est dérivable sur $\Lambda$
3. $\exists g \in L^1(A, \mathbb R^+)$ telle que pour presque tout $t, x |\frac{\partial{f}}{\partial{t}}(t,x)| \leq g(x)$ 
Alors on a que $$t \mapsto F(t) = \int_Af(t,x)dx \text{ est derivable et } F'(t) = \int_A \frac{\partial{f}}{\partial{t}}(t,x)dx$$
<!--ID: 1710449411685-->


