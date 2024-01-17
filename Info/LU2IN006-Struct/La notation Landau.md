#struct
## Borne supérieure O
Soit $f(n)$ et $g(n)$ deux fonctions positives définies sur $\mathbb{N}$, On dit que $f(n)$ est en $O(g(n))$ si la fonction $f$ est asymptotiquement bornée supérieurement par la fonction $g$ a un facteur près.

Plus formellement, $f(n)$ est en $O(g(n))$ si et seulement si
$$  \exists n_0 \in \mathbb{N}, k \in \mathbb{R}^+,\forall n \geq n_0, f(n) \leq k g(n)$$

## Borne inférieure $\Omega$
Soit $f(n)$ et $g(n)$ deux fonctions positives définies sur $\mathbb{N}$, On dit que $f(n)$ est en $\Omega(g(n))$ si la fonction $f$ est asymptotiquement bornée inférieurement par la fonction $g$ a un facteur près.

Plus formellement, $f(n)$ est en $\Omega(g(n))$ si et seulement si
$$  \exists n_0 \in \mathbb{N}, k \in \mathbb{R}^+,\forall n \geq n_0, f(n) \geq k g(n)$$

## Borne inférieure et supérieure $\Theta$
Soit $f(n)$ et $g(n)$ deux fonctions positives définies sur $\mathbb{N}$, On dit que $f(n)$ est en $\Theta(g(n))$ si la fonction $f$ est asymptotiquement dominée par la fonction $g$ 

Plus formellement, $f(n)$ est en $\Theta(g(n))$ si et seulement si
$$  \exists n_0 \in \mathbb{N}, k_1, k_2 \in \mathbb{R}^+,\forall n \geq n_0, k_1g(n)\leq f(n) \leq k_2g(n)$$

## Comment cela se calcule ?

Tout simplement en comptant le nombre d'opération élémentaire nécessaire pour traiter un paramètre de taille n.

**Remarque**: si une partie de notre programme a une complexité très importantes, alors il n'est pas nécessaire d'en considérer les parties de codes de complexité moindre dans le calcul de la notation Landau