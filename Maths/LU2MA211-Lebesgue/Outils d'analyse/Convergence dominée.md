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

Soit $A \subseteq \mathbb R^d$ mesurable et $(f_n)_{n \in \mathbb N}$ une suite de fonction mesurable tel que $\sum_{n=0}^{+\infty} \int_A |f_n| < +\infty$ alors on a $$\sum^{+\infty}_{n=0}\int_{A}f_n(t)dt = \int_{A}\sum^{+\infty}_{n=0}f_n(t)dt$$ 
<!--ID: 1710447988710-->

# Lien entre la convergence dominée et uniforme
On définit ce lien comme suit: #!

 $(f_n) \in \mathcal B(A, \mathbb C)^{\mathbb N}$ une suite de fonction bornée qui tend uniformément vers $f\in \mathcal B(A, \mathbb C)$ autrement dit $$\lim_{n \to +\infty}||f_n -f||_{\infty} = 0$$
 On alors que $$||f_n||_{\infty} \leq ||f_n-f||_{\infty} + ||f||_\infty$$ par inégalité triangulaire. D'où finalement, comme $f$ bornée:
 $$||f_n||_{\infty} \leq C$$
 Et donc la convergence dominée s'applique car $C$ intégrable sur un compact
<!--ID: 1710449391184-->
