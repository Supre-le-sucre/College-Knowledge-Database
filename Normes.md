On définit une norme sur $\mathbb{R}^n$, une application $N: \mathbb{R}^n \to \mathbb{R}$ telle que:

- La __séparation__ est vérifiée
$$\forall x \in \mathbb{R}, N(x) = 0 \Leftrightarrow x = 0_{\mathbb{R}^n}$$
- L'**homogénéité** est vérifiée
$$\forall x \in \mathbb{R}^n, \forall \lambda \in \mathbb{R},  N(\lambda x) = |\lambda|N(x)$$
- L'[[Inégalité triangulaire]] est vérifiée
$$ \forall x,y \in \mathbb{R}^n, N(x+y) \leq N(x)+N(y) $$

## Normes usuelles sur $\mathbb{R}^n$

Soit $x \in \mathbb{R}^n$ de i ème cordonnée: $x_i$
### Norme de Manathan

$$ N(x) = \sum_{i=1}^n |x_i| $$
### Norme euclidienne
$$ N(x) = \sqrt{\sum_{i=1}^n x_i^2} $$

### Norme infinie
$$N(x) = \sup_{[1, n]}{|x_i|} $$


