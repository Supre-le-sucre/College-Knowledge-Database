## Définition
On définit un polynôme d'endomorphisme $P$ de la façon suivante:#!

Soit $u \in \mathcal L(E)$ un endomorphisme sur $E$. On définit $u^k$ comme la composée $k$ fois de $u$. Par convention on note $u^0 = Id_E$, l'endomorphisme identité.
Soit $P = \sum^n_{k=0}a_k X^k \in \mathbb K[X]$ on définit alors: $$P(u) = \sum_{k=0}^na_ku^k \in \mathcal L(E)$$ Observons que si $P = 1$, alors on a $1(u) = Id_E$

## Lemme
Soient pour $P, Q \in \mathbb K[X]$ avec $u \in \mathcal L(E)$ (i.e un endomorphisme dans $E$) on a les propriétés suivantes sur les polynômes d'endomorphisme: #!

- $\forall \lambda \in \mathbb K, (P+\lambda Q)(u) = P(u) + \lambda Q(u)$
- $(PQ)(u) = (QP)(u) = P(u) \circ Q (u)$

### Preuve

La première propriété est immédiate. En effet, elle découle de la linéarité de la somme:

Soit $P = \sum_{k=0}^na_kX^k$ et $Q= \sum_{l=0}^mb_lX^l$
Observons pour $u \in \mathcal L(E)$
$$(P+ \lambda Q)(u) = \sum_{k=0}^na_ku^k + \lambda\sum_{l=0}^mb_lu^l=P(u) + \lambda Q(u)$$

Pour la seconde, observons que comme $\mathbb K[X]$ est un [[Corps]], ses opérations sont commutatives. Donc $PQ = QP$ et soit $(PQ)(u) = (QP)(u)$ 

Observons que l'égalité est linéaire. C'est à dire que l'on peut considérer les termes un à un.
En effet:
$$\sum_{k=0}^na_kX^k\left(\sum^m_{l=0}b_lX^l\right) = \sum_{k=0}^n\sum_{l=0}^ma_kb_lX^{k+l}$$
En considérons le terme particulier où $k=K$ et $l=L$ on a alors le terme complet:
$$a_Kb_LX^{K+L}$$ sur lequel on passe en paramètre l'endomorphisme $u$. Il devient alors:
$$a_Kb_Lu^{K+L}$$et par définition de l'endomorphisme $u^k$, on a $u^{K+L} = u^K \circ u^L$

D'où...
$$a_Kb_Lu^{K+L} = a_Kb_L (u^K \circ u^L) = (a_Ku^K) \circ (b_Lu^L)$$

Comme ceci est valable pour tous les termes, on a, finalement que
$$(PQ)(u) = P(u) \circ Q(u)$$


## Lemme des noyaux
On énonce le lemme suivant: #!

Soient $P,Q \in \mathbb K[X]$