## Définition
Soit $(\Omega, \mathcal F)$ et $(\Omega', \mathcal F')$ deux espaces mesurables. Une application de $f: \Omega \to \Omega'$ est dite mesurable si et seulement si
$$\forall A \in \mathcal F', f^{-1}(A) \in \mathcal F$$
Remarquons que la mesurabilité d'une fonction ne dépend aucunement de la mesure.
### Exemple
- Tout application constante de $\Omega$ dans $\mathbb R$ est mesurable
	En effet pour $f = k$ si on considère l'espace mesurable $(\Omega, \mathcal F)$ on a que
	$\forall A \in \mathcal P(\Omega)$, si $k \in A$, alors $f^{-1}(A) = \Omega \in \mathcal F$, sinon $f^{-1}(A) = \emptyset \in \mathcal F$ (cf. [[Maths/LU2MA211-Lebesgue/Tribu#Propriétés issue de la définition|Tribu]])

- ==Les fonctions indicatrices==
	Soit $(\Omega, \mathcal F)$ un espace mesurable, en prenant $E \subset \Omega$ on a que:
	$\mathbb 1^{-1}(1) = E$ et $\mathbb 1^{-1}(0) = E^c$. 
	Ainsi donc $\mathbb 1_{E}$ mesurable $\Leftrightarrow$ $E \in \mathcal F$ ($E$ mesurable)

- Les suites numériques
	 Les suites numériques sont des applications de $\mathbb{N}$ dans $\mathbb R$
	 Il est naturel de prendre comme tribu de $\mathbb N$, l'ensemble $\mathcal P(\mathbb N)$
	 Et l'image réciproque d'une telle application sera toujours dans $\mathcal P(\mathbb N)$.
	 Ainsi donc, toutes les suites numériques sont mesurables à condition d'être d'avoir ces images dans n'importe quel ensemble mesurable


### Similitude avec la définition de continuité topologique
Une application $f: E \to E'$ entre deux espaces métriques est continue si et seulement si
$$\forall \mathcal O \subset E' \text{ ouvert}, f^{-1}(\mathcal O) \subset E \text{ ouvert}$$
C'est en réalité une simple généralisation de la propriété de continuité sur $\mathbb R$ 

## Simplification du critère de mesurabilité
### Proposition
Soient $(\Omega, \mathcal F)$ et $(\Omega', \mathcal F')$ deux espaces mesurables, et soit $f: \Omega \to \Omega'$.
S'il existe $\mathcal C \subset \mathcal P(\Omega')$ telle que $\sigma(\mathcal C) = \mathcal F'$ ([[Tribu#Tribu engendrée|Tribu engendrée]]) avec
$$\forall C \in \mathcal C, f^{-1}(C) \in \mathcal F$$ alors $f$ est mesurable

### Preuve
On pose l'ensemble $\mathcal F_{f}= \set{A \subset \Omega' \; | \; f^{-1}(A) \in \mathcal F}$
Montrons que cet ensemble est une [[Tribu]] 

- Stabilité par complémentaire
	Soit $A \in \mathcal F_f$ donc $f^{-1}(A) \in \mathcal F$. Par stabilité du complémentaire de $\mathcal F$ on a que $(f^{-1}(A))^c \in \mathcal F$
	Or $f^{-1}(A) = \set{x \in \Omega \; | \; f(x) \in A}$ d'où $(f^{-1}(A))^{c} = \set{x \in \Omega \; | \; f(x) \not \in A}=f^{-1}(A^c)$ 
	Donc $f^{-1}(A^{c}) \in \mathcal F$ d'où $A^{c}\in \mathcal F_f$ stable par complémentaire

- Stabilité par union dénombrable
	Soit $A_{i}\in \mathcal F_f^{\mathbb N}$, On a alors que $\bigcup_{i \in \mathbb N}f^{-1}(A_{i})\in \mathcal F$ par stabilité d'union dénombrable de $\mathcal F$ 
	Or $\bigcup_{i \in \mathbb N}f^{-1}(A_{i})= \set{x \in \Omega \; | \; \exists i, f(x) \in A_{i}}= f^{-1}(\bigcup_{i \in \mathbb N} A_i)$
	Donc  $\bigcup_{i \in \mathbb N} A_{i}\in \mathcal F_f$ stable par union dénombrable

$\mathcal F_f$ est donc bien une tribu.
Or $\mathcal C \subset \mathcal F_{f}$ par définition. Et comme $\mathcal F_f$ une tribu, $\mathcal F_{f}$ contient $\sigma(\mathcal C) = \mathcal F'$ par [[Tribu#Tribu engendrée|tribu engendrée]]

