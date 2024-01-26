#algo

L'algorithmie est utilisé pour prouver mathématiquement le bon fonctionnement d'un programme.
Ainsi donc les différents types de raisonnement de base sont en rigueur.

Un raisonnement important est aussi le [[Raisonnement par réccurrence]] distinguable en plusieurs types

## Raisonnement calculatoire
*Exemple*: Montrer que $(a+b)^2 + (a-b)^2 = 2(a+b)^2-4ab$
$$ (a+b)^2 + (a-b)^2 $$
$$= a^2 + 2ab + b^2 + a^2 - 2ab + b^2$$
$$ = 2a^2 + 2b^2 = 2(a^2 + b^2)$$
$$= 2(a+b)^2 -4ab$$
## Implication

L'implication est simplifiable logiquement: $a \Rightarrow b \equiv \neg a \vee b$
### Raisonnement équivalent
$$ a \Rightarrow b \equiv \neg a \vee b \equiv \neg (\neg b) \vee \neg a \equiv \neg b \Rightarrow \neg a $$
### Négation d'une implication
$$ \neg (a \Rightarrow b) \equiv \neg(\neg a \vee b) \equiv a \wedge \neg b$$

### Exemple
On souhaite montrer $P$: $\forall n \in \mathbb{N}, n > 2, n$ impair

#### Raisonnement direct
On montre immédiatement $P$, donc $\forall n \in \mathbb{N}, n > 2, n$ impair
Soit $n > 2$ premier.
On a donc que $n$ a exactement 2 diviseurs, 1 et lui-même, donc 2 n'est pas un diviseur de $n$, donc $n$ est impair

#### Raisonnement par l'absurde
Supposons qu'on est $\neg P$ et montrons que cela est absurde.

Autrement dit, supposons $\exists n \in \mathbb{N} n > 2, n$ premier et pair

Ce $n$ est divisible par 1 et par $n$, puisqu'il est pair, il est aussi divisible par 2, il aurait donc 3 diviseurs différents, ceci est absurde, car $n$ est premier.

#### Raisonnement par contraposée
Il faut alors montrer que $\forall n \in \mathbb{N}, n$ pair $\Rightarrow$ $n$ non premier ou $n \leq 2$

Soit $n \in \mathbb{N}$ pair, il existe alors 2 cas de figure:
- 1er cas, $n=2$, on a donc que $n \leq 2$
- 2e cas, $n \geq 2$, $n$ a au moins 3 diviseurs différents, 1, 2, et $n$, donc $n$ n'est pas premier.

#### Raisonnement par l'absurde II
Prouvons qu'il existe une infinité de nombre premiers.
Cette preuve ne peut pas être résolue par contraposée.

Supposons qu'il y ait un nombre fini $N$ de nombre premiers.
On les note $(p_1, \cdots, p_N)$
On pose $P = \prod_{i=1}^N p_i$ +1
$P$ n'est divisible par aucun $p_i$, donc $P$ est premier, ceci est absurde, car il y aura alors $N+1$ premiers.
