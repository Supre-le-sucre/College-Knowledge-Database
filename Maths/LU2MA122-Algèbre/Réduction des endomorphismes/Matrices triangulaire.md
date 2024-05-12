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
Pour $BC \in T_n(\mathbb K)$ un simple calcule matriciel suffit à le prouver. Mais nous allons plutôt étudier l'aspect endomorphique