## Définition
On considère un graphe $G=(N, A)$ avec

- $N$ l'ensemble de ses nœuds (sommet)
- $n_{0} \in N$ le nœud initial
- $\Gamma \subset N$ les nœuds buts
- $S(n) \subset N$ les successeurs du nœud $n$ avec supposition que $|S(n)|$ fini
- $A = \{ (n,p), n \in N, p \in S(n) \}$ l'ensemble des arcs du graphe
- $k: A \to \mathbb{R}^{+}$ la valuation du graphe $k(n, m)$ est donc le coût de l'arc $(n, m)$

Notre problème, c'est de savoir s'il existe un chemin à moindre coup pour aller de $n_{0}$ à $\gamma \in\Gamma$
