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
Soient $G' \subset G, H' \subset H$ des sous groupes. On a alors $\phi(G')$ et $\phi^{-1}(G)$ sont aussi des sous-groupes.

#### Démonstration
On prend $e \in G'$. 
Comme $G'$ est un sous groupe, on a que $\phi(e) = e' \in \phi(G')$. 
Observons que $\phi(x)\phi(y)^{-1} = \phi(xy^{-1})$ par propriété de [[Morphismes de groupes]]

