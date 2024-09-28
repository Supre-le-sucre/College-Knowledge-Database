## Définition d'un $\pi$-système
On dit que $\mathcal P \in \mathcal P(E)$ est un $\pi$-système si: #!

i) $E \in \mathcal P$
ii) $\mathcal P$ est stable par intersection ==finie==

## Définition d'une classe monotone
On dit que $\mathcal L \in \mathcal P(E)$ est une classe monotone si: #!

i) $E \in \mathcal L$
ii) $\mathcal L$ est stable par différence propre (i.e $B \subseteq C$, alors $C \setminus B \in \mathcal L$)
iii) $\mathcal L$ est stable par union dénombrable croissante
**Remarque**: Une tribu est un $\pi$-système et une classe monotone

## Théorème: tribu induite d'un $\pi$-système (admis)
Observons que: #!

Si $\mathcal L$ est une classe monotone sur $E$ et que $\mathcal P$ est un $\pi$-système tel que $\mathcal P \subseteq \mathcal L$, alors
$$\sigma(\mathcal P) \subseteq \mathcal L$$

## Théorème: Conséquence de mesure sur un $\pi$-système
On considère le théorème suivant: #!

Soit $(E, \mathcal E)$ un espace mesurable et soir $\mu_1, \mu_2$, 2 mesures sur $(E, \mathcal E)$
On considère un $\pi$-système $\mathcal P$ sur $E$ tel que $\forall A \in \mathcal P$
- $\mu_1(A) = \mu_2(A)$
- $\sigma(\mathcal P) = \mathcal E$
Alors:
- Si $\mu_1$, $\mu_2$ sont finies alors $\mu_1 \equiv \mu_2$
- Si $\exists E_n \in \mathcal P^\mathbb N$, $E_n \subseteq E_{n+1}$ et que $\bigcup E_n = E$ avec $\forall n \in \mathbb N$, $\mu_1(E_n) = \mu_2(E_n)$ alors $\mu_1 \equiv \mu_2$

### Preuve
Soit $\mu_1$ et $\mu_2$ finies
On pose $\mathcal L = \set{A \in \mathcal E, \mu_1(A) = \mu_2(A)}$

Si $\mathcal L = \mathcal E$, alors on aura terminé, car $\mu_1$ et $\mu_2$ seront équivalente.

Par hypothèse, on sait que $\mathcal P \subseteq \mathcal L$