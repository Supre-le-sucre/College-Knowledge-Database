## Définition d'un PDM
Un PDM ou Processus décisionnel Markovien se définit de la façon suivante: #!

Il s'agit d'un tuple $(S, A, T, R)$ avec
- $S$ l'ensemble des états du monde (cet ensemble est fini)
- $A$ l'ensemble des actions que l'agent peut effectuer
- $T: S \times A \to L(S)$ ($L(S)$ représente les lois de probas à support fini sur $S$) qui pour tout couple d'état et d'action, renvoie la loi de probabilité $T(s, a)$. C'est à dire les probabilités d'atteindre un état en sachant que l'action $a$ a été réalisé sur l'état $s$
- $R: S \times A \to \mathbb{R}$ qui qualifie la récompense immédiate obtenu si le couple état action a eu lieu.
<!--ID: 1734268137933-->


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
**A noter que:** Il est aussi possible de poser ce facteur dans un horizon fini.
