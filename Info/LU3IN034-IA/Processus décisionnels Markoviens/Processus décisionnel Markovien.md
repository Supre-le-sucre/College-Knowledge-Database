## Définition d'un PDM
Un PDM ou Processus décisionnel Markovien se définit de la façon suivante: #!

Il s'agit d'un tuple $(S, A, T, R)$ avec
- $S$ l'ensemble des états du monde (cet ensemble est fini)
- $A$ l'ensemble des actions que l'agent peut effectuer
- $T: S \times A \to L(S)$ ($L(S)$ représente les lois de probas à support fini sur $S$) qui pour tout couple d'état et d'action, renvoie la loi de probabilité $T(s, a)$. C'est à dire les probabilités d'atteindre un état en sachant que l'action $a$ a été réalisé sur l'état $s$
- $R: S \times A \to \mathbb{R}$ qui qualifie la récompense immédiate obtenu si le couple état action a eu lieu.

## Horizon
Un PDM se formule en fonction d'une "temporalité". Dans un état, nous sommes amené à effectuer une action en *une temporalité.* 

Si ces temporalités sont finies, autrement dit,  qu'il existe des états "finaux", dans lesquels, une action n'entraîne pas l'évaluation d'un autre état, on parle d'horizon ==fini==

Autrement, si on est amené à prendre en compte une infinité d'actions, on parle d'horizon infini.

## Politique
On pose la règle de décision, la fonction $d_{i}: S \to A$ qui à l'instant $i$ et suivant un état $s$, renvoie une action $a$
Une politique est un n-uplet de "règle de décision" qui permet de prendre une décision à n'importe quel instant




## Formulation du problème
Bien souvent, on cherche à trouver une "politique optimale" permettant de maximiser la récompense. 

Dans le cas d'un horizon finie, la formulation est simple, car il s'agit de maximiser l'**espérance de la récompense**: 
$$\mathbb E\left( \sum_{t=1}^{N} R(s, d_{t}(s)) \right)$$

Dans le cas d'un horizon infini, notons que la récompense ne ==dépend pas== de la temporalité dans laquelle nous nous trouvons. Ainsi donc, **toutes les politiques se valent car elles rapportent toutes une récompense infinie**.

Afin de tendre vers une politique idéale, on cherche donc à maximiser l'espérance de la récompense **en rajoutant un facteur d'actualisation** qui change en fonction de la temporalité.

On note $\gamma \in ]0, 1[$  ce facteur. Il permet donc de pondéré la récompense au fur et à mesure des itérations. 
Sa valeur dépend de si on veut gagner une récompense rapidement (proche de 0) ou dans longtemps proche de $1$. On calcule alors l'espérance $$\mathbb E\left( \sum_{t=1}^{+\infty} \gamma^t R(s, d_{t}(s)) \right) \leq \frac{M}{1 - \gamma} $$

## Valeur d'une politique
Une politique représente l'ensemble des décisions à chaque étape sur un horizon.
La valeur d'une politique en l'état $s$ à un instant $t$ se définit de la façon suivante correspond à l'**espérance de la récompense** à une certaine étape de décision

En posant l'état $1$ comme la dernière décision
- **Dernière décision** $$V_{d,1}(s) = R(s, d_{1}(s))$$
- **Décision à l'étape t** $$V_{d,t}(s) = R(s, d_{t}(s)) + \sum_{s' \in S}T(s,a)(s')V_{d,t-1} (s')$$

## Calcul de la politique optimale
On pose $V^*$ la valeur optimale et $d^*$ la décision optimale. Elles sont définies récursivement de la façon suivante. (En commençant par 1)

$V_{1}^* = \max R(s,a)$ et $d^*_{1} = \arg \max_{a} R(s, a)$
Et puis

$V_{t}^* = \max( R(s, a) + \sum_{s' \in S}T(s,a)(s')V^*_{d,t-1} (s')$
Et $d^*$ donné par l'argument $a$ de ce max