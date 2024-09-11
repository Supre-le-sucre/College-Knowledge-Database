## Définition d'un graphe
On définit plus précisément un graphe ==orienté== de la façon suivante $G =(V, E, c, s, t)$
où 
- $c: E \to \mathbb R$ est la capacité (valeur du label sur l'arête)
- $s$ et $t$ sont respectivement les sources et les puits qui représente les sommets entrant et les sommets sortant

## Définition du flot

Un flot est une application sur les sommets d'un [[Graphes orientés|graphe]] $f: V^2 \to \mathbb R$ avec les conditions:
- Antisymétrique: $f(u,v) = -f(v,u)$
- Conservation $\forall u \not = \set{s, t} \in V, \sum_{v \in V} f(u,v) = 0$
- Capacité: $\forall u, v \in V f(u,v) \leq c(\{u,v\})$