## Définition
Soit $X$ une [[Variable aléatoire réelle]]. On appelle la fonction de répartition de $X$: #!

La fonction $F_X: \mathbb R \to [0, 1]$ définie par $$\forall x \in \mathbb R, F_X(x) = \mathbb P(X \leq x)$$
## Propriété d'égalité
On observe que deux [[Variable aléatoire réelle]] $X$ et $Y$, si elles admettent la même fonction de répartition, admettent aussi la même loi

## Propriété de la fonction de répartition
La fonction de répartition $F_X$ d'une [[Variable aléatoire réelle]] $X$ admet les propriétés suivantes: #!

1. $F_X$ est croissante
2. $F_X$ est continue à droite, i.e: $F_X(x) = \lim_{y \to x^-}F_X(y)$
3. $\lim_{x \to +\infty} F_X(x) = 1$
4. $\lim_{x \to -\infty} F_X(x) = 0$

## Probabilité et fonction de répartition
Pour tout $x \in \mathbb R$ on peut faire le rapprochement entre $\mathbb P(X = x)$ et la fonction de répartition tel que: #!
$$\mathbb P(X =x) = F_X(x) - F_X(x^-)$$

De manière générale d'ailleurs, on peut effectuer les rapprochement suivants entre probabilité et fonctions de répartitions: #!

Soit $a \leq b \in \mathbb R$
- $\mathbb P(X > a) = 1 - F_X(a)$
- $\mathbb P(X \geq b) = 1 - F_X(b^-)$
- $\mathbb P(X \in [a,b]) = F_X(b) - F_X(a^-)$ 
- $\mathbb P(X < a) = F_X(a^-)$
- $\mathbb P(X \in ]a,b]) = F_X(b) - F_X(a)$
- $\mathbb P(X \in ]a,b[]) = F_X(b^-) - F_X(a)$
