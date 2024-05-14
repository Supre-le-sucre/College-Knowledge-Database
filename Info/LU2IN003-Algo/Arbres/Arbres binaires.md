#algo
## Définition
Un arbre binaire est défini inductivement de la façon suivante. #!

Soit $T$ l'ensemble des arbres binaires étiquetés sur $E$ est tel que:
- $\emptyset \in T$
- $(x, G, D) \in T$, où $x \in E$, et $G, D \in T$ avec ($G$ la branche gauche et $D$ la branche droite)

## Primitives
- `AB(x, G, D)` renvoie l'arbre de racine $x$ et de branche gauche $G$ et droite $D$
- `ABvide()` renvoie l'arbre vide
- `estABvide(T)` renvoie vraie si l'arbre $T$ est vide.

L'ensemble de ces primitives sont en $\Theta(1)$

## Accès
Les accès sur un arbre $T$ sont immédiat, donc $\Theta(1)$
- `T.clef` désigne l'étiquette courante de $T$
- `T.gauche`, `T.droit` renvoie respectivement la branche gauche et droite de $T$

## Ensembles pratiques des arbres
### Nœuds
Les nœuds d'un arbre binaire sont sa racine, les nœuds de sont sous arbre gauche puis le nombre de nœuds du sous arbre droit. On note l'ensemble de ces éléments $\mathcal N(T)$ définie inductivement comme: #!
- $\mathcal N(\emptyset) = \emptyset$
- $\mathcal N(x, G, D) = \set{x} \cup \mathcal N(G) \cup \mathcal N(D)$

### Feuille
Une feuille est un nœuds dont les deux fils sont vides, on note l'ensemble de ces éléments $\mathcal F(T)$ définie inductivement comme: #!
- $\mathcal F(\emptyset) = \emptyset$
- $\mathcal F(x, G, D) = \set{x} \cup \mathcal F(G) \cup \mathcal F(D)$

### Nœuds internes
Un nœuds interne est un nœud qui n'est pas une feuille. On note l'ensemble de ces éléments $\mathcal I(T)$ définie inductivement comme: #!
- $\mathcal I(\emptyset) = \emptyset$
- $\mathcal I(x, \emptyset, \emptyset) = \emptyset$
- $\mathcal I(x, G, D) = \set{x} \cup \mathcal I(G) \cup \mathcal I(D)$

## Fonctions importantes

### Taille d'un arbre
La taille d'un arbre est définie par son nombre de nœuds dont la fonction `n(T)` renvoyant le cardinal de $\mathcal N(T)$ définie inductivement de la façon suivante: #!

- `n(ABVide())` renvoie 0
- `n(AB(x, G, D))` renvoie `1 + n(G) + n(D)`

### Hauteur d'un arbre
La hauteur d'un arbre est donné par le nombre de branche qu'il contient. On note `h(T)` la fonction renvoyant la hauteur d'un arbre définie de la façon suivante: #!

- `h(ABVide())` renvoie 0
- `h(AB(x, G, D)` renvoie  `1 + max(h(G), h(D))`

### Complexité en $\Theta(n)$
Pour un arbre $T$, de taille $n$, la complexité des fonctions `n(T)` et `h(T)` est de #!
$$\Theta(n)$$

#### Preuve
Soit la fonction suivante:
```python
def ABTaille(T):
	if estABvide(T):
		return 0
	else:
		return 1 + ABTaille(T.gauche) + ABTaille(T.droit)
```

Montrons que sa complexité est de $\Theta(n)$ en posant $c(T)$ le nombre d'addition effectuées par `ABTaille(T)`

Par induction sur $T \in AB$, on prends $P(T):$ "$c(T)$ = 2`ABTaille(T)`"

Initialisation: `ABTaille(ABvide()) = 0` pas d'addition à faire, donc $c(T) = 0$ et on a bien $P(0)$

Hérédité: Soit $G, D \in AB$ vérifiant $P(G)$ et $P(D)$
$c(T) = c(G) + c(D) + 2$
$c(T) =$ 2`ABTaille(G)` + 2`ABTaille(D)` + 2 = 2(`ABTaille(G)` + `ABTaille(D)` + 1) = 2`ABTaille(T)`
$$\tag*{$\blacksquare$}$$
## Relations entre la hauteur et la taille d'un arbre
### Théorème
On observe la relation suivante entre la taille d'un arbre et sa hauteur: #!
Pour tout arbre de taille $n$ et de hauteur $h$ on a: $h \leq n \leq 2^h-1$

### Corollaire
De fait à partir de la relation entre la taille d'un arbre et sa hauteur on en déduit l'encadrement de sa hauteur suivant: #!
Pour tout arbre de taille $n$ et de hauteur $h$ on a: $log_2(n+1)\leq h \leq n$

## Parcours d'arbre binaire
Pour parcourir un arbre, la complexité est en #!
$$\Theta(n)$$

On énumère les parcours définis inductivement suivants pour un arbre: #!

- Préfixe
	$\text{pre}(\emptyset) = \text{""}$
	$\text{pre}((x, G, D)) = x.\text{pre}(G).\text{pre}(D)$
- Infixe
	$\text{inf}(\emptyset) = \text{""}$
	$\text{inf}((x, G, D)) = \text{inf}(G).x.\text{inf}(D)$
- Suffixe
	$\text{suf}(\emptyset) = \text{""}$
	$\text{suf}((x, G, D)) = \text{suf}(G).\text{pre}(D).x$

