## Définition d'un graphe
On définit plus précisément un graphe ==orienté== de la façon suivante $G =(V, E, c, s, t)$
où #!
- $c: E \to \mathbb R$ est la capacité (quantité d'information pouvant passer)
- $s$ et $t$ sont respectivement les sources et les puits qui représente les sommets entrant et les sommets sortant

## Définition du flot
Un flot est une application sur les sommets d'un [[Graphes orientés|graphe]] $f: V^2 \to \mathbb R$ avec les conditions: #!
- Antisymétrique: $f(u,v) = -f(v,u)$
- Conservation $\forall u \not = \set{s, t} \in V, \sum_{v \in V} f(u,v) = 0$
- Capacité: $\forall u, v \in V f(u,v) \leq c(\{u,v\})$
Un arc est dit saturé si $f(u, v) = c(u, v)$
**ATTENTION** : ==Tout ce qui rentre dans un sommet (à part la source et le puits), ressort==

### Valeur du flot
Dans un graphe, la valeur du flot $f$, notée $|f|$ est donnée par: #!
$$|f| = \sum_{v \in V} f(s, v) = \sum_{u \in V} f(u, t)$$
# Coupe minimum

## Définition d'une coupe
On dit que $(A, B)$ est une coupe pour $G = (V, E, c, s, t)$ si: #!

$A, B$ sont des partitions de $V$ et tel que $s \in A$ et $t \in B$

### Capacité d'une coupe
On définit la capacité de la coupe $(A, B)$: #!
$$c(A, B) = \sum_{u \in A, v \in B} c(a, b)$$
### Flot d'une coupe
On définit le flot d'une coupe $(A,B)$: #!
$$f(A, B) = \sum_{u \in A, v \in B} f(u,v)$$
