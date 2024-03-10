#algebre 

## Définition
Pour $M = (m_{ij}) \in M_n(A)$ on définit le déterminant de cet matrice comme: #!
$$det(M) = \sum_{\sigma \in S_n}\epsilon(\sigma)\prod_{i=1}^nm_{\sigma(i)i}$$
<!--ID: 1710069542118-->
**Remarque**: C'est exactement ce que l'on retrouve dans [[Formes n-linéaires alternées#Proposition|la proposition de det(u)]]

### Exemple
On peut observer dans le cas $n=2$ que pour
$$M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$$
On a par définition, que son déterminant est donné par $det(M) = ad-bc$
comme on pourrait effectivement s'y attendre.


## Théorèmes sur le déterminant d'une matrice
Pour $M \in M_n(A)$ on a les propriétés suivantes: #!
1. $det(M) = \prod_{i=1}^nm{ii}$ pour $M$ une matrice triangulaire supérieure
2. $det(M) = det(^tM)$
3. $\forall M, M' \in M_n(A), det(MM')=det(M)det(M')$
<!--ID: 1710069515037-->

### Preuve

On commence d'abord par montrer (1)
Si $M$ est triangulaire supérieure, alors vérifions que pour tout $\sigma \not = Id$ on a qu'il existe $i$ tel que $m_{\sigma(i)i} = 0$, autrement dit, que $\sigma(i) > i$
 
