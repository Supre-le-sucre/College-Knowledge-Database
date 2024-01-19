#algo

L'algorithmie est utilisé pour prouver mathématiquement le bon fonctionnement d'un programme.
Ainsi donc les différents types de raisonnement de base sont en rigueur.

## Raisonnement calculatoire
*Exemple*: Montrer que $(a+b)^2 + (a-b)^2 = 2(a+b)^2-4ab$
$$ (a+b)^2 + (a-b)^2 $$
$$= a^2 + 2ab + b^2 + a^2 - 2ab + b^2$$
$$ = 2a^2 + 2b^2 = 2(a^2 + b^2) = 2(a+b)^2 -4ab$$
## Implication
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

Soit $n \in \mathbb{N}$ 