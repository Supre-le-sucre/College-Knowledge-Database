
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
fin Tant que 
```