## Définition d'un préflot
Pour un [[Graphes de capacité|graphe]] $G = (V, E, c)$. On appelle préflot $\tilde{f}$: #!

Une fonction $\tilde{f}:E \to \mathbb R^+$ satisfiant ces deux conditions
- *Toujours positif et respectant la condition de capacité* $$\forall e \in E, 0 \leq \tilde{ f}(e) \leq c(e)$$ 
- *Ce qui entre ne sort pas nécessairement* $$\forall v \in V, \sum_{e \text{ entrant à } v} \tilde f(e) \geq \sum_{e \text{ sortant à } v} \tilde{f}(e)$$On qualifie cela de préflot, car il s'agit d'un état intermédiaire dans lequel tout ce qui entre n'est pas encore nécessairement sorti

