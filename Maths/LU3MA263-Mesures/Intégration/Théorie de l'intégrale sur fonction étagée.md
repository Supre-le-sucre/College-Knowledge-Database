## Définition
On définit une intégrale sur une [[Fonctions étagées#Définition|fonction étagée]] de la façon suivante: #!

Dans un espace mesuré $(E, \mathcal E, \mu)$, dans lequel on note $S_{i}$ l'ensemble des fonctions étagées positive $s : E \to [0, \infty]$. On définit l'intégrale de $s$ contre $\mu$ sur l'ensemble $A \in \mathcal E$, l'application telle que $$
\int_{A}s\;d\mu = \sum_{k=0}^{n}c_{k}\:\mu(A_{k} \cap A)
$$
Avec les $A_{k}$ deux à deux disjoints

### Remarque importante
On rappelle qu'une [[Fonctions étagées#Définition|fonction étagée]] peut s'écrire de plusieurs façon différentes. Il est donc nécessaire de prouver ==l'unicité de la définition de l'intégrale==.

Notons $s(E) = \{ \gamma_{1}, \dots, \gamma_{p} \}$ les valeurs distinctes
Observons que $s^{-1}(\gamma_{i})= B_{i}$ qui sont 2 à 2 disjoints par définition

En posant une autre écriture $$
s = \sum_{k=0}^nc_{k}
 \mathbb 1_{A_{k}}
 $$
 avec $c_{k}\geq 0$ avec $A_{k}$ deux à deux disjoints.
 Pour avoir des indices qui coïncident, On va poser l'espace suivant
 $$
I_{l} = \{ k \in \{ 1, \dots, n \} : c_{k} = \gamma_{l} \}
$$
Ce qui nous permet ainsi de poser l'égalité suivante. $$
B_{l} = \bigcup_{k \in I_{l}} A_{k}
$$
Comme les $A_{k}$ sont posé comme étant disjoint 2 à 2, on a par sigma additivité de la [[Mesure]] l'égalité suivante $\mu(A \cap B_{l}) = \sum_{{k \in I_{l}}} \mu(A \cap A_{k})$
Et ainsi on a
$$
\begin{align*}
\sum_{{y} \in s(E)} y \mu(A \cap s^{-1}(\{ y \})) = &\sum_{l=1}^p \gamma_{l} \mu(A \cap B_{l}) \\
= & \sum_{l=1}^p \sum_{{k \in I_{l}}} \gamma_{l}\mu(A \cap A_{k})
\end{align*}
$$