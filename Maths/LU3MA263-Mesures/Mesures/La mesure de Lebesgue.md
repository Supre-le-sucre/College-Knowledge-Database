## Théorème de l'unicité
Pour la mesure de Lebesgue en considérant le [[Boréliens|borélien B(Rd)]], on observe que: #!

Il existe une unique mesure $\lambda_d: \mathcal B(\mathbb R^d)$ tel que:
$$\forall a_i < b_i, \forall R = ]a_1, b_1[\times]a_2, b_2[ \times \cdots \times]a_d, b_d[$$
$$\lambda_d(R) = \prod_{i=1}^d(b_i-a_i)$$
<!--ID: 1727551528540-->


## Propriétés principales de $\lambda_d$
On observe que: #!

$\lambda_d$ est [[Vocabulaire de la mesure|une mesure diffuse]]. Ainsi $\forall I_1, \dots, I_d$ intervalles bornées de $\mathbb R$ on a que
$$\lambda_d(I_1 \times \cdots \times I_d) = \prod_{j=1}^d\lambda_1(I_j)$$
### Preuve
Si on prouve que $\lambda_d$ est diffuse, on aura aussi prouvé la seconde propriété.
<!--ID: 1727551528542-->


Soit $x = (x_1, \dots, x_d) \in \mathbb R^d$ Et posons $A_n = ]x_1-\frac{1}{n}, x_1 + \frac{1}{n}[ \times \cdots \times ]x_d-\frac{1}{n}, x_d + \frac{1}{n}[$
Alors observons que $A_{n+1} \subseteq A_n$ et que $\bigcap A_n = \set{x}$
Aussi observons que $\lambda_d(A_1) = 2^d < \infty$. Donc, la [[Propriétés fondamentales de la mesure#Croissance et décroissance séquentielle|décroissance séquentielle s'applique]] 

On a que $\lambda_d(A_n) = \left(\frac{2}{n}\right)^d$
Donc par décroissance séquentielle:
$$\lambda_d(\set{x}) = \lim_{n \to +\infty}\lambda_d(A_n) = \lim_{n \to +\infty}\left(\frac{2}{n}\right)^d = 0$$
