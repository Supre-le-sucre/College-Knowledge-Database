On a définit l'espérance [[Variable aléatoire#Espérance|ici]]

## Propriétés principales
Pour $X, Y$, 2 variable aléatoires on observe les propriétés principales de l'espérance: #!

1) Linéarité de l'intégrale
$$
\mathbb E(X + cY) = \mathbb E(X) + c \mathbb E(Y)
$$
2) Inégalité triangulaire de l'intégrale
$$
|\mathbb E(X)| \leq \mathbb E(|X|)
$$
3) Cohérence de l'intégrale
$$
\mathbb E(\mathbb 1_{A}) = \mathbb P(A)
$$
4) Si $X$ est une variable aléatoire **bornée** alors elle est nécessairement intégrable (la masse de $\mathbb P$ étant finie)
$$
|X| \leq C \implies \mathbb E(|X|) \leq \mathbb E(C) \leq C \ \mathbb P(\Omega) \leq C < \infty
$$