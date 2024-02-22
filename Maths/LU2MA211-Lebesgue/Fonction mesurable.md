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
Autrement dit on a bien que $\forall A \in \mathcal F', f^{-1}(A) \in \mathcal F$
$$\tag*{$\blacksquare$}$$
## Toute application continue dans les mesurables est mesurable

### Propriété
Si $\Omega$ et $\Omega'$ sont deux espaces métriques munies de leur [[Tribu#Tribu Borélienne|tribu borélienne]] alors toute application continue $f: \Omega \to \Omega'$ est mesurable

### Preuve
On utilise la [[#Simplification du critère de mesurabilité|propriété précédente]] avec $\mathcal O$ l'ensemble des ouvert...

On a que $\mathcal B(\Omega') = \sigma(\mathcal{O})$ par [[Tribu#Tribu Borélienne|définition de la tribu borélienne]]
Comme $f$ est continue, on sait par [[#Similitude avec la définition de continuité topologique|définition de la continuité topologique]] que $f^{-1}(O)$ est un ouvert de $\Omega$, donc que $\forall O \in \mathcal O, f^{-1}(O) \in \mathcal B(\Omega)$  

Ainsi donc $f$ est mesurable
$$\tag*{$\blacksquare$}$$
### Conséquence: la translation est stable dans les boréliens
Soit $v \in \mathbb R ^{n}$ et $\tau_{v}:\mathbb R ^{n} \to \mathbb{R}^{n}$ tel que $x \mapsto x-v$ une translation 
La translation $\tau_v$ est continue et donc par [[#Toute application continue dans les mesurables est mesurable|la propriété précédente]] $$\forall A \subset \mathbb R^{n}, \tau_{v}(A)= A+v \in \mathcal B(\Omega)$$
Autrement dit, si $A \subset \mathbb R^n$ est un borélien, alors $\forall v \in \mathbb{R}^{n}, A+v$ l'est aussi

## Stabilité universelle des fonctions mesurables

### Proposition de la composition
Soient, $(\Omega,\mathcal F)$, $(\Omega',\mathcal F')$ et $(\Omega'',\mathcal F'')$ trois espaces mesurables.
Soit $f: \Omega \to \Omega'$ et $g: \Omega' \to \Omega''$ sont mesurables. Alors $g \circ f: \Omega \to \Omega''$ est mesurable.

#### Preuve
Soit $A \in \mathcal F''$ $(g \circ f)^{-1}(A)=f^{-1}(g^{-1}(A))$ 
Donc $g^{-1}(A) \in \mathcal F'$ et donc $f^{-1}(g^{-1}(A)) \in \mathcal F$
$$\tag*{$\blacksquare$}$$
### Proposition des fonctions composantes
Soit $f: \Omega \to \mathbb{R}^{n}$ tel que $x \mapsto (f_{1}(x)\dots, f_n(x))$
$f$ est mesurable si et seulement si l'ensemble des $f_i: \Omega \to \mathbb{R}$ le sont


### Proposition sur les opérations entre fonctions
Si $f,g:(\Omega, \mathcal F) \to \mathbb R$ sont mesurables, alors $f + g, fg, f/g$ sont mesurables