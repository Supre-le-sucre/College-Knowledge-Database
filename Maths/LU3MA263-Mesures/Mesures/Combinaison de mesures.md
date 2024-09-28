## Séries de mesures
Soit $\mu_n : \mathcal E \to [0, \infty]$ des mesures sur $(E, \mathcal E)$: #!

On considère une suite $(c_n)_{n \in \mathbb N}$ ==positive== alors:
$$\forall A \in \mathcal E, \mu(A) = \sum_{n \in \mathbb N}c_n \mu_n(A)$$est une mesure


### Preuve
On vérifie les [[Mesure|axiomes d'une mesure]]:
- $\mu(\emptyset) = \sum_{n \in \mathbb N}c_n \mu_n(\emptyset) = 0$
- Soit $(A_k)_{k \in \mathbb N} \in \mathcal E^\mathbb N$ une suite d'ensemble deux à deux disjoints
$$\mu\left(\bigcup_{k \in \mathbb N}A_k\right) = \sum_{n \in \mathbb N} c_n\mu_n\left(\bigcup_{k \in \mathbb N} A_k\right)$$
Par $\sigma$-additivité on a que:
$$ = \sum_{n \in \mathbb N}c_n \sum_{k \in \mathbb N}\mu_n(A_k)$$
Et par commutativité de la somme infinie à terme positif...
$$ = \sum_{k \in \mathbb N} \sum_{n \in \mathbb N}c_n\mu_n(A_k)$$
Donc finalement
$$\mu\left(\bigcup_{k \in \mathbb N}A_k\right) = \sum_{k \in \mathbb N}\mu({A_k})$$
$$\tag*{$\blacksquare$}$$

## Mesure trace
On définit la mesure trace comme étant: #!

Soit $\mu:\mathcal E \to [0 ,\infty]$ une mesure sur $(E, \mathcal E)$.
Soit $A \in \mathcal E$ fixé, alors $\nu:\mathcal E \to [0 ,\infty]$ défini tel que
$$\forall B \in \mathcal E, \nu(B) = \mu(A \cap B)$$est une mesure que l'on appelle mesure trace


### Preuve
On vérifie les [[Mesure|axiomes d'une mesure]]:
- $\nu(\emptyset) = \mu(A \cap \emptyset) = 0$
- Soit $B_n \in \mathcal E^\mathbb N$ une suite d'ensembles 2 à 2 disjoints
$$\nu\left(\bigcup_{n \in \mathbb N} B_n \right) = \mu\left(A \cap\left(\bigcup_{n \in \mathbb N} B_n\right)\right) = \mu\left(\bigcup_{n \in \mathbb N} A \cap  B_n\right)$$
Et $A \cap B_n$ sont disjoints deux à deux donc...
$$\nu\left(\bigcup_{n \in \mathbb N} B_n \right) =\sum_{n \in \mathbb N}\mu( A \cap  B_n) = \sum_{n \in \mathbb N}\nu(B_n)$$
$$\tag*{$\blacksquare$}$$