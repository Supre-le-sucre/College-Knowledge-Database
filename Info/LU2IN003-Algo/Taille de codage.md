#algo
## Définition
La taille de codage d'un paramètre est une évaluation, la plus raisonnable possible de la place nécessaire en mémoire pour le stocker.
Un ordinateur stocke les données dans des bits, pouvant être 0 ou 1. Les données sont alors accessibles en base 2.

## Propriété de la base 2
On a que 
$$ \forall n \in \mathbb{N}^*, \exists k \in\mathbb{N}, 2^k \leq n \leq 2^{k+1} $$
Avec la valeur de $k$ donnée par:
$$ k = \lfloor log_2(n)\rfloor$$
Autrement dit, n'importe quel entier peut être codée dans la base 2 avec pour $\forall i, n_i = \set{0, 1}$

$$ n = \sum_{i=0}^{K(n)} n_i2^i$$
On a alors $1 + K(n) = k + 1 = \lfloor log_2(n)\rfloor + 1$ la taille de codage d'un entier.
