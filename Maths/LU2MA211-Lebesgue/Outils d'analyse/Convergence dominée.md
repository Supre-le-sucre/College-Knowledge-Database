# Théorème
Le théorème de convergence dominée, plus fort que [[Beppo-Levi]] peut s'énoncer comme suit: #!

Soit $(f_n)_{n \in \mathbb N}$ une suite de foncions intégrables sur $A$ et tel que
- $f_n \to f$ presque partout
- $\exists g$  intégrable positive et telle que: $\forall n \in \mathbb N |f_n| \leq g$
Alors $f$ est intégrable et on a en particulier: $$\lim_{n \to +\infty}\int_Af_n(x) = \int_A f(x)dx$$ et aussi que: $\int |f_n -f| \to 0$. On dit alors que $g$ domine $f_n$ ou est chapeau intégrable de $f_n$
<!--ID: 1710447314064-->

## Corollaire Réduction sur un compact
Le théorème de convergence dominée nous permet de sortir un résultat important de convergence qui suit: #!

Soit $(A_n)_{n \in \mathbb N}$ une suite croissante de mesurables. On pose $A = \bigcup_{n \in \mathbb N}A_n$ 
Si $f \in \mathcal L^1(A)$ alors $$\lim_{n \to +\infty}\int_{A_n} f = \int_Af$$
<!--ID: 1710447577816-->

# Théorème de l'inversion $\int$ et $\sum$ 
On donne le théorème suivant: #!

Soit $A \subseteq \mathbb R^d$ mesurable et $(f_n)_{n \in \mathbb N}$ une suite de fonction mesurable tel que $\sum_{n=0}^{+\infty} \int_A |f_n| < +\infty$ alors on a $$\sum^{+\infty}_{n=0}$$ 