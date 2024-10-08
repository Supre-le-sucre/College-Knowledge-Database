## Définition
Soit $E$ un $\mathbb K$-espace vectoriel de dimension finie $n$ et $u \in \mathcal L(E)$. On dit que $u$ est trigonalisable si #!
Il existe une base $B$ dans laquelle $Mat_B(u)$ est une [[Matrices triangulaire supérieure]]
<!--ID: 1715537862457-->


De la même manière on dit qu'une matrice $M_n(\mathbb K)$ est trigonalisable si elle est semblable à une matrice triangulaire supérieure

## Lemme: similitude des matrices triangulaires
On observe le phénomène suivant: #!

Si une matrice $M$ est triangulaire inférieure alors elle est semblable à une matrice triangulaire supérieure
<!--ID: 1715537862458-->


### Preuve
Il suffit simplement de prendre la transformation de transposition en tant que matrice.

Notons $T_n^{(1)}(\mathbb K)$ l'espace vectoriel représentant les matrices triangulaires inférieures.
On pose la matrice $D$ antidiagonale correspondant au changement de base $(e_1, \dots, e_n) \to (e_n, \dots, e_1)$. Alors l'isomorphisme est de $M_n(\mathbb K)$ est donné par $DMD^{-1}$ et envoie $T_n(\mathbb K)$ sur $T_n^{(1)}(\mathbb K)$
$$\tag*{$\blacksquare$}$$
## Définition d'un drapeau
Soit $E$ un $\mathbb K$-espace vectoriel. On appelle drapeau de $E$: #!

Toute de suite de sous-espaces vectoriel de $E$ satisfaisant: $$\{0\} = E_0 \subset E_1 \subset \cdots \subset E_n = E$$ avec $\dim(E_i) = i$
<!--ID: 1715537862460-->


## Lemme trigonalisation et stabilité d'un drapeau
On observe le phénomène suivant: #!

Soit $u \in \mathcal L(E)$, on a que $u$ est trigonalisable si et seulement si $u$ [[Espaces stables et codiagonalisation|stabilise]] un drapeau de $E$
<!--ID: 1715537862462-->


### Preuve
$\Rightarrow$ 
On pose $B = (e_1, \dots, e_n)$ la base qui trigonalise $u$. Il suffit de considérer le drapeau:
$E_i = Vect(e_1, \dots, e_i)$ avec $E_0 = \{0\}$

$\Leftarrow$
Réciproquement, si $u$ stabilise un drapeau de $E$, alors pour toit $i \in [1,n]$, on a que $E_{i-1}$ est un hyperplan de $E_i$ de tel sorte que:
$$E_i = E_{i-1} \oplus \mathbb Ku_i$$
avec $u_i \not = 0$, on écrit alors $u$ dans la base $B= (u_1, \dots, u_n)$
