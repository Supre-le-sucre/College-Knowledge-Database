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
Soit $\mathcal C$