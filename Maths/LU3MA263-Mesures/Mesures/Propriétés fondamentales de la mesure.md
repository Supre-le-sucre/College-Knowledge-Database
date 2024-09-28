## Propriété de bases
De par la définition d'une mesure $\mu$, il est possible de déduire trivialement 2 propriétés de bases: #!

- $\forall (A,B) \in \mathcal E^2$ tel que $A \cap B = \emptyset$ alors on a $\mu (A \cup B) = \mu(A) + \mu(B)$
- $\forall (A,B) \in \mathcal E^2$ tel que $A \subseteq B$ alors on a que $\mu(A) \leq \mu(B)$

### Preuve
Le premier point est issue de la sigma additivité de $\mu$

Pour le second point on pose $A \subseteq B$ et $A$ et $B \cap A^c$. Deux ensembles d'union disjointe.
D'après le premier point on a donc...
$$\mu(A \cup (B \cap A^c)) = \mu(B) = \mu(A) + \mu(B \cap A^c)$$
Or $\mu(B \cap A^c) \geq 0$ donc $$\mu(B) \geq \mu(A)$$
$$\tag*{$\blacksquare$}$$
## Croissance et décroissance séquentielle
On énonce la propriété suivante: #!

