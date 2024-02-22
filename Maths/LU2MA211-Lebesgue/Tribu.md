#lebesgue
## Définition
Soit $\Omega$ un ensemble non vide, on définit une tribu $\mathcal{F}$ de $A$ un ensemble $\mathcal{F} \subset A$ non vide tel que
1. $\forall E \in \mathcal F$, $E^{c}\in \mathcal{F}$ (Stable par complémentaire)
2. $\forall (A_i)_{i\in\mathbb N} \in \mathcal{F}^{\mathbb N}$, $\bigcup_{n \in \mathbb N} A_{n}\in \mathcal{F}$ (Stable par union dénombrable)

## Propriétés issue de la définition
Par définition d'une tribu $\mathcal{F}$ de $\Omega$, il est aussi possible de déduire d'autre fait importants quant à sa stabilité:

1. $\emptyset$ et $\Omega \in \mathcal{F}$
	En effet, $\mathcal{F}$ est non vide, donc on a au moins $A \in \mathcal{F}$. Comme $\mathcal{F}$ est aussi stable par complémentaire,
	on a aussi l'ensemble $A^{c}\in \mathcal{F}$. 
	Or $\mathcal{F}$, stable par union dénombrable, donc $A \cup A^{c}= \Omega \in \mathcal F$
	Toujours par stabilité du complémentaire, on retrouve aussi que $\Omega^{c}=\emptyset \in \mathcal{F}$

2. $\mathcal{F}$ est stable par intersection dénombrable
	Ceci découle de la combinaison de la stabilité par complémentaire et de la stabilité par union dénombrable:
	Soit $(B_i)_{i\in \mathbb{N}} \in \mathcal{F}^{\mathbb N}$, on note $\forall i, B_{i}= A_{i}^{c}\in \mathcal{F}$ par stabilité du complémentaire.
	On a que $\bigcup_{n \in \mathbb N} A_{n}\in \mathcal F$ par stabilité de l'union dénombrable.
	Par stabilité du complémentaire $\left(\bigcup_{n \in \mathbb N} A_{n}\right)^{c}= \bigcap_{n \in \mathbb N} A_{n}^{c}= \bigcap_{n \in \mathbb N} B_{n}\in \mathcal F$

3. $\mathcal F$ est stable par exclusion: $A, B \in \mathcal F$ et $A \subset B$, on a que $B \setminus A \in \mathcal F$ 
	Ceci est une conséquence de la stabilité par intersection dénombrable et du complémentaire:
	$B \setminus A = (B \cap A^c)$ or $A^{c}\in \mathcal F$ par stabilité du complémentaire

## Tribu engendrée

### Définition
Soit $\mathcal C \in \mathcal P(\Omega)$. On définit la tribu engendrée par $\mathcal C$, noté $\sigma(\mathcal C)$ la plus petite tribu de $\Omega$ contenant l'ensemble $\mathcal C$.
On peut remarquer que $\sigma(\mathcal C)$ est l'intersection de toutes les tribus de $\mathcal P(\Omega)$ contenant $\mathcal C$

### Tribu engendrée par des partitions de $\Omega$
#### Propriété
Soit $\mathcal C = \set{P_1, \dots, P_n}$ une partition de $\Omega$, alors on a que $\sigma(\mathcal C) = \set{\bigcup_{i \in I} P_{i}| I \subset \set{1, \dots, n}}$.

## Tribu Borélienne
### Définition
Soit $(E, d)$ un espace métrique (donc $d$ une distance). On note $\mathcal O$ l'ensemble des ouverts de $E$
On appelle la tribu borélienne de $E$, noté $\mathcal B(E)$, la [[#Tribu engendrée]] par $\sigma(\mathcal O)$

On appelle par ailleurs les éléments de cette tribu les boréliens de $E$

### Exemple
Les ouverts sont évidemment des boréliens, mais les fermés aussi par stabilité complémentaire.
Les singletons sont aussi boréliens car c'est un fermé
etc.


## Tribu trace
### Définition et propriété 
Soit $\Omega$ un ensemble non vide et $\mathcal F$ une tribu de $\Omega$. On a que $A \subset \Omega$
On note $\mathcal F_{A}= \set{A \cap B, B \in \mathcal F}$ la tribu trace de $\mathcal F$ sur $A$ (Autrement dit la tribu $\mathcal F$ restreinte à $A$).
$\mathcal F_A$ est une tribu de $A$.

### Preuve
Souvenons nous que $\mathcal F_A$ est une tribu **DE** $A$

Le complémentaire d'un ensemble $B$ selon $\Omega$ s'exprime $\Omega \setminus B$
Donc le complémentaire d'un ensemble $B$ selon $A$ s'exprime $A \setminus B$

Ici un élément de $\mathcal F_A$ s'exprime $A \cap B$ d'où les preuves de stabilité suivantes:

- $\forall B \in \mathcal F, A\setminus(A\cap B) = A \cap (B^c)$ or $B^{c}\in \mathcal F$ donc $A\setminus(A\cap B) \in \mathcal F_A$ est stable par complémentaire
- $\forall (B_n) \in \mathcal F^{\mathbb N}$, $\bigcup_{n \in \mathbb N}(A \cap B_{n}) = A \cap (\cup_{n \in \mathbb N} B_n)$ et $\cup_{n \in \mathbb N} B_{n}\in \mathcal F$ donc $\bigcup_{n \in \mathbb N}(A \cap B_{n}) \in \mathcal F_A$ est stable par union dénombrable

## Trace des boréliens

### Propriété
Soit $(E, d)$ un espace métrique avec $A \subset E$, on a que $\mathcal B(E)_{A}= \mathcal B(A)$

### Preuve
Comme $\mathcal B(E)$ contient tous les ouverts de $E$, $\mathcal B(E)_A$ contient tous les ouverts de $A$
On a donc que $\mathcal B(E)_{A}\subseteq \mathcal B(A)$

Considérons maintenant $\mathcal D = \set{B \subset E, A \cap B \in \mathcal B(A)}$, on a que $\mathcal D$ une tribu des parties de $E$ (cf. [[#Preuve]]) et $\mathcal D$ contient les ouverts de $E$ et donc $\mathcal D \subseteq \mathcal B(E)$, d'où $\mathcal D_{A}\subseteq \mathcal B(E)_A$ et $\mathcal D_{A}= \mathcal B(A)$

$$\tag*{$\blacksquare$}$$

