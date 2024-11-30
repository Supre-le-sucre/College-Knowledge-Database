
L'algorithme est une [[Procédure de recherche]] caractérisé par une [[Heuristique]] particulière et dont le choix est déterminer comme suit

```
O <- { n0 }; F <- None; g(n0) = 0; n <- n0
Tant que O != None et n != Etats_finaux faire
	O <- O \ { n }; F <- F U { n }
	Pour tout m dans S(n) faire
		Si m != O U F ou g(m) > g(n) + k(n,m) // Si m n'a jamais été vu, ou si le chemin pour y aller est meilleur...
			g(m) <- g(n) + k(n, m)
			f(m) <- g(m) + h(m)
			pere(m) <- n
			ranger m dans O par f croissant et g décroissant
		fin Si
	fin pour
	Si O != None alors n <- first(O)
fin Tant que 
```

## Propriétés de l'algorithme

- Pour toute heuristique positive et $G$ fini, admettant un chemin but fini, l'algorithme $A^{*}$ se termine en un temps fini
- Pour toute heuristique positive et $G$ fini ou infini, admettant un chemin but fini, alors tout chemin optimal entre $n_{0}$ à $\Gamma$ possède au moins un nœud $n_{i}$ tel que $g(n_{i})=g^*(n_{i})$
- Si l'heuristique est minorante alors à la fin de chacun des itérations de $A^{*}$, le noeud en tête de $O$ est tel que $f(n) \leq f^{*}(n_{0})$
- Si l'heuristique est minorante alors $A^*$ ne développe aucun nœud dont l'évaluation $f$ est plus grande que $f^{*}$
- Si l'heuristique est minorante alors $A^{*}$ est valide (mais peut ne pas se terminer voir premier point)
- Si l'heuristique est minorante alors la recherche se limite aux nœuds de l'ensemble
$$\{ n  \in N, g^*(n) + h(n) \leq f^*(n_{0}) \}$$
- Si $h$ est monotone, alors tout nœud développé par $A^{*}$ est tel que $g(n) = g^{*}(n)$. Il s'ensuite qu'un nœud ne peut être développer au plus d'une fois
