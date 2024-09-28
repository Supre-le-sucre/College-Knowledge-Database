## L'intersection de tribu
Soit $\mathcal E_i$ avec $i \in I$ des tribus sur $E$. Alors:
$$\mathcal E = \bigcap_{i \in I}\mathcal E_i$$est encore une tribu de $E$.
**Remarque**: En général, l'union de tribu ne forme pas de tribu

### Preuve
On vérifie que $\mathcal E$ est une tribu...

i) $\forall i \in I$, $E \in \mathcal E_i$ car les $\mathcal E_i$ sont des tribus
Donc $E \in \bigcap \mathcal E_i$

ii) Soit $A \in \mathcal E$, montrons que $A^c \in \mathcal E$
Si $A \in \mathcal E$, alors $A \in \mathcal E_i$ pour tout i. Mais $\mathcal E_i$ sont des tribus, donc, $A^c \in \mathcal E_i$ pour tout i

iii) Soit $A_n \in \mathcal E$, on a donc que pour tout i et n $A_n \in \mathcal E_i$
Or comme les $\mathcal E_i$ sont des tribus, $\bigcup A_n \in E_i$ pour tout i

## Tribu engendrée
On définit une tribu engendrée de la façon suivante: #!

Soit $\mathcal R \in \mathcal P(E)$ un sous-ensemble quelconque. On appelle la tribu engendrée par $\mathcal R$, ==la plus petite tribu== qui contient $\mathcal R$. Autrement dit:
$$\sigma(\mathcal R) = \bigcap_{\mathcal R \subset \mathcal E, \mathcal E \text{ une tribu}} \mathcal E$$
**Remarquons que** si $\mathcal R$ est une tribu, alors $\mathcal R = \sigma(\mathcal R)$

# Tribu borélienne sur $\mathbb R$
On définit une telle tribu comme suit: #!

La tribu borélienne de $\mathbb R$ est la tribu engendrée pare tous les ouverts.
$$\mathcal B(\mathbb R) = \sigma(\tau(\mathbb R))$$
**Remarque** Si on considère l'ensemble topologique $(E, \tau(E))$, sa tribu borélienne est alors $\mathcal B(E) = \sigma(\tau(E))$


## Lemme
On observe que la tribu borélienne possède tous ces ensembles particuliers: #!

Tous les types d'intervalles possibles, soit $\forall a < b$ on a que $\mathcal B(\mathbb R)$ contient
$$\mathbb R, \emptyset, \set{a}, ]-\infty; a], ]-\infty; a[, ]b; +\infty[,  [b, +\infty[, [a,b], ]a,b[, ]a, b], [a,b[$$

### Preuve
Par définition $\mathcal B(\mathbb R)$ contient tous les ouverts, donc par stabilité du complémentaire, il contient aussi tous les fermés. Les ensembles restants sont le résultats d'un combinaison d'ouvert et de fermé par stabilité de l'union:
*Ex:* $]a,b] = ]a,b[ \cup \set{b}$

## Lemme, un autre moyen d'engendrer $\mathcal B(\mathbb R)$ 
On observe que: #!

Si $\mathcal R = \set{]-\infty, a], a \in \mathbb R}$, alors $\mathcal B(\mathbb R) = \sigma(\mathcal R)$

### Preuve
D'abord montrons $\sigma(\mathcal R) \subseteq \mathcal B(\mathbb R)$.
D'après le lemme précédent, on a que $\mathcal R \in \mathcal B(\mathbb R)$. Et comme $\mathcal B(\mathbb R)$ est une tribu, et que $\sigma(\mathcal R)$ est censé être la plus petite, alors on a forcément que $\sigma(\mathcal R) = \mathcal B(\mathbb R)$

Montrons maintenant que $\mathcal B(\mathbb R) \subseteq \sigma(\mathcal R)$
Nous utilisons la définition du borélien: on vérifie que tous les ouverts sont dans $\sigma(\mathcal R)$

i) $]a, +\infty[ \in \sigma(\mathcal R)$, car c'est le complémentaire immédiat de $]-\infty, a]$ et la stabilité du complémentaire d'une tribu l'y oblige

ii) $]-\infty; a[ \in \sigma(\mathcal R)$, car $]-\infty; a[ = \bigcup_{n \in \mathbb N} ]-\infty, a - \frac{1}{n}[$ et on a la stabilité par union dénombrable

iii) $]a,b[ \in \sigma(\mathcal R)$ car $]a,b[ = ]- \infty, b[\; \cap \; ]a, +\infty[$ par stabilité du complémentaire et de l'union

iv) Soit $O$ un ouvert de $\mathbb R$, alors $O$ s'écrit comme une union dénombrable d'intervalle ouvert, donc $O \in \sigma(\mathcal R)$ d'après les résultats précédent

**Remarque**: Les boréliens sont engendrés par plein de classe de sous-ensemble

# Tribu borélienne sur 