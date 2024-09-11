## Définition du flot
Un flot est une application sur les sommets d'un [[Graphes de capacité]] $f: V^2 \to \mathbb R$ avec les conditions: #!
- Antisymétrique: $f(u,v) = -f(v,u)$
- Conservation $\forall u \not = \set{s, t} \in V, \sum_{v \in V} f(u,v) = 0$
- Capacité: $\forall u, v \in V f(u,v) \leq c(\{u,v\})$
Un arc est dit saturé si $f(u, v) = c(u, v)$
**ATTENTION** : ==Tout ce qui rentre dans un sommet (à part la source et le puits), ressort==

### Valeur du flot
Dans un graphe, la valeur du flot $f$, notée $|f|$ est donnée par: #!
$$|f| = \sum_{v \in V} f(s, v) = \sum_{u \in V} f(u, t)$$
