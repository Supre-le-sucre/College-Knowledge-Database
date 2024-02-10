#probas
## Propriété
Soit $(\Omega, \mathcal{F}, \mathbb{P})$ un [[Espaces probabilisés]], on a la continuité par le bas / par le haut si... #!
- <u>Continuité par le bas:</u> Si $(A_n)_{n \geq 1}$ est une suite croissante par inclusion d'événements $\forall n \in \mathbb{N}$ alors: $$\mathbb{P}\left(\bigcup_{n=1}^\infty A_n\right) = \lim_{n\to + \infty} \mathbb{P}(A_n)$$
- <u>Continuité par le haut</u> Si $(A_n)_{n \geq 1}$ est une suite décroissante par inclusion d'événements $\forall n \in \mathbb{N}$ alors: $$\mathbb{P}\left(\bigcap_{n=1}^\infty A_n\right) = \lim_{n\to + \infty} \mathbb{P}(A_n)$$
<!--ID: 1707589760449-->

## Preuve
On se proposera ici d'étudier des événement disjoints.
Montrer la continuité par le bas permet aussi de montrer celle par le haut par complémentarité.

On pose $C_0 = A_0, C_1 = A_1 \setminus A_0, \cdots C_n = A_n \setminus A_{n-1}$
Les événement $C_i$ sont tous deux à deux disjoints. 
Avec de plus $\bigcup^n_{i=0} C_i = A_n$ et $\bigcup_{n \in \mathbb N} C_n = \bigcup_{n \in \mathbb{N}} A_n$ puisque $A_n \subseteq A_{n+1}$ 

Par [[Espaces probabilisés#Axiome de probabilité|sigma-additivité]] on a que $$ \mathbb P\left(\bigcup_{n \in \mathbb N} C_n\right) = \sum_{n \in \mathbb N} \mathbb P(C_n)$$ Or on sait que:
$$\sum_{n \in \mathbb N} \mathbb P(C_n) = \lim_{n \to + \infty}\mathbb \sum ^n _{i=0}P(C_i)$$
Et par [[Espaces probabilisés#Axiome de probabilité|sigma-additivité]] on a que:
$$\sum ^n _{i=1}P(C_i) = \mathbb P \left(\bigcup^n_{i=0}C_i\right) = \mathbb P(A_n)$$ D'où finalement:
$$ \mathbb P\left(\bigcup_{n \in \mathbb N} C_n\right) = \mathbb P\left(\bigcup_{n \in \mathbb N} A_n\right)= \lim_{n \to + \infty}\mathbb P(A_n)$$

## Corollaire

Par continuité par le bas et par le haut, on peut en déduire que pour toutes suites d'événement non nécessairement croissante ou décroissante on a que #!
$$ \mathbb P \left(\bigcup^\infty_{n=1}A_n\right) = \lim_{n \to \infty} \mathbb P \left(\bigcup^n_{k=1}A_k\right)$$
et aussi
$$ \mathbb P \left(\bigcap^\infty_{n=1}A_n\right) = \lim_{n \to \infty} \mathbb P \left(\bigcap^n_{k=1}A_k\right)$$
<!--ID: 1707591980020-->

