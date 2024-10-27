## Définition d'un préflot
Pour un [[Graphes de capacité|graphe]] $G = (V, E, c)$. On appelle préflot $\tilde{f}$: #!

Une fonction $\tilde{f}:E \to \mathbb R^+$ satisfaisant ces deux conditions
- *Toujours positif et respectant la condition de capacité* $$\forall e \in E, 0 \leq \tilde{ f}(e) \leq c(e)$$ 
- *Ce qui entre ne sort pas nécessairement* $$\forall v \in V, \sum_{e \text{ entrant à } v} \tilde f(e) \geq \sum_{e \text{ sortant à } v} \tilde{f}(e)$$On qualifie cela de préflot, car il s'agit d'un état intermédiaire dans lequel tout ce qui entre n'est pas encore nécessairement sorti

## Définition d'excédant
Comme ce qui entre dans un sommet n'est pas nécessairement ressorti dans un préflot, on qualifie alors la fonction excédant du préflot $\tilde{f}$, la fonction $ex_{\tilde{f}} :V \to \mathbb R^+$ telle que: #!

$$
ex_{f}(v) = \sum_{e \text{ entrant à }v} \tilde{f}(e) - \sum_{e \text{ sortant à }v}\tilde{ f}(e)
$$

## Etiquetage d'un préflot
Pour une fonction d'étiquetage $h: V \to \mathbb{N}$, on dit que celle-ci est compatible avec le préflot $\tilde{ f}$ de graphe d'écart $G_{\tilde{ f}} = \left(V_{\tilde{ f}}, E_{\tilde{ f}}\right)$ si et seulement si: #!

$h(t) = 0$ et $h(s) = |V| = n$
$$
\forall(v,f) \in E_{\tilde{f}}, \quad h(v) \leq h(w)+1
$$L'étiquetage peut alors faire penser à la hauteur d'un sommet


## Propriété de l'étiquetage compatible
On observe les 2 propriétés suivantes: #!

- Si un préflot $\tilde{f}$ est compatible avec un étiquetage $h$, alors il n'existe pas de chemin augmentant dans $G_{\tilde{f}}$
- Si $f$ est ==un flot== compatible avec $h$, alors dans ce cas, il s'agit d'un [[Flots maximum et coupe minimum|flot maximum]]


# Algorithme de préflot
L'algorithme de préflot cherche à trouver le flot maximum d'un [[Graphes de capacité|graphe]] $G$ en s'autorisant une meilleur flexibilité sur les flots du graphe (ce qui entre ne sort pas encore nécessairement)

## Initialisation
On pose au départ, un étiquetage $h$ tel que $h(s) = |V| = n$ et $\forall v \neq s, h(v) = 0$
Et un préflot $f$ tel que:

- *On [[Flots#Définition du flot|sature]] les arcs issus de la source* $$\forall e = (s, v), \quad f(e) = c(e)$$
- *Aucun flot ne sort de tous les autres arcs* $$\forall e \neq (s,v), \quad f(e) = 0$$
**NOTE**: Ici le préflot et l'étiquetage sont <u>compatibles</u>. ==**OR**==, il s'agit ici d'un ==**PREFLOT**==, donc il ne s'agit pas encore d'un flot maximum !!


## Push
Pour