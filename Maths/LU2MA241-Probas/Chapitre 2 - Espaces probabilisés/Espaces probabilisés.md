#probas
## Définition
On qualifie le triplet $(\Omega, \mathcal{F}, \mathbb{P})$ d'espace probabilisé si #!
- Soit $\Omega$ un espace d'état qui constitue notre univers
- Soit $\mathcal{F}$ une [[Tribu]] de $\Omega$ l'ensemble des événement.
- Soit une probabilité $\mathbb{P}$, une application de la forme $\mathbb{P} : \mathcal{F} \to [0,1]$ respectant l'[[#Axiome de probabilité]]
<!--ID: 1707586301874-->

### Vocabulaire
On qualifie d'événement presque sûr un événement $A$ tel que #!
$\mathbb P(A) = 1$
<!--ID: 1707592075745-->

## Axiome de probabilité
Soit $\Omega$ un espace d'état et $\mathcal{F}$ une [[Tribu]] de $\Omega$. On qualifie $\mathbb{P} : \mathcal{F} \to [0,1]$ une probabilité si elle vérifie l'ensemble des propriétés suivantes: #!
1. $\mathbb{P}(\Omega) = 1$
2. ($\sigma$-additivité) Pour toute suite $(A_n)_{n\geq 1}$ d'événements disjoints (i.e $\forall (i,j), i \not = j, A_i \cap A_j = \emptyset$) on a $$\mathbb{P}\left(\bigcup_{n=1}^{+\infty}A_n\right) = \sum_{n=1}^{+\infty}\mathbb{P}(A_n)$$
**Remarque:** la $\sigma$-additivité entraîne l'additivité finie entre événement disjoints.
<!--ID: 1707586321110-->

## Propriétés fondamentales

### Définition de $\mathbb P$ pour un ensemble $\Omega$ fini
En posant $\mathcal{F} = \mathcal{P}(\Omega)$ et en étudiant l'[[Espaces probabilisés]] $(\Omega, \mathcal{F}, \mathbb{P})$, On a que $\forall A \subseteq \Omega$ #!
$$\mathbb{P}(A) = \frac{|A|}{|\Omega|}$$
<!--ID: 1707605523404-->


### Privatisation avec inclusion
On considère l'[[Espaces probabilisés]] $(\Omega, \mathcal{F}, \mathbb{P})$ Soit $A,B \in \mathcal{F}$ avec $A \subseteq B$. Il est possible de déduire une propriété pour $\mathbb{P}(B \setminus A)$ #!
$$ \mathbb{P}(B \setminus A) = \mathbb P(B) - \mathbb P(A)$$
Plus particulièrement, on observe que: $\mathbb P(A) \leq \mathbb P(B)$ et que $\mathbb P(A^c) = 1 - \mathbb P(A)$ 
<!--ID: 1707588267113-->

#### Preuve
Soit $A \subseteq B$. On pose $C_1 = A, C_2 = B\setminus A$. On a que $C_1 \cap C_2 = \emptyset$
Par [[#Axiome de probabilité|sigma-additivité]] $\mathbb P(C_1 \cup C_2) = \mathbb P(C_1) + \mathbb P(C_2) = \mathbb P(A) + \mathbb{P}(A \setminus B)$ 

Et $\mathbb{P}(C_1 \cup C_2) = \mathbb P (B)$ d'où $\mathbb{P}(B)= \mathbb{P}(A) + \mathbb{P}(A \setminus B)$ 
$$\tag*{$\blacksquare$}$$

### Union de deux événements
On considère l'[[Espaces probabilisés]] $(\Omega, \mathcal{F}, \mathbb{P})$ Soit $A,B \in \mathcal{F}$. Il est possible de déduire une propriété pour $\mathbb{P}(A \cup B)$ #!
$$ \mathbb P(A \cup B) = \mathbb P(A) + \mathbb P(B) - \mathbb P(A \cap B) $$
Ainsi donc, on observe que $\mathbb P(A \cup B) \leq \mathbb P(A) + \mathbb P(B)$ 
<!--ID: 1707588800764-->

#### Preuve
Il est possible de réécrire: $B \setminus A = B \setminus (A \cap B)$ ne retirant que les éléments de $A$ étant dans $B$.
De plus $A \cup B = A \cup (B \setminus A)$ est une union disjointe

Par [[#Axiome de probabilité|sigma-additivité]],
$$\mathbb P(A \cup B) = \mathbb P(A) + \mathbb P(B \setminus (A \cap B)$$
Puis par [[#Privatisation avec inclusion|la propriété précédente]] 
$$\mathbb P(A \cup B) = \mathbb P(A) + \mathbb P(B) - \mathbb P (A \cap B)$$
$$\tag*{$\blacksquare$}$$

### Formule d'inclusion exclusion
Soit $(\Omega, \mathcal{F}, \mathbb{P})$ un [[Espaces probabilisés]], pour n'importe quel événement $A_1, \cdots A_n \in \mathcal{F}$ on a #!
$$ \mathbb{P}(A_1 \cup \cdots \cup A_n) = \sum_{k=1}^n(-1)^{k+1} \sum_{I \subseteq\set{1, \cdots, n}, |I| = k} \mathbb P \left(\bigcap_{i \in I}A_i\right) $$
<!--ID: 1707589371896-->

















