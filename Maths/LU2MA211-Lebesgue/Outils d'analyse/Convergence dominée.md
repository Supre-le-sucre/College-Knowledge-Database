# Théorème
Le théorème de convergence dominée, plus fort que [[Beppo-Levi]] peut s'énoncer comme suit: #!

Soit $(f_n)_{n \in \mathbb N}$ une suite de foncions intégrables sur $A$ et tel que
- $f_n \to f$ presque partout
- $\exists g$  intégrable positive et telle que: $\forall n \in \mathbb N |f_n| \leq g$
Alors $f$ est intégrable et on a en particulier: $$\lim_{n \to +\infty}\int_Af_n(x) = \int_A f(x)dx$$ et aussi que: $\int |f_n -f| \to 0$. On dit alors que $g$ domine $f_n$ ou est chapeau intégrable de $f_n$
<!--ID: 1710447314064-->
