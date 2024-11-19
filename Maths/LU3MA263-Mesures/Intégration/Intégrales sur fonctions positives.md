## Définition
Soit $(E, \mathcal E, \mu)$ un espace mesuré, et $f: E \to [0, \infty]$ une fonction positive et $\mathcal E$-mesurable. Pour $A \in \mathcal E$, on définit l'intégrale de $f$ conte $\mu$ sur $A$ par: #!

$$
\int_{A} fd\mu = \sup\left\{ \int_{A}sd\mu, s \in S_{+}, \forall x \in A, 0 \leq s(x) \leq f(x) \right\} 
$$

## Propriété
On note les propriétés fondamentales de l'intégrale sur fonctions positives: #!

Soit $f, g: E \to [0, \infty]$, $\mathcal E$-mesurable. Alors

i) <u>Conservation de l'ordre</u> $f \leq g$ sur $A \in \mathcal E$
$$
\int_{A}fd\mu \leq \int_{A}gd\mu
$$

ii) <u>Cohérence de la fonction nulle</u> si $f=0$ sur $A \in \mathcal E$ $$
\int_{A} fd\mu = 0
$$
iii) <u>Cohérence de l'espace négligeable</u> $\mu(A)= 0$
$$
\int_{A}fd\mu = 0
$$

iv) <u>Cohérence par produit de l'indicatrice</u> $\forall A \in \mathcal E$
$$
\int_{A} f d\mu = \int_{E}f\mathbb 1_{A}d\mu
$$
v) <u>Linéarité de l'intégrale</u>, $\forall c \geq 0$
$$
\int_{A}cfd\mu = c\int_{A}fd\mu
$$

### Preuve
Les preuves de ces propriétés découlent de la définition ainsi que des [[Théorie de l'intégrale sur fonction étagée#Propriété de bases de l'intégrales|propriété de bases de l'intégrale sur fonctions étagées]]
