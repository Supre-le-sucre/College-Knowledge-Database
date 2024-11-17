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
 avec $c_{k}\geq 0$ avec $A_{k}$ deux à deux disjoints, alors on a nécessairement $\{ c_{1}, \dots, c_{k} \} = \{ \gamma_{1}, \dots \gamma_{p} \}$
 