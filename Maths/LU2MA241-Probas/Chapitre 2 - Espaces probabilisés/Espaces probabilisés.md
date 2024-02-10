#probas
## Définition
On qualifie le triplet $(\Omega, \mathcal{F}, \mathbb{P})$ d'espace probabilisé si #!
- Soit $\Omega$ un espace d'état qui constitue notre univers
- Soit $\mathcal{F}$ une [[Tribu]] de $\Omega$ l'ensemble des événement.
- Soit une probabilité $\mathbb{P}$, une application de la forme $\mathbb{P} : \mathcal{F} \to [0,1]$ respectant l'[[#Axiome de probabilité]]
<!--ID: 1707586301874-->
## Axiome de probabilité
Soit $\Omega$ un espace d'état et $\mathcal{F}$ une [[Tribu]] de $\Omega$. On qualifie $\mathbb{P} : \mathcal{F} \to [0,1]$ une probabilité si elle vérifie l'ensemble des propriétés suivantes: #!
1. $\mathbb{P}(\Omega) = 1$
2. ($\sigma$-additivité) Pour toute suite $(A_n)_{n\geq 1}$ d'événements disjoints (i.e $\forall (i,j), i \not = j, A_i \cap A_j = \emptyset$) on a $$\mathbb{P}\left(\bigcup_{n=1}^{+\infty}A_n\right) = \sum_{n=1}^{+\infty}\mathbb{P}(A_n)$$
**Remarque:** la $\sigma$-additivité entraîne l'additivité finie entre événement disjoints.
<!--ID: 1707586321110-->

## Propriétés fondamentales
### Privatisation avec inclusion
On considère l'[[Espaces probabilisés]] $(\Omega, \mathcal{F}, \mathbb{P})$ Soit $A,B \in \mathcal{F}$ avec $A \subseteq B$. Il est possible de déduire une propriété pour $\mathbb{P}(B \setminus A)$ #!
$$ \mathbb{P}(B \setminus A) = \mathbb P(B) - \mathbb P(A)$$
Plus particulièrement, on observe que: $\mathbb P(A) \leq \mathbb P(B)$ et que $\mathbb P(A^c) = 1 - \mathbb P(A)$ 
<!--ID: 1707588267113-->

### Union de deux événements
On considère l'[[Espaces probabilisés]] $(\Omega, \mathcal{F}, \mathbb{P})$ Soit $A,B \in \mathcal{F}$. Il est possible de déduire une propriété pour $\mathbb{P}(A \cup B)$ #!
$$ \mathbb P(A \cup B) = \mathbb P(A) + \mathbb P(B) - \mathbb P(A \cap B) $$
Ainsi donc, on observe que $\mathbb P(A \cup B) \leq \mathbb P(A) + \mathbb P(B)$ 
<!--ID: 1707588800764-->

### Formule d'inclusion exclusion
Soit $(\Omega, \mathcal{F}, \mathbb{P})$ un [[Espaces probabilisés]]
















