## Propriété du déterminant par bloc
On donne la propriété suivante: #!

Soit la matrice donné par blocs $M = \begin{pmatrix}B & C \\ 0 & Q\end{pmatrix}$ avec $B \in M_p(A), Q \in M_r(A), C \in M_{p,r}(A)$. On a l'égalité suivante: $\det(M) = \det(B)\det(Q)$

### Preuve
Commençons à traiter le cas d'un corps $\mathbb K$.

On utilise ici la [[Multi linéarité du déterminant]]
Si $B$ n'est pas inversible, ses colonnes sont liées, ce qui signifie que les $p$ première colonne de la matrice $M$ sont liées. On a $\det(M) = 0 = \det(B)\det(Q)$

Sinon, si $B$ est inversible on peut écrire: 
$$\begin{pmatrix}B & C \\ 0 & Q\end{pmatrix} = \begin{pmatrix}B & 0 \\ 0 & Id\end{pmatrix} \begin{pmatrix}Id & B^{-1}C \\ 0 & Q\end{pmatrix}$$
Continuons. Observons cette fois que si $Q$ n'est pas inversible, alors ses lignes sont liées, ça sera le cas aussi donc pour les $r$ dernières lignes de $M$. De la même manière on a donc $\det(M) = 0 = \det(B)\det(Q)$ 
Autrement on a alors que:
$$\begin{pmatrix}Id & B^{-1}C \\ 0 & Q\end{pmatrix} = \begin{pmatrix}Id & B^{-1}CQ^{-1} \\ 0 & Id\end{pmatrix}\begin{pmatrix}Id & 0 \\ 0 & Q\end{pmatrix}$$
d'où finalement:
$$\begin{pmatrix}B & C \\ 0 & Q\end{pmatrix} = \begin{pmatrix}B & 0 \\ 0 & Id\end{pmatrix} \begin{pmatrix}Id & B^{-1}CQ^{-1} \\ 0 & Id\end{pmatrix}\begin{pmatrix}Id & 0 \\ 0 & Q\end{pmatrix}$$
Soit
$$\det\begin{pmatrix}B & C \\ 0 & Q\end{pmatrix} = \det\begin{pmatrix}B & 0 \\ 0 & Id\end{pmatrix} \det\begin{pmatrix}Id & B^{-1}CQ^{-1} \\ 0 & Id\end{pmatrix}\det\begin{pmatrix}Id & 0 \\ 0 & Q\end{pmatrix}$$

La matrice centrale est une matrice triangulaire, on applique [[Déterminant matriciel#Théorèmes sur le déterminant d'une matrice|le théorème du déterminant pour les matrices triangulaires]]:
$$\det\begin{pmatrix}Id & B^{-1}CQ^{-1} \\ 0 & Id\end{pmatrix} = 1$$

Calculons maintenant $\det\begin{pmatrix}B & 0 \\ 0 & Id\end{pmatrix}$
Pour cela, commençons à prendre le déterminant en fonction de la $p+1$ ème ligne. C'est là que commence la sous matrice identité. Sur cette ligne, il n'y a qu'un seul et unique $1$, celui de la matrice identité.
Remarquons que ce $1$ est forcément sur la diagonale de la matrice $M$ car $B$ est une matrice carrée. De fait, le coefficient devant le déterminant extrait est positif:
$$\det\begin{pmatrix}B & 0 \\ 0 & Id_r\end{pmatrix} = 1.\det\begin{pmatrix}B & 0 \\ 0 & Id_{r-1}\end{pmatrix} =\det\begin{pmatrix}B & 0 \\ 0 & Id_{r-1}\end{pmatrix}$$
En effet, en commençant par la $p+1$ ème ligne pour le déterminant, on ne coupe pas la matrice $B$ car la $p+1$ ème colonne et ligne ne la contient pas. De plus, en supprimant cet espace de la matrice, nous n'avons en fait que réduit la sous matrice identité de $1$.
Les $1$ sont toujours sur la diagonale de la matrice en raison du fait que $B$ est une matrice carrée. Le coefficient du déterminant reste toujours positif.
En réitérant le procédé on obtient finalement:
$$\det\begin{pmatrix}B & 0 \\ 0 & Id_r\end{pmatrix} = \det(B)$$

Le même cas de figure se présente pour calculer $\det\begin{pmatrix}Id & 0 \\ 0 & Q\end{pmatrix}$
Cette fois-ci on prends la toute première colonne de la matrice et on continue jusqu'à atteindre la $p$ ème. Et on en déduit le même résultat que précédemment:
$$\det\begin{pmatrix}Id & 0 \\ 0 & Q\end{pmatrix} = \det(Q)$$

Finalement on a:
$$\det(M)=\det\begin{pmatrix}B & C \\ 0 & Q\end{pmatrix} = \det\begin{pmatrix}B & 0 \\ 0 & Id\end{pmatrix} \det\begin{pmatrix}Id & B^{-1}CQ^{-1} \\ 0 & Id\end{pmatrix}\det\begin{pmatrix}Id & 0 \\ 0 & Q\end{pmatrix} = \det(B).1.\det(Q)$$
D'où
$$\det(M) = \det(B)\det(Q)$$

Dans le cas général, il suffit de voir cet égalité comme une identité polynomiale dans $\mathbb Z[B_{ij}, Q_{ij}, C_{ij}]$ que l'on plonge dans le corps $\mathbb Q(B_{ij}, Q_{ij}, C_{ij})$. Comme ceci est vrai dans un corps, il est vrai pour l'anneau polynomiale $\mathbb Z$ considéré, qui peut être spécialisé en un anneau commutatif arbitraire. (La preuve est le même procédé pour montrer [[Déterminant matriciel#Théorèmes sur le déterminant d'une matrice|le point 3 de ce théorème]] dans le cas général)
$$\tag*{$\blacksquare$}$$
