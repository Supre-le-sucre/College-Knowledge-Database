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