## Définition
Soit $X$ une variable aléatoire de [[Densité discrète]] $p_X$. On définit la fonction génératrice de la variable $X$ la fonction $G_X$ telle que: #!
$$G_X(z) = \sum_{k \in \mathbb N}p_X(k)z^k = \mathbb E(z^X)$$
<!--ID: 1713346066364-->


## Propriété
Il est possible de tirer des propriétés intéressantes de la fonction génératrice de $X$: #!

Pour tout $X$ une variable aléatoire à valeurs dans $\mathbb N$, sa fonction génératrice est bien définie au moins sur $[-1, 1]$ et infiniment dérivable sur $]-1, 1[$.
On peut aussi caractériser la loi de $X$ en fonction de la fonction génératrice: $$p_X(k) = \frac{1}{k!}G_X^{(k)}(0)$$
<!--ID: 1713346066373-->


## Fonction génératrice avec l'indépendance
Soit $X$ et $Y$ deux variables aléatoires indépendantes à valeurs dans $\mathbb N$ alors on a: #!
$$\forall z \in \mathbb R^+, G_{X+Y}(z) = G_X(z)G_Y(z)$$ Si les fonctions génératrices sont toutes deux finies, cette égalité est valable $\forall z \in \mathbb R$
<!--ID: 1713346066378-->

