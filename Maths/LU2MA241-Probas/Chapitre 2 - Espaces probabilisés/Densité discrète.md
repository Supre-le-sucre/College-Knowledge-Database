#probas 
## Définition
On définit une densité discrète comme suit #!
Soit $\Omega \not = \emptyset$ dénombrable. Toute fonction $p : \Omega \to \mathbb{R}$ satisfaisant:
$$\forall \omega \in \Omega,  p(\omega) \geq 0 \text{ et } \sum_{\omega \in \Omega} p(\omega) = 1$$
<!--ID: 1707597060876-->


## Propriété liant la densité discrète et la probabilité.
On a la propriété suivante: #!
Soit p une densité discrète sur un ensemble dénombrable $\Omega$. La fonction $\mathbb P : \mathcal{P}(\Omega) \to \mathbb{R}$ définie par $$\forall A \subseteq \Omega, \mathbb{P}(A) = \sum_{\omega \in A}p(\omega)$$
Satisfait l'[[Espaces probabilisés#Axiome de probabilité|axiome de probabilité]] et est donc une probabilité. 
<!--ID: 1707597086950-->

### Preuve
Il est claire que $\mathbb P(\Omega) = 1$ dans cette situation.
Il s'agit donc de montrer la deuxième partie de l'axiome, soit $(A_i)_{i \geq 1}$ disjoints
Montrons que...
$$ \mathbb P \left(\bigcup^{+\infty}_{i=1}A_i\right) = \sum^{+\infty}_{i=1}\mathbb P(A_i)$$
Sauf que là encore, l'opération est triviale car par hypothèse nous avons $\forall i \in \mathbb{N}$
$\mathbb P(A_i) = \sum_{\omega \in A_i} p(\omega)$.
Etant donné que les ensembles sont disjoints il est possible d'écrire que:
$$\mathbb P \left(\bigcup^{+\infty}_{i=1}A_i\right) = \sum_{i \in \mathbb{N}} \left(\sum_{\omega \in A_i} p(\omega) \right) = \sum^{+\infty}_{i=1}\mathbb P(A_i)$$
$$\tag*{$\blacksquare$}$$
