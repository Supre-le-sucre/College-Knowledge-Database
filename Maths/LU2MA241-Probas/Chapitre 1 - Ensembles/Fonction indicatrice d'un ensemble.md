#probas 
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
Dans la suite, on pose $\Omega$ un ensemble avec $A, B \in \mathcal{P}(\Omega)$
### Egalité de deux ensembles
$$ \mathbb{1}_A = \mathbb{1}_B \Leftrightarrow A=B$$
#### Démonstration
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

### Inclusion de deux ensembles
$$ A \subseteq B \Leftrightarrow \forall x \in \Omega, \mathbb{1}_A(x) \leq \mathbb{1}_B(x)$$

#### Démonstration
$\Rightarrow$
Soit $A \subseteq B$
Montrons que $\forall x \in \Omega, \mathbb{1}_A(x) \leq \mathbb{1}_B(x)$
Soit $x \in \Omega$
- Si $x \in A$, par hypothèse, on a $x \in B$, dans ce cas $\mathbb{1}_A(x) = \mathbb{1}_B(x) =1$ donc $\mathbb{1}_A(x) \leq \mathbb{1}_B(x)$
- Si $x \in B \setminus A$, on a $\mathbb{1}_A(x) =0$ et $\mathbb{1}_B(x) =1$ donc $\mathbb{1}_A(x) \leq \mathbb{1}_B(x)$
- Si $x \not \in A \cup B$ dans ce cas $\mathbb{1}_A(x) = \mathbb{1}_B(x) =0$ donc $\mathbb{1}_A(x) \leq \mathbb{1}_B(x)$

$\Leftarrow$
Supposons $\forall x \in \Omega, \mathbb{1}_A(x) \leq \mathbb{1}_B(x)$
Montrons que $A \subseteq B$

Soit $x \in A$, on a alors par hypothèse que $\mathbb{1}_A(x) \leq \mathbb{1}_B(x)$
En l'occurrence, puisque $x \in A$, on a $\mathbb{1}_A(x)=1$.
Puisque $\forall x \in \Omega, \mathbb{1}_B(x) = 0$ ou $1$, on a donc que $\mathbb{1}_B(x) =1$ par respect de l'hypothèse.
Ceci implique alors que $x \in B$, d'où $A \subseteq B$







### Intersection de deux ensembles
$$ \mathbb{1}_{A \cap B} = \mathbb{1}_A \times \mathbb{1}_B = \min(\mathbb{1}_A, \mathbb{1}_B)$$
#### Démonstration
On pose $f := \mathbb{1}_A \times \mathbb{1}_B$ et soit $x \in \Omega$
- Si $x \in A \cap B$, $\mathbb{1}_A(x) = \mathbb{1}_B(x) = 1$ et on a bien $f(x) = 1$
- Si $x \not \in A \cap B$, trois possibilités sont à développer
	- Si $x \in A$, $\mathbb{1}_A(x) = 1$ et $\mathbb{1}_B(x) =0$ donc $f(x) = 0$
	- Si $x \in B$, $\mathbb{1}_B(x) = 1$ et $\mathbb{1}_A(x) =0$ donc $f(x) = 0$
	- Si $x \not \in A \cup B$, $\mathbb{1}_A(x) = \mathbb{1}_B(x) = 0$, donc $f(x) =0$

Ainsi donc remarquons plus brièvement que, $\forall x \in \Omega$:
- Si $x \in A \cap B, f(x) =1$
- Si $x \not \in A \cap B, f(x) = 0$
D'où la possibilité d'affirmer $f := \mathbb{1}_{A \cap B}$, d'où $\mathbb{1}_{A\cap B} = \mathbb{1}_A \times \mathbb{1}_B$

### Complémentaire d'un ensemble
$$ \mathbb{1}_{\overline{A}} = 1 - \mathbb{1}_A$$
#### Démonstration
On pose $f := 1 - \mathbb{1}_A$ et soit $x \in \Omega$
- Si $x \in A$, on a $\mathbb{1}_A(x) = 1$, d'où $f(x) = 0$
- Si $x \not \in A$, on a $\mathbb{1}_A(x) = 0$, d'où $f(x) = 1$

Ainsi donc remarquons plus brièvement que, $\forall x \in \Omega$
- Si $x \in \overline{A}, f(x) = 1$
- Si $x \not \in \overline{A}, f(x) =0$
D'où la possibilité d'affirmer, $f := \mathbb{1}_{\overline{A}}$, d'où $\mathbb{1}_{\overline{A}} = 1 - \mathbb{1}_A$

### Réunion d'un ensemble
$$ \mathbb{1}_{A \cup B} = \mathbb{1}_A + \mathbb{1}_B - \mathbb{1}_A \times \mathbb{1}_B = \max(\mathbb{1}_A, \mathbb{1}_B)$$

#### Démonstration
On pose $f:= \mathbb{1}_A + \mathbb{1}_B - \mathbb{1}_A \times \mathbb{1}_B$, et soit $x \in \Omega$
- Si $x \in A \cup B$, on a deux possibilités:
	- Si $x \in A$, $\mathbb{1}_A(x) = 1$, peu importe la valeur de $\mathbb{1}_B(x)$, on a $f(x) = 1$
	- Si $x \in B$, $\mathbb{1}_B(x) = 1$, peu importe la valeur de $\mathbb{1}_A(x)$, on a $f(x) = 1$
- Si $x \not \in A \cup B$, on a $\mathbb{1}_A(x) = \mathbb{1}_B(x) = 0$, donc $f(x)= 0$

Ainsi donc remarquons plus brièvement que, $\forall x \in \Omega$
- Si $x \in A \cup B, f(x) = 1$
- Si $x \not \in A \cup B, f(x) = 0$
D'où la possibilité d'affirmer, $f := \mathbb{1}_{A \cup B}$, d'où $\mathbb{1}_{A \cup B} = \mathbb{1}_A + \mathbb{1}_B - \mathbb{1}_A \times \mathbb{1}_B$

