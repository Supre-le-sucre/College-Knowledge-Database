## Définition
On définit un polynôme d'endomorphisme $P$ de la façon suivante:#!

Soit $u \in \mathcal L(E)$ un endomorphisme sur $E$. On définit $u^k$ comme la composée $k$ fois de $u$. Par convention on note $u^0 = Id_E$, l'endomorphisme identité.
Soit $P = \sum^n_{k=0}a_k X^k \in \mathbb K[X]$ on définit alors: $$P(u) = \sum_{k=0}^na_ku^k \in \mathcal L(E)$$ Observons que si $P = 1$, alors on a $1(u) = Id_E$. En effet, ceci découle de la convention $u^0 = Id_E$

## Lemme
Soient pour $P, Q \in \mathbb K[X]$ avec $u \in \mathcal L(E)$ (i.e un endomorphisme dans $E$) on a les propriétés suivantes sur les polynômes d'endomorphisme: #!

- $\forall \lambda \in \mathbb K, (P+\lambda Q)(u) = P(u) + \lambda Q(u)$
- $(PQ)(u) = (QP)(u) = P(u) \circ Q (u)$
<!--ID: 1715537862470-->


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


## Théorème de Bachet-Bézout
On énonce le théorème suivant: #!

Soit $P,Q \in \mathbb K[X]$. Alors on a $P \wedge Q = 1$ (i.e P et Q sont premiers entre eux) si et seulement s'il existe $U, V \in \mathbb K[X]$ tel que $$PU+QV = 1$$
### Conséquence
On remarque la conséquence suivante sur le théorème de Bachet-Bézout: #!
Deux polynômes sont premiers entre eux s'ils ont tous les deux des racines disjointes.
<!--ID: 1715537862472-->


## Lemme des noyaux
On énonce le lemme suivant: #!

Soient $P,Q \in \mathbb K[X]$ premiers entre eux (i.e en décomposition de facteurs, ces polynômes ne partagent aucun facteurs communs, maintenant écrit $P\wedge Q = 1$) et $u \in \mathcal L(E)$ alors on a que: $$\ker((PQ)(u)) = \ker(P(u)) \oplus \ker(Q(u))$$
<!--ID: 1715537862474-->


### Preuve
Considérons $x \in \ker(P(u)) \cap \ker(Q(u))$. Alors on a $P(u)(x) = Q(u)(x) = 0$
Puisque $P \wedge Q = 1$, on a d'après la relation de Bachet-Bézout, il existe $(W, R) \in \mathbb K[X]^2$ tel que$PW + QR = 1$.
En y appliquant $u$ et en évaluant $x$ on obtient:
$$PW(u)(x) + QR(u)(x) = 1(u)x = x$$
Car $1(u) = Id_E$
Or observons que...
$$PW(u)(x) + QR(u)(x) = WP(u)(x) + QR(u)(x) = W(u)(P(u)(x)) + Q(u)(R(u)(x))$$
Soit finalement:
$$PW(u)(x) + QR(u)(x) = W(u)(0) + Q(u)(0) = 0+0 = 0 = x$$
Donc on a $x = 0$ d'où $\ker(P(u)) \cap \ker(Q(u)) = \{0\}$

En outre observons que
$\ker(P(u)) \subset \ker(PQ(u))$ et $\ker(Q(u)) \subset \ker(PQ(u))$ d'où l'inclusion suivante:
$$\ker(P(u)) \oplus \ker(Q(u)) \subset \ker(PQ(u))$$

Réciproquement, considérons $x \in \ker(PQ(u))$, on a cette fois encore par Bézout:
$$x = PW(u)(x) + QR(u)(x)$$

Posons $y = PW(u)(x)$ et $z=QR(u)(x)$ et montrons que $y \in \ker(Q(u))$ et $z \in \ker(P(u))$

Observons que $Q(u)(y) = QPW(u)(x) = (W(u) \circ PQ(u))(x) = W(u)(0) = 0$ car $x \in \ker(PQ(u))$.
On a la même égalité pour $z$, ce qui conclut notre preuve
$$\tag*{$\blacksquare$}$$
### Corollaire
Le lemme des noyaux peut se généraliser: #!

Soit $P_1, \dots, P_s \in \mathbb K[X]$ deux à deux premiers entre eux. Avec $f \in \mathcal L(E)$ alors on a que $$\ker(P_1\cdots P_s(f)) = \bigoplus_{i=1}^s\ker(P_i(f))$$Si de plus, on a que $(P_1\cdots P_s)(f) = 0$ alors pour tout $i \in [1, s]$ les projections $\pi_i: \ker((P_1\dots P_s)(f)) \to P_i(f)$ sont des polynômes en $f$
<!--ID: 1715537862475-->


#### Preuve
On procède par récurrence forte
Si $s=2$ on l'a déjà montré dans le lemme précédent.

Soit $s \geq 2$, alors comme les $P_i$ sont deux à deux premiers entre eux, on a que $P_1, \dots P_{s-1}$ sont aussi premier deux à deux.
Par hypothèse de récurrence on que
$$\ker(P_1 \dots P_{s-1}(f)) = \bigoplus_{i=1}^{s-1}\ker(P_i(f))$$
Et comme le produit $P_1 \cdots P_{s-1} \in \mathbb K[X]$ est aussi un polynôme et $P_s$ premier avec $P_1, \dots, P_{s-1}$, on a que $P_s$ est premier avec le produit $P_1 \dots P_{s-1}$.
Par hypothèse de récurrence dans le cas $s=2$ on a donc:
$$\ker(P_1\cdots P_{s-1}P_s(f)) = \ker(P_1 \dots P_{s-1}(f)) \oplus\ker(P_s(f)) = \bigoplus_{i=1}^{s}\ker(P_i(f))$$

Vérifions maintenant l'assertion des projecteurs. Fixons $i \in [1, s]$ avec $R_i = \prod_{j \not = i}P_j$ alors $R_i$ et $P_i$ sont premiers entre eux.
On écrit la relation de Bézout
$$UR_i + HP_i = 1$$
Soit $\pi_i := UR_i(f)$, il s'agit d'un polynôme en $f$. Montrons qu'il s'agit bien d'un projecteur…
Soit $x \in E$, alors $$P_i(\pi_i(x)) = UP_iR_i(f)(x) = 0$$car en effet, on a par hypothèse que $P_1 \cdots P_s = 0$
On a donc que $Im(\pi_i) \subset \ker(P_i(f))$

De plus observons que $\pi_i(HP_i(f)) = 0$ pour les mêmes raisons
Or puisque l'on a l'égalité suivante: $$x = \pi_i(x)+ HP_i(f)(x)$$si on applique $\pi_i$ de nouveau on obtient que...
$$\pi_i(x) = \pi_i(\pi_i(x) + HP_i(f)(x)) = \pi_i^2(x) + \pi_i(HP_i(f)(x)) = \pi_i^2(x)$$
D'où
$$\forall x \in E, \; \pi_i(x) = \pi_i^2(x)$$

On a donc bien que $\pi_i$ est un projecteur. De plus on a exactement $Im(\pi_i) = \ker(P_i(f))$ puisque si $x \in \ker(P_i(f))$ alors...
$$x = \pi_i(x)+ HP_i(f)(x) \implies x = \pi_i(x)$$
$$\tag*{$\blacksquare$}$$
