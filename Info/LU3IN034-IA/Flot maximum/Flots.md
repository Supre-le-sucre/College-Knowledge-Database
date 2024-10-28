## Définition du flot
Un flot est une application sur les sommets d'un [[Graphes de capacité]] $f: V^2 \to \mathbb R$ avec les conditions: #!
- Antisymétrique: $f(u,v) = -f(v,u)$
- Conservation $\forall u \not = \set{s, t} \in V, \sum_{v \in V} f(u,v) = 0$
- Capacité: $\forall u, v \in V f(u,v) \leq c(u,v)$
Un arc est dit saturé si $f(u, v) = c(u, v)$
**ATTENTION** : ==Tout ce qui rentre dans un sommet (à part la source et le puits), ressort==, c'est ce que dit la propriété de conservation.
<!--ID: 1730114115954-->



### Valeur du flot
Dans un graphe, la valeur du flot de $G$ notée $|f|$ est donnée par: #!
$$|f| = \sum_{v \in V} f(s, v) = \sum_{u \in V} f(u, t)$$
En d'autres termes, il s'agit du flot en circulation dans le graphe. L'égalité entre la source et le puit viens du fait que tout ce qui rentre dans un sommet doit ressortir.
<!--ID: 1730114115955-->


#### Exemple
![[Pasted image 20241026185306.png]]
Le graphe ci-dessous admet une valeur de flot $|f| = 6$

## Définition du flot maximum
On qualifie une fonction de flot $f^*$ de $G$ de maximum si et seulement si: #!
Il n'existe pas d'autres fonctions de flot $f$ telle que $|f| > |f^*|$
<!--ID: 1730114115957-->



