## Définition d'un PDM
Un PDM ou Processus décisionnel Markovien se définit de la façon suivante: #!

Il s'agit d'un tuple $(S, A, T, R)$ avec
- $S$ l'ensemble des états du monde (cet ensemble est fini)
- $A$ l'ensemble des actions que l'agent peut effectuer
- $T: S \times A \to L(S)$ ($L(S)$ représente les lois de probas à support fini sur $S$) qui pour tout couple d'état et d'action, renvoie la loi de probabilité $T(s, a)$. C'est à dire les probabilités d'atteindre un état en sachant que l'action $a$ a été réalisé sur l'état $s$
- $R: S \times A \to \mathbb{R}$ qui qualifie la récompense immédiate obtenu si le couple état action a eu lieu.

On pose la règle de décision, la fonction $d_{i}: S \to A$ qui à l'instant $i$ et suivant un état $s$, on obtient une action $a$
**Notre problème**: C'est de maximiser la récompense sur un "horizon" fini (donc jusqu'à $N$ itérations d'actions) ou un horizon infini. (Maximiser l'==espérance de la récompense==: $$\mathbb E\left( \sum_{t=1}^{N} R(s, d_{t}(s)) \right)$$

## Horizon infini
Dans le cadre d'un horizon infini, tous les chemins se valent, étant donné que ces chemins donnent tous une récompense infinie.
On pose alors le facteur d'actualisation comme suit: #!

$\gamma \in ]0, 1[$ qualifié de facteur d'actualisation permet de pondéré la récompense au fur et à mesure des itérations, il dépend de si on veut gagner une récompense rapidement (proche de 0) ou dans longtemps proche de $1$. On calcule alors l'espérance $$\mathbb E\left( \sum_{t=1}^{+\infty} \gamma^t R(s, d_{t}(s)) \right) \leq \frac{M}{1 - \gamma} $$

## Valeur d'une politique
Une politique représente l'ensemble des décisions à chaque étape sur un horizon.
La valeur d'une politique en l'état $s$ à un instant $t$ se définit de la façon suivante

En posant l'état $1$ comme la dernière décision
- **Dernière décision** $$V_{d,1}(s) = R(s, d_{1}(s))$$
- **Décision à l'étape t** $$V_{d,t}(s) = R(s, d_{t}(s)) + \sum_{s' \in S}T(s,a)(s')V_{d,t-1} (s')$$