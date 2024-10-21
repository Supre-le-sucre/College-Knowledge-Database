## Propriété de bases
De par la définition d'une mesure $\mu$, il est possible de déduire trivialement 2 propriétés de bases: #!

- $\forall (A,B) \in \mathcal E^2$ tel que $A \cap B = \emptyset$ alors on a $\mu (A \cup B) = \mu(A) + \mu(B)$
- $\forall (A,B) \in \mathcal E^2$ tel que $A \subseteq B$ alors on a que $\mu(A) \leq \mu(B)$
<!--ID: 1729505204723-->



### Preuve
Le premier point est issue de la sigma additivité de $\mu$

Pour le second point on pose $A \subseteq B$ et $A$ et $B \cap A^c$. Deux ensembles d'union disjointe.
D'après le premier point on a donc...
$$\mu(A \cup (B \cap A^c)) = \mu(B) = \mu(A) + \mu(B \cap A^c)$$
Or $\mu(B \cap A^c) \geq 0$ donc $$\mu(B) \geq \mu(A)$$
$$\tag*{$\blacksquare$}$$

## Croissance et décroissance séquentielle
On énonce la propriété suivante: #!

Soit $(A_n)_{n \in \mathbb N} \in \mathcal E$
- Si $\forall n \in \mathbb N A_n \subseteq A_{n+1}$ avec $A = \bigcup_{n\in \mathbb N} A_n$ alors $$\lim_{n \to \infty} \mu(A_n) = \mu(A)$$
- Si $\forall n \in \mathbb N A_{n+1} \subseteq A_{n}$ avec $A = \bigcap_{n\in \mathbb N} A_n$ ==ET QUE== $\mu(A_0) < + \infty$ alors $$\lim_{n \to \infty} \mu(A_n) = \mu(A)$$
- ($\sigma$-sous-additivité) $$\mu\left(\bigcup_{n\in \mathbb N} A_n\right) \leq \sum_{n \in \mathbb N} \mu(A_n)$$
<!--ID: 1729505204724-->




### Preuves
i) Soit $(A_n)_{n\in \mathbb N} \in \mathcal E$, avec $A_n \subseteq A_{n+1}$
Pour travailler avec des unions disjointes posons $B_0 = A_0$ et $\forall n \in \mathbb N$, $B_n = A_{n}\setminus A_{n-1}$



Observons que $B_n \in \mathcal E$ par stabilité de $\mathcal E$. Et aussi $\bigcup^n_{k=0} B_k = A_n$
En particulier on a alors que
$$\lim_{n \to +\infty}\mu(A_n) = \lim_{n \to +\infty} \mu\left(\bigcup^n_{k=0} B_k\right)$$
$$= \lim_{n \to +\infty} \sum^n_{k=0} \mu(B_k) = \sum_{n \in \mathbb N} \mu(B_n) = \mu\left(\bigcup_{n \in \mathbb N} B_n\right)$$
Or observons que $\bigcup_{n \in \mathbb N} B_n = \bigcup_{n \in \mathbb N} A_n$
Donc finalement
$$\lim_{n \to +\infty}\mu(A_n) = \mu\left(\bigcup_{n \in \mathbb N} A_n\right) = \mu(A)$$

ii) Soit $(A_n)_{n\in \mathbb N} \in \mathcal E$, avec $A_{n+1} \subseteq A_{n}$ ==ET== $\mu(A_0) < \infty$
On pose cette fois une suite d'ensemble croissante $A'_n = A_0 \setminus A_n$
D'après la première propriété on a alors que
$$\mu\left(\bigcup_{n \in \mathbb N} A'_n\right) = \lim_{n \to +\infty} \mu(A'_n)$$

De plus observons que par construction, et en appliquant l'union disjointe on a que
$$\mu(A'_n) + \mu(A_n) = \mu(A_0)$$
Alors comme $\mu(A_0) < \infty$ on peut poser que
$$\mu(A'_n) = \mu(A_n) - \mu(A_0)$$

De plus observons que $\bigcup_{n \in \mathbb N} A'_n = A_0 \setminus (\bigcap_{n \in \mathbb N} A_n)$
Donc
$$\lim_{n \to +\infty} \mu(A'_n) = \mu\left(A_0 \setminus \left(\bigcap_{n \in \mathbb N} A_n\right)\right) = \mu(A_0\setminus A)$$
Ainsi donc
$$\mu(A_0) - \mu(A) = \lim_{n \to +\infty} \mu(A'_n) = \lim_{n \to +\infty} \mu(A_n) - \mu(A_0)$$
$$\mu(A) = \lim_{n \to +\infty} \mu(A_n)$$


