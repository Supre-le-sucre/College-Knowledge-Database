## Définition
Soit $E$ un $\mathbb K$-espace vectoriel de dimension finie $n$ et $u \in \mathcal L(E)$. On dit que $u$ est trigonalisable si #!
Il existe une base $B$ dans laquelle $Mat_B(u)$ est une [[Matrices triangulaire supérieure]]

De la même manière on dit qu'une matrice $M_n(\mathbb K)$ est trigonalisable si elle est semblable à une matrice triangulaire supérieure

## Lemme: similitude des matrices triangulaires
On observe le phénomène suivant: #!

Si une matrice $M$ est triangulaire inférieure alors elle est semblable à une matrice triangulaire supérieure

### Preuve
Il suffit simplement de prendre la transformation de transposition en tant que matrice.

Notons $T_n^{(1)}(\mathbb K)$ l'espace vectoriel représentant les matrices triangulaires inférieures.
On pose la matrice $D$ antidiagonale correspondant au changement de base $(e_1, \dots, e_n) \to (e_n, \dots, e_1)$. Alors l'isomorphisme est de $M_n(\mathbb K)$ est donné par $DMD^{-1}$ et envoie $T_n(\mathbb K)$ sur $T_n^{(1)}(\mathbb K)$
$$\tag*{$\blacksquare$}$$
