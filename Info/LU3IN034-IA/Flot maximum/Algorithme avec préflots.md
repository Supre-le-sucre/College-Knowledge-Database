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
