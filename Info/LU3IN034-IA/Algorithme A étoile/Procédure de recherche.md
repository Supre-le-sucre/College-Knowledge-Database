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

- Posons $k^{*}(n,m)$ le coût d'un chemin optimal de $n$ à $m$ (qui vaut $+\infty$ s'il n'existe pas de chemin tel)
- $g^*(n) = k^*(n_{0}, n)$ est le coût du meilleur chemin pour joindre $n$ depuis $n_{0}$
- $h^{*}(n) = \min_{\gamma \in \Gamma}k^*(n, \gamma)$ est le plus petit coût permettant de joindre $n$ à un état but
- $f^{*}(n) = g^{*}(n) + h^{*}(n)$ le coût du meilleur chemin solution passant par $n$

On pose $g$ et $h$ les fonctions caractérisant le meilleur chemin actuellement connu
