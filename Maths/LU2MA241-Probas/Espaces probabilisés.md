#probas
## Définition
- Soit $\Omega$ un espace d'état qui constitue notre univers
- Soit $\mathcal{F}$ une [[Tribu]] de $\Omega$ l'ensemble des événement.
- Soit une probabilité $\mathbb{P}$, une application de la forme $\mathbb{P} : \mathcal{F} \to [0,1]$ respectant l'[[#Axiome de probabilité]]

Alors on qualifie le triplet $(\Omega, \mathcal{F}, \mathbb{P})$ d'espace probabilisé
## Axiome de probabilité
Q: Quelle est l'axiome de probabilité ?
A: Soit $\Omega$ un espace d'état et $\mathcal{F}$ une [[Tribu]] de $\Omega$.
On qualifie $\mathbb{P} : \mathcal{F} \to [0,1]$ une probabilité si elle vérifie l'ensemble des propriétés suivantes:
1. $\mathbb{P}(\Omega) = 1$
2. ($\sigma$-additivité) Pour toute suite $(A_n)_{n\geq 1}$ d'événements disjoints (i.e $\forall (i,j), i \not = j, A_i \cap A_j = \emptyset$) on a $$\mathbb{P}\left(\bigcup_{n=1}^{+\infty}A_n\right) = \sum_{n=1}^{+\infty}\mathbb{P}(A_n)$$
**Remarque:** la $\sigma$-additivité entraîne l'additivité finie entre événement disjoints.

## Propriétés fondamentales opératoires
On considère ici, l'espace probabilisé $(\Omega, \mathcal{F}, \mathbb{P})$

### Privation entre ensemble inclus

