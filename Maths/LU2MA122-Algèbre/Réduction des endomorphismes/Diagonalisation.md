## Définition
Soit $\mathbb K$ un corps avec $E$ un $\mathbb K$-espace vectoriel de ==dimension finie==
On dit que $u \in \mathcal L(E)$ et $M \in M_n(\mathbb K)$ sont diagonalisable si et seulement si: #!

- Pour $u \in \mathcal L(E)$ il existe une base $B$ pour laquelle la matrice $Mat_B(u)$ est diagonale
- Pour $M \in M_n(\mathbb K)$ lorsqu'il existe $P \in GL_n(\mathbb K)$ tel que $PMP^{-1}$ est diagonale

## Théorème
Soit $E$ un $\mathbb K$ espace vectoriel de dimension $n$ et $u \in \mathcal L(E)$, les assertions suivantes sur la diagonalisation sont équivalentes: #!

- $(i)$ $u$ est diagonalisable
- $(ii)$ Il existe une base de vecteurs propres de $E$
- $(iii)$ On a la décomposition en somme directe $E = \bigoplus_{\lambda \in Sp(u)} E_\lambda$ 
- $(iv)$ Le polynôme caractéristique $\mathcal X_u$ est *"scindé"* et $\dim(E_\lambda) = m(\lambda)$, où m donne la multiplicité d'une racine dans $\mathcal X_u$
- $(v)$ Il existe un polynôme $P \in \mathbb K[X]$ scindé à racines simples tel que $P(u)= 0$

### Preuve
On montre $(i) \Leftrightarrow (ii)$

 Si $B = (x_1, \dots, x_n)$ la base dans laquelle $Mat_B(u)$ est diagonale, à coefficient diagonaux $\lambda_i$, alors on a que $u(x_i) = \lambda_ix_i$ donc $x_i$ sont des vecteurs propres.
Réciproquement, en considérant la base de vecteur propre $B=(x_1, \dots, x_n)$ on a que $u(x_i) = \lambda_ix_i$ et donc $Mat_B(u)$ est diagonale à coefficient diagonaux $\lambda_i$

Montrons maintenant $(ii) \Leftrightarrow (iii)$ 
Si $(x_1, \dots, x_n)$ est une base de vecteurs propres, de valeurs propres distinctes $\lambda_1, \dots \lambda_s$.
On considère pour chaque $\lambda_k$, l'espace $E_k = Vect(x_{k_1}, \dots x_{k_l})$ où chaque $x_k$ sont de valeurs propres $\lambda_k$
