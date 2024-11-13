## Définition d'un PDM
Un PDM ou Processus décisionnel Markovien se définit de la façon suivante: #!

Il s'agit d'un tuple $(S, A, T, R)$ avec
- $S$ l'ensemble des états du monde (cet ensemble est fini)
- $A$ l'ensemble des actions que l'agent peut effectuer
- $T: S \times A \to L(S)$ ($L(S)$ représente les lois de probas à support fini sur $S$) qui pour tout couple d'état et d'action, renvoie la loi de probabilité $T(s, a)$. C'est à dire les probabilités d'atteindre un état en sachant que l'action $a$ a été réalisé sur l'état $s$
- $R: S \times A \to \mathbb{R}$ qui qualifie la récompense immédiate obtenu si le couple état action a eu lieu.

**Notre problème**: C'est de maximiser la récompense sur un "horizon" fini (donc jusqu'à $N$ itérations d'actions) ou un horizon infini.
