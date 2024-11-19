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


## Propriété de linéarité de l'intégrale sur fonction
Soit $f,g: E \to [0, \infty]$ et $\mathcal E$-mesurables avec $c \geq 0$, alors: #!
$$
\int_{E}(f+cg)d\mu=\int_{E}fd\mu+c\int_{E}gd\mu
$$

### Preuve
Soit $(s_{n})_{n \in \mathbb{N}}$ une suite de fonctions de $S_{+}$ tel que $s_{n} \leq s_{n+1}$ et $\lim_{ n \to \infty } s_{n} = f$ possible par le [[Fonctions étagées#Propriété convergence vers une fonction mesurable|lemme technique]]

On pose aussi une suite $s'_{n}$ de $S_{+}$ de même propriété qui cette fois converge vers $g$.
On sait que l'[[Théorie de l'intégrale sur fonction étagée|intégrale est linéaire]] sur les fonctions étagées i.e
$$
\int_{E}(s_{n}+cs'_{n}) d\mu = \int_{E}s_{n}d\mu+c\int_{E}s'_n
d\mu$$
Comme la suite de $s_{n}$ et de $s'_{n}$ est croissante, il est possible d'appliquer [[Convergence monotone|le théorème de convergence monotone]] 

$$
\begin{align*}
\int_{E}(s_{n}+cs'_{n}) d\mu = & \int_{E}s_{n}d\mu+ c\int_{E}s'_n \\ \\
\lim_{ n \to \infty } \int_{E}(s_{n}+cs'_n)d\mu = & \lim_{ n \to \infty } \left( \int_{E}s_{n}d\mu \right) + \lim_{ n \to \infty } \left(c \int_{E} s'_{n}d\mu \right) \\ \\
 \int_{E}\left(\lim_{ n \to \infty }(s_{n}+cs'_n)d\mu\right) = &   \int_{E}\left(\lim_{ n \to \infty }s_{n}\right)d\mu  +  c \int_{E} \left(\lim_{ n \to \infty }s'_{n}\right)d\mu  \\ \\
\int_{E}(f+cg)d\mu= &\int_{E} fd\mu +c \int_{E}gd\mu
\end{align*}
$$