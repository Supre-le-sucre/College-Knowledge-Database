## Définition
On définit une intégrale sur une [[Fonctions étagées#Définition|fonction étagée]] de la façon suivante: #!

Dans un espace mesuré $(E, \mathcal E, \mu)$, dans lequel on note $S_{+}$ l'ensemble des fonctions étagées positive $s : E \to [0, \infty]$. On définit l'intégrale de $s$ contre $\mu$ sur l'ensemble $A \in \mathcal E$, l'application telle que $$
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
= & \sum_{l=1}^p \sum_{{k \in I_{l}}} \gamma_{l}\mu(A \cap A_{k}) \\
= & \sum_{l=1}^p \sum_{{k \in I_{l}}} c_{k} \mu(A \cap A_{k}) \\
= & \sum_{k=0}^n c_{k} c_{k} \mu(A \cap A_{k}) = \int_{A}s \; d\mu
\end{align*}
$$
Comme on peut le voir, nous avons pu réécrire la même intégrale de deux manières différentes, ce qui montre bien que l'unicité de sa définition.


## Propriété de bases de l'intégrales
Pour un espace mesuré $(E, \mathcal E, \mu)$, on observe que les propriétés de bases sont satisfaites: #!

i) <u>Linéarité</u>: $\forall s_{1},s_{2} \in S_{+}, \forall c \geq 0, \forall A \in \mathcal E$ $$
\int_{A}(s_{1}+cs_{2})d\mu = \int_{A}s_{1}d\mu + c \int_{A}s_{2}d\mu
$$
ii) <u>Equivalence d'intégrale</u> $\forall s \in S_{+}, \forall A \in \mathcal E$ $$
\int_{A}sd\mu = \int_{E}s \times\mathbb 1_{A}d\mu
$$
iii) <u>Conservation de l'ordre</u> $\forall s_{1} \leq s_{2} \in S_{+}, \forall A \in \mathcal E$
$$
\int_{A}s_{1}d\mu \leq \int_{A}s_{2}d\mu
$$

iv) <u>Cohérence de l'indicatrice</u> $\forall A, B \in \mathcal E$ $$
\int_{A} \mathbb 1 _{B} d\mu = \mu(A \cap B)
$$
v) <u>Cohérence de l'espace négligeable</u> $\forall A \in \mathcal E, \mu(A)= 0, \forall s \in S_{+}$ $$
\int_{A}sd\mu = 0
$$ vi) <u>Obtention d'une mesure</u>
