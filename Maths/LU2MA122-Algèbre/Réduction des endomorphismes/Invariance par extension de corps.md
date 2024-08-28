
## Invariance du rang sur l'extension de corps
On énonce le lemme suivant: #!

Soient $X_1, \dots, X_s$ des vecteurs de $\mathbb K^n$ alors on a que $rg_\mathbb K[X_1, \dots, X_s] = rg_\mathbb L[X_1, \dots, X_s]$
<!--ID: 1715537862418-->


### Preuve
En effet, si on note $M \in M_{n,s}(\mathbb K)$, la matrice de colonnes $X_1, \dots, X_s$, si $r = rg_\mathbb K[X_1, \dots, X_s]$ alors par le théorème du rang, il existe $P, Q \in GL_n(\mathbb K)$ telles que $M = PJ_rQ$ avec $J_r = diag[1, \dots, 1, 0, \dots, 0]$ avec $r$ fois 1.

Comme $GL_n(\mathbb K) \subset GL_n(\mathbb L)$, on a alors que $rg_\mathbb L[X_1, \dots, X_s] = r$

## Théorème sur les générateurs unitaire par extension de corps
On énonce le théorème suivant: #!

Soit $M \in M_n(\mathbb K)$, alors on a que $\mu_M^\mathbb K = \mu_M^\mathbb L$
<!--ID: 1715537862422-->


### Preuve
On a déjà l'inclusion des idéaux annulateurs $I_M^\mathbb K \subset I_M^\mathbb L = \{P \in \mathbb L[X], P(M) = 0\}$ ce qui donne que $\mu_M^\mathbb K$ divise $\mu_M^\mathbb L$.
Maintenant on a d'après [[Idéaux de polynôme#Relation entre le degré de générateur unitaire et le rang|ce lemme]] que $\deg(\mu_M^\mathbb L) = rg_\mathbb L(A^k)_{k \in \mathbb N}$ qui d'après le lemme précédent est égale à $rg_\mathbb K(A^k)_{k \in \mathbb N} =\deg(\mu_M^\mathbb K)$
Ainsi $\mu_M^\mathbb K$ et $\mu_M^\mathbb L$ sont de même degré et unitaire, car on a $\mu_M^\mathbb L$ qui divise $\mu_M^\mathbb K$.
On trouve bien $\mu_M^\mathbb K = \mu_M^\mathbb L$
$$\tag*{$\blacksquare$}$$