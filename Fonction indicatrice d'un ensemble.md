Soit un univers $\Omega$, avec $A \in \mathcal{P}(\Omega)$.
On définit la fonction indicatrice de l'ensemble A telle que:
$$\mathbb{1}_A : \Omega \to \set{0,1}$$
$$
\forall x \in A, \mathbb{1}_A(x) = \begin{cases} 
      0 & x\not \in A\\
      1 & x \in A 
   \end{cases}
\
$$

## Propriétés
Dans la suite, on pose $\Omega$ un ensemble avec, $A, B \in \mathcal{P}(\Omega)$
### Egalité de deux ensembles
$$ \mathbb{1}_A = \mathbb{1}_B \Leftrightarrow A=B$$
**Démonstration**:
$\Rightarrow$
Soit $\mathbb{1}_A = \mathbb{1}_B$
Montrons que $A=B$ par double inclusion:
- Soit $x \in A$, $\mathbb{1}_A(x) = 1$, puisque $\mathbb{1}_A = \mathbb{1}_B$, $\mathbb{1}_B(x) = 1$, donc $x \in B$, finalement $A \subseteq B$
- Soit $x \in B$, $\mathbb{1}_B(x) = 1$, puisque $\mathbb{1}_A = \mathbb{1}_B$, $\mathbb{1}_A(x) = 1$, donc $x \in A$, finalement $B \subseteq A$
Puisqu'on a $A \subseteq B$ et $B\subseteq A$, on a indubitablement $A=B$

$\Leftarrow$
Soit $A = B$
Montrons que $\mathbb{1}_A = \mathbb{1}_B$, autrement dit: $\forall x \in \Omega, \mathbb{1}_A(x) = \mathbb{1}_B(x)$
Soit $x \in \Omega$
- Si $x \in A$ alors $\mathbb{1}_A(x) = 1$. Puisque $A=B$, $x \in B$, donc $\mathbb{1}_B(x) =1$, dans ce cas: $\mathbb{1}_A(x) = \mathbb{1}_B(x)$
- Si $x \not \in A$ alors $\mathbb{1}_A(x) = 0$. Puisque $A=B$, $x \not \in B$, donc $\mathbb{1}_B(x) =0$, dans ce cas: $\mathbb{1}_A(x) = \mathbb{1}_B(x)$
Dans tous les cas on a bien que $\mathbb{1}_A = \mathbb{1}_B$ 




