#algebre 
## Définition

Soit $(G, .)$ un [[Groupe |groupe]]. Une partie non vide $H \subseteq G$ est qualifiée de sous-groupe si celui-ci est stable par opération avec un inverse. i.e:
$$ \forall (x,y) \in H^2, x.y^{-1} \in H $$
*Exemple:* $(\mathbb{Q}^*, \times)$ est un sous-groupe de $({R^*, \times})$
### Remarques importantes

1. La définition implique forcément que l'élément neutre $e \in H$
$$ H \not = \emptyset, x \in H \Rightarrow x.x^{-1} = e \in H$$
2. Il est commode, pour prouver qu'on a à faire à un groupe, de prouver qu'il s'agit d'un sous-groupe d'un groupe de référence.

## Lemme de conservation par [[Morphismes de groupes|morphisme de groupe]]

### Lemme
On pose $\phi : G \to H$ un [[Morphismes de groupes]].
Soient $G' \subset G, H' \subset H$ des sous groupes. On a alors $\phi(G')$ et $\phi^{-1}(H')$ sont aussi des sous-groupes.

#### Démonstration
Soient $\phi : G \to H$, un [[Morphismes de groupes]] et $G' \subset G, H' \subset H$ avec $G,H$ des groupes, $G', H'$ des sous-groupes.
Soit $1_G, 1_H$ les éléments neutres respectifs de $G$ et $H$

- Montrons que $\phi(G')$ est un sous groupe.
Autrement dit, montrons la stabilité par opération d'un inverse de $\phi(G')$

On sait que $1_G \in G'$ (cf. [[Sous-groupe#Remarques importantes]])

Comme $G'$ est un sous groupe, $G' \subset G$, on a que $\phi(1_G) = 1_H \in \phi(G')$.
On a donc que $\phi(G') \not = \emptyset$.

Soit $x,y \in G'$
Observons que $\phi(x).\phi(y)^{-1} = \phi(x.y^{-1})$ par propriété de [[Morphismes de groupes#Remarques importantes]].
Puisque $G'$ est un sous groupe, par stabilité: $x.y^{-1} \in G'$ 
Donc $\phi(x.y^{-1}) \in \phi(G')$, autrement dit: $\phi(x).\phi(y)^{-1} \in \phi(G')$

On a bien la stabilité propre aux sous groupe. Donc $\phi(G')$ est un sous groupe.

- Montrons que $\phi^{-1}(H')$ est un sous groupe

Observons que par définition, on a l'équivalence suivante $(1)$
$$ x \in \phi^{-1}(H') \Leftrightarrow \phi(x) \in H'$$

Puisque $\phi$ un morphisme de groupe: $\phi(1_G) = 1_H$
Par $(1)$