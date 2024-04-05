#algebre 
## Définition d'éléments orthogonaux
Des éléments $x \in E$ et $\phi \in E^\vee$ sont dits orthogonaux si #!
$$\phi(x) = \langle x, \phi \rangle = 0$$
<!--ID: 1709995298346-->


## Définition des orthogonaux de $E$ et $E^\vee$
Si $A \subset E$ alors on désigne l'orthogonal de $A$ comme étant: #!
$$A^\perp = \set{\phi \in E^\vee, \forall x \in A, \phi(x) = 0}$$
où $A^\perp \subset E^\vee$ un [[Espaces vectoriels|sous espace vectoriel]] de $E^\vee$
<!--ID: 1709995226285-->


Si $B \subset E^\vee$ alors on désigne l'orthogonal de $B$ comme étant: #!
$$B^\circ = \set{x \in E, \forall \phi \in E^\vee, \phi(x) = 0}$$
où $B^\circ \subset E$ un [[Espaces vectoriels|sous espace vectoriel]] de $E$
<!--ID: 1709995226288-->

**Remarque**: Si $\phi \in E^\vee$ alors $\set{\phi}^\circ = Ker(\phi)$

## Lemme des inclusions orthogonales
Ce lemme énonce 4 propriétés qui sont les suivantes: #!

- $A_1 \subset A_2 \subset E \Rightarrow A_2^\perp \subset A_1^\perp$
- $B_1 \subset B_2 \subset E^\vee \Rightarrow B_2^\circ \subset B_1^\circ$
- $A \subset E \Rightarrow A^\perp = Vect(A)^\perp$
- $B \subset E^\vee \Rightarrow B^\circ  = Vect(B)^\circ$
<!--ID: 1709995850711-->



## Théorème de la double orthogonalité

Soit $E$ un $\mathbb K$-[[Espaces vectoriels]] de dimension finie, $F \subset E$ et $H \subset E^\vee$ des sous-espaces vectoriels, alors on a: #!

1. $dim(F) + dim(F^\perp) = dim(E)$ et $(F^\perp)^\circ = F$
2. $dim(H) + dim(H^\circ) = dim(E)$ et $(G^\circ)^\perp = G$
<!--ID: 1709995850717-->

### Preuve

On montre d'abord (1)
Soit $r = dim(F)$ et $(e_1, \dots, e_r)$ une base de $F$ que l'on complète en $(e_1, \dots, e_n)$ pour former une base de $E$

De fait on a $F = Vect(e_1, \dots, e_r)$. D'après le [[#Lemme des inclusions orthogonales]] on a alors que $F^\perp = \set{e_1, \dots, e_r}^\perp$.

On pose $\phi \in E^\vee$ telle que $\phi = \sum\lambda_ie^*_i$
On a alors que par [[#Définition des orthogonaux de $E$ et $E vee$]]

$$\phi \in \set{e_1, \dots, e_r}^\perp \Leftrightarrow \forall i \in [1, r], \phi(e_i) = \lambda_i = 0$$
Ceci montre bien que $\phi \in F^\perp$ si et seulement si $\phi \in Vect(e_{r+1}^*, \dots, e_n^*)$  d'où l'égalité dimensionnelle $dim(F) + dim(F^\perp) = dim(E)$ vérifiée car $F^\perp = Vect(e_{r+1}^*, \dots, e_n^*)$.

Observons d'autre part que
$$x = \sum a_i e_i \in (F^\perp)^\circ \Leftrightarrow \forall i \in [r+1, n], e_i^*(x) = a_i = 0$$
Donc $x$ n'est que généré sur $Vect(e_1, \dots, e_r) = F$ d'où $F = (F^\perp)^\circ$


Pour la (2) le raisonnement est analogue
Soit $r = dim(G)$ on pose $(f_1, \dots, f_r)$ une base de $G$ complétée pour donnée $(f_1, \dots, f_n)$ une base de $E^\vee$ 

En posant $(e_1, \dots, e_n)$ une base antéduale de telle sorte que $\forall i, f_i = e_i^*$
On a donc $G = Vect(e_1^*, \dots , e_r^*)$.
On trouve ensuite par le même raisonnement que ci-dessus que $G^\circ = Vect(e_{r+1}, \dots, e_n)$ et finalement que $(G^\circ)^\perp = G$

