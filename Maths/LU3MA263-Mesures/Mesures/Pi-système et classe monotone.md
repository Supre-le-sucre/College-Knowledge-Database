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
- Si $\exists E_n \in \mathcal P^\mathbb N$, $E_n \subseteq E_{n+1}$ et que $\bigcup E_n = E$ avec $\forall n \in \mathbb N$, $\mu_1(E_n) = \mu_2(E_n)$ alors $\mu_1 \equiv \mu_2$ (admis)

### Preuve
Soit $\mu_1$ et $\mu_2$ finies
On pose $\mathcal L = \set{A \in \mathcal E, \mu_1(A) = \mu_2(A)}$

Si $\mathcal L = \mathcal E$, alors on aura terminé, car $\mu_1$ et $\mu_2$ seront équivalente.

On sait déjà que $\mathcal L \subseteq E$ par hypothèse.
Par hypothèse également, on sait que $\mathcal P \subseteq \mathcal L$... 

Donc si on montre que $\mathcal L$ est une classe monotone, alors on aura $\sigma(\mathcal P) \subseteq \mathcal L$ et donc que $E \subseteq \mathcal L$ et par double inclusion, on aura montré ce que l'on cherche.

Pour montrer que $\mathcal L$ est une [[Pi-système et classe monotone|classe monotone]], reprenons les axiomes de sa définition.

i) $E \in \mathcal P$ car c'est un $\pi$-système... Et comme $\mathcal P \subseteq \mathcal L$, on a bien que $E \in \mathcal L$

ii)
Soit $B, C \in \mathcal L$ tel que $B \subseteq C$. Montrons qu'il y a stabilité par différence propre...
On veut donc que $C \setminus B \in \mathcal L$

Observons que $\mu_1(C) = \mu_1(B) + \mu_1(C \setminus B)$ par $\sigma$-additivité de la [[Mesure]] (les ensembles sont disjoints). Comme $\mu_1$ est supposée finie on a donc que $\mu_1(C \setminus B) = \mu_1(C) - \mu_1(B)$
Le résultat est le même pour $\mu_2$...

Donc on a bien $\mu_1(C \setminus B) = \mu_2(C \setminus B)$ et donc $C \setminus B \in \mathcal L$

iii)
On veut maintenant montrer la stabilité par union dénombrable croissante

Considérons donc une suite d'ensemble $B_n \in \mathcal L^\mathbb N$ telle que $B_n \subseteq B_{n+1}$
On pose $B = \bigcup B_n$, montrons que $B \in \mathcal L$

Par [[Propriétés fondamentales de la mesure#Croissance et décroissance séquentielle|croissance séquentielle de la mesure]] $\mu_1(B_n) \to \mu_1(B)$, et la même chose s'applique sur $\mu_2$
Or comme $\mu_1(B_n) = \mu_2(B_n)$, elles convergent vers la même limite. Donc $B \in \mathcal L$

$\mathcal L$ est donc une classe monotone.
Donc $\sigma(\mathcal P) \subseteq \mathcal L$, et d'où $E \subseteq \mathcal L$

Finalement $E = \mathcal L$, donc $\mu_1 \equiv \mu_2$
$$\tag*{$\blacksquare$}$$