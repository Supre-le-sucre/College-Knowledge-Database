## Définition
Le parcours en largeur est un [[Parcours]] défini de la façon suivante: #!

Soit $G = (V, E)$ un [[Graphes non orientés]] qui est [[Graphes non orientés#Connexité|connexe]].
Un parcours $L=(v_1, \dots, v_n)$ est dit *"en largeur"* si pour tout sous parcours $L_k = (v_1, \dots, v_k)$ on a que $v_{k+1}$ est un sommet adjacent du premier sommet [[Parcours#Sommet ouvert et fermé|ouvert]] de $L_k$
Autrement dit, pour parcourir en largeur, on regarde tous les sommets adjacents à un sommet jusqu'à qu'il soit [[Parcours#Sommet ouvert et fermé|fermé]]. Ensuite, on le refait avec le prochain sommet [[Parcours#Sommet ouvert et fermé|ouvert]]
<!--ID: 1715702538597-->


## [[Graphes de liaison]] en largeur
On définit un graphe de liaison en largeur de la façon suivante: #!

Soit $G = (V, E)$ un [[Graphes non orientés]] qui est [[Graphes non orientés#Connexité|connexe]], et $L = (v_1, \dots, v_n)$ un parcours en largeur de $G$
On donne le graphe orienté $\mathcal A^*(L) = (V(L), H(L))$ le graphe de liaison en largeur si:
- $\mathcal A^*(L) = (V(L), H(L))$ est un [[Graphes de liaison]] de $L$
- Pour tout sous-parcours $L_k =(v_1, \dots, v_k)$, $v_{k+1}$ a pour prédécesseur le premier sommet ouvert de $L_k$
Notons que le graphe de liaison en largeur ==est unique==
<!--ID: 1715702538602-->


## Propriété sur la plus courte [[Graphes non orientés#Chaîne|chaîne]]
Observons que pour un parcours en largeur d'un graphe $G=(V, E)$ d'origine $s$: #!

Pour tout sommet $u \in V$, le chemin de $s$ à $u$ de $\mathcal A^*(L)$ est associé à la plus courte [[Graphes non orientés#Chaîne|chaîne]] de $G$ entre $s$ et $u$
Ainsi donc $\text{dist}_s(u)$ est égale à la distance du chemin de $s$ à $u$ dans $\mathcal A^*(L)$
<!--ID: 1715702538606-->


## Implémentation d'un parcours en largeur

On peut observer l'implémentation d'un parcours en largeur de $G=(V, E)$ d'origine $s$ comme suit:
(cf. [[Files]] du cours de Structure de données)

```
for all u in V
	dist[u] := infinity
end for

L := (), Enfiler(F, s), dist[s] := 0
while F not empty do
	u := Defiler(F), L := L + (u)
	for all {u,v} in E
		if dist[v] = infinity then
			Enfiler(F, v), dist[v] = dist[u] + 1
		end if
	end for
end while
``