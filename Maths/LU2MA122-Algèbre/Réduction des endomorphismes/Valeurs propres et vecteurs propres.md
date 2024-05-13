## Définition
Soit $\lambda \in \mathbb K$, on dit que $\lambda$ est une valeur de propre de $u \in \mathcal L(E)$ si: #!

Il existe un $x \in E - \{0\}$ tel que $u(x) = \lambda x$. On dit alors que $x$ est un vecteur propre. En particulier, si $\lambda$ est une valeur propre, alors $u- \lambda Id$ n'est pas injectif.
Pour $\lambda \in \mathbb K$, on appelle sous-espace propre de $u$ associé à $\lambda$ l'espace vectoriel: $\ker(u - \lambda Id_E)$.
Enfin on note $Sp(u)$ l'ensemble des valeurs propres de $u$ que l'on appelle spectre de $u$
<!--ID: 1715537862424-->


## Lemme
On donne le lemme suivant pour les [[Polynômes d'endomorphismes]] admettant des valeurs propres: #!

Soit $u \in \mathcal L(E)$ et $\lambda$ une valeur propre de $u$. Pour $P \in \mathbb K[X]$ tel que $P(u) = 0$, on a que  $P(\lambda) = 0$
<!--ID: 1715537862425-->


### Preuve
Soit $x$ un vecteur propre non nul, alors $u(x) = \lambda x$ et donc $P(u)(x) = P(\lambda x) = P(\lambda)x = 0$ donc on a bien $P(\lambda) = 0$

$$\tag*{$\blacksquare$}$$