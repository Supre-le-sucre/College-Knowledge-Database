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

## Théorème de convergence monotone
Sur l'espérance on pose le théorème suivant: #!

Soit $(X_{n})_{n \in \mathbb{N}}$ une suite de variable aléatoire à valeur dans $[0, \infty]$ et croissante.
En posant $X = \lim_{n \to \infty } X_{n} = \sup X_{n}$ alors on obtient: $$
\lim_{ n \to \infty } \mathbb E(X_{n}) =  \mathbb E(X)
$$
## Inversion $\sum$ et $\int$ 
Sur l'espérance on pose le théorème suivant: #!

Pour $(X_{n})_{n _{in \mathbb{N}}}$ une suite de variable aléatoire positive alors on a $$
\mathbb E\left( \sum_{n \in \mathbb{N}} X_{n}  \right) = \sum_{n \in \mathbb{N}} \mathbb E(X_{n})
$$

## Lemme de Fatou
Sur l'espérance on a le lemme suivant: #!

Soit $(X_{n})_{n \in \mathbb{N}}$ une suite de variables aléatoire positives alors on a que $$
\mathbb{E}(\liminf_{ n \to \infty } X_{n}) \leq \liminf_{ n \to \infty } \mathbb{E}(X_{n})
$$

## Théorème de convergence dominée
Sur l'espérance, on a le théorème suivant: #!

Soit $(X_{n})_{n \in \mathbb{N}}$ une variable aléatoire à valeur dans $\mathbb{C}$ en supposant que
- $\exists X$ tel que l'on a $\lim_{ n \to \infty } X_{n} =  X$
- $\exists Y$ une variable aléatoire positive telle que $\mathbb E(Y) <\infty$ et $|X_{n}| \leq Y$ presque sûrement
Alors $X$ et $X_{n}$ sont intégrables et $$
\lim_{ n \to \infty } \mathbb{E}(\left| X_{n} - X \right| ) = 0 \text{ et } \lim_{ n \to \infty } \mathbb{E}(X_{n}) = \mathbb{E}(X)
$$

## Inversion $\sum$ et $\int$ dans le cas général
Sur l'espérance, on a le théorème suivant: #!

Soit $(X_{n})_{n \in \mathbb{N}}$ une variable aléatoire à valeur dans $\mathbb{C}$ avec $\mathbb{E}(|X_{n}|) <\infty$. Alors $\sum_{n \in \mathbb{N}} X_{n}$ absolument et on a $$
\mathbb{E}\left( \sum_{n \in \mathbb{N}} X_{n} \right) = \sum_{ n \in \mathbb{N}} \mathbb{E}(X_{n})
$$


## Variance
On définit la variance d'une [[Variable aléatoire]] $X$ de la façon suivante: #!

$$
Var(X) = \mathbb{E}((X - \mathbb{E}(X))^{2}) = \mathbb{E}(X^{2}) - \mathbb{E}(X)^{2}
$$