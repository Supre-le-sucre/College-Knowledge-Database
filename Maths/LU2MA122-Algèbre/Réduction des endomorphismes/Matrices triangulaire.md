## Dimensions de l'ensemble
On définit l'ensemble des matrices triangulaires supérieurs par $T_n(\mathbb K) \subset M_n(\mathbb K)$.
Observons que la dimension d'un tel ensemble est de #!

$$\dim(T_n(\mathbb K)) = \frac{n(n+1)}{2}$$
Car en effet il est nécessaire d'avoir $n$ matrices pour construire la diagonale, puis $n-1$ matrices pour la diagonale juste au dessus etc.

## Stabilité des matrices triangulaires
On observe le phénomène suivant: #!

$$\forall B,C \in T_n(\mathbb K), \; BC \in T_n(\mathbb K)$$
On observe aussi que si $B \in GL_n(\mathbb K)$ également, alors $B^{-1} \in \mathbb T_n(\mathbb K)$ (i.e son inverse reste triangulaire supérieure)

### Preuve
Pour $BC \in T_n(\mathbb K)$ un simple calcule matriciel suffit à le prouver. Mais nous allons plutôt étudier l'aspect endomorphique.

Posons $(e_1, \dots, e_n)$ la base canonique de $u$ et de $v$ les endomorphismes associés à $B$ et $C$ respectivement.
Comme $B$ et $C$ sont triangulaires supérieures on a que
$$\forall i \in [1, n], u(e_i), v(e_i) \in Vect(e_k)_{1 \leq k \leq i}$$
Observons alors simplement que
$$\forall i \in [1,n], u(v(e_i)) \in u(Vect(e_k)_{1\leq k \leq i}) \subset Vect(e_k)_{1\leq k \leq i}$$
Et donc la matrice associé à $u \circ v$ est bien triangulaire supérieure.

Pour la deuxième assertion, observons que $B^{-1}$ est un polynôme en $B$. Donc comme $T_n(\mathbb K)$ est un $\mathbb K$-espace vectoriel stable par multiplication, on a que $\mathbb K[B] \subset T_n(\mathbb K)$ soit alors que $B^{-1} \in T_n(\mathbb K)$
$$\tag*{$\blacksquare$}$$

## Nilpotent
Pour une matrice $B \in T_n(\mathbb K)$ dont les coefficient diagonaux sont nuls, on observe que: #!

$B$ est une matrice nilpotente tel que $B^n = 0$

### Preuve
Bien que ceci soit vérifiable par calcul matriciel, il y a moyen plus simple.
Les valeurs propres de $B$ sont forcément ses coefficient diagonaux. Or, comme ceux-ci sont  nuls, on a d'après