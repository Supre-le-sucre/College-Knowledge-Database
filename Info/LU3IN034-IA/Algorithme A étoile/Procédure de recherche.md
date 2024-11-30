Pour répondre au problème du [[Graphes d'états|graphe d'état]] on propose un algorithme de recherche général

```
O <- { n0 }; F <- None; trouve <- false
Tant que O != None et trouve = false faire
	n <- choix(O) // le choix est à déterminer
	si n dans Etats_finaux alors
		trouve <- vrai
		renvoyer solution
	sinon
		Sn = developper(n) // tous les successeurs de n
		O <- O \ { n }; F <- F U { n }
		Si Sn != None
			pour tout m de Sn, décider si pere(m) <- n // décider pas défini
			O <- O U Sn
		fin Si
	fin Si
fin Tant que 
```

## Comment choisir et décider ?
Proposons l'établissement d'une fonction d'évaluation
