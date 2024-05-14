## Définition intuitive
Soit $G = (V, E)$ un [[Graphes non orientés]] ou [[Graphes orientés|orienté]] et un sommet $s \in V$. A partir de l'origine $s$ , on visite les sommet le long de la chaîne élémentaire jusqu'à arriver à un sommet sans voisin non visité. On revient alors au dernier sommet sur la chaîne avec un voisin non visité et on recommence.

## Définition
Un parcours en profondeur est un [[Parcours en largeur]] où l'on va visiter le dernier sommet ouvert plutôt que le premier.

On définit un parcours en profondeur mathématiquement de la façon suivante: #!

Soit $G=(V, E)$ un [[Graphes non orientés]] ou [[Graphes orientés|orienté]] et $L=(v_1, \dots, v_n)$ un parcours de $G$.
Ce parcours $L$ est dit *"en profondeur"* si pour tout sous-parcours $L_k = (v_1, \dots, v_k)$ le sommet $v_{k+1}$ est un sommet adjacent au ==dernier== sommet [[Parcours#Sommet ouvert et fermé|ouvert]] de $L_k$

## [[Graphes de liaison]] en profondeur

On définit un graphe de liaison en profondeur de la façon suivante: #!

Soit $G = (V, E)$ un [[Graphes non orientés]] qui est [[Graphes non orientés#Connexité|connexe]], et $L = (v_1, \dots, v_n)$ un parcours en profondeur de $G$
On donne le graphe orienté $\mathcal A^*(L) = (V(L), H(L))$ le graphe de liaison en profondeur si:
- $\mathcal A^*(L) = (V(L), H(L))$ est un [[Graphes de liaison]] de $L$
- Pour tout sous-parcours $L_k =(v_1, \dots, v_k)$, $v_{k+1}$ a pour prédécesseur le dernier sommet ouvert de $L_k$
Notons que le graphe de liaison en largeur ==est unique==

## Implémentation d'un parcours en profondeur
Observons qu'un parcours en profondeur se fait plus naturellement de façon [[Fonctions récursives|récursive]].
On donne alors la fonction pour construire un parcours en profondeur d'origine $s$ la fonction ci-dessous

```
function DFS(G, s)
	visite[s] := True, L := (s)
	for all {s,u} in E
		if not visite[u]
			L := L + DFS(G, u)
		end if
	end for
	return L
end function
```

## Post et pré visite
On définit les instants post-visite et les instants pré-visite de la façon suivante: #!

Soit $G = (V, E)$ un [[Graphes non orientés]] et $L$ un parcours en profondeur tel que $n = |V|$. On numérote de $1$ à $2n$ les instants où l'on rentre et l'on sort de la [[#Implémentation d'un parcours en profondeur|fonction]] `DFS`.
On donne les instants de post-visite et de pré-visite les deux fonctions $\text{post}$ et $\text{pre}$ allant de $V$ vers $\set{1, \dots, 2n}$ telles que:
- $\text{pre}(u)$ est l'instant où le sommet $u$ est visité (i.e `DFS(G, u)` vient d'être appelé)
- $\text{post}(u)$ est l'instant où l'on sort de la fonction `DFS(G, u)`

## Intervalles
Pour tout couple de sommets $(u,v) \in V^2$ avec $u \not = v$, les intervalles $[\text{pre}(u), \text{post}(u)]$ et $[\text{pre}(v), \text{post}(v)]$ sont tels que: #!

- $[\text{pre}(u), \text{post}(u)] \cap [\text{pre}(v), \text{post}(v)] = \emptyset$
- $[\text{pre}(u), \text{post}(u)] \subset [\text{pre}(v), \text{post}(v)]$
- $[\text{pre}(v), \text{post}(v)] \subset [\text{pre}(u), \text{post}(u)]$

## Descendant et ancêtres
Pour $\mathcal A = (V, A)$ une [[Graphes orientés#Arborescence|arborescence]]. On définit les termes suivants: #!

- Soit deux sommets $(u,v) \in V^2$ avec $u \not =v$. $u$ est un descendant de $v$ s'il existe un [[Graphes orientés#Chemin|chemin]] dans $\mathcal A$ de $v$ vers $u$ 
- Soit deux sommets $(u,v) \in V^2$ avec $u \not =v$. $u$ est un ancêtre de $v$ s'il existe un [[Graphes orientés#Chemin|chemin]] dans $\mathcal A$ de $u$ vers $v$ 