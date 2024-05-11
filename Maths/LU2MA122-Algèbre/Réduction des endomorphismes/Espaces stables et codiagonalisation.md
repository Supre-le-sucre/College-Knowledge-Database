## Définition
Soit un $\mathbb K$-espace vectoriel $E$, on considère $F \subset E$ un sous espaces vectoriel et $u \in \mathcal L(E)$.
On dit que $F$ est stable si #!

On a que $u(F) \subset F$. Dans ce cas on peut d'ailleurs induire l'endomorphisme: $u_{|F}\in \mathcal L(F)$ que l'on appelle sobrement endomorphisme induit.

## Lemme: Conséquence de la stabilité sur la diagonalisation
On observe le lemme suivant: #!

Soit $E$ un $\mathbb K$-espace vectoriel de dimension finie et $u \in \mathcal L(E)$ diagonalisable. On considère $F \subset E$ un sous-espace stable. On a alors que l'endomorphisme induit $u_{|F}$ est diagonalisable.
Si de plus on a que $E = F\oplus G$ avec $F, G$ stables par $u$, alors $u$ est diagonalisable si et seulement si les endomorphismes induit de $F$ et $G$ le sont

### Preuve
D'après [[Diagonalisation#Théorème|ce théorème]] il existe un polynôme annulateur scindé en racine simple tel que $P(u) = 0_E$.
En particulier comme $F$ est stable par $u$, on a aussi que $P(u_{|F}) = 0_F$ et donc on a bien $u_{|F}$ diagonalisable d'après [[Diagonalisation#Théorème|ce même théorème]]

Pour la deuxième assertion, on a déjà montré le sens direct, pour la réciproque, on considère les bases $B_F$ et $B_G$ de diagonalisation des endomorphisme induits. Comme la réunion donne $E$, on a bien ce que l'on cherche
$$\tag*{$\blacksquare$}$$

## Lemme stabilité des sous espaces propres
On observe le lemme suivant: #!

Soient $u, v \in \mathcal L(E)$ tels que $u \circ v = v \circ u$ alors les sous espaces propres de $u$ sont stables par $v$

### Preuve
Soit $\lambda \in \mathbb K$ et $x \in E_{\lambda}$
On a que:
$$u(v(x)) = v(u(x)) = v(\lambda x) = \lambda v(x)$$
donc $v(x) \in E_\lambda$

## Théorème de codiagonalisation
On énonce le théorème suivant: #!

Soit $E$ un $\mathbb K$-espace vectoriel de dimension finie. Soit $\mathcal A$ une partie de $\mathcal L(E)$ constituée d'éléments diagonalisables qui commutent deux à deux. Alors ils sont codiagonalisble (i.e diagonalisable dans la même base)

### Preuve
On procède par récurrence fore sur $n = dim(E)$
Si $n=0$ ou 1, c'est clair

Si $n \geq 1$ on va considérer 2 cas

Si $\mathcal A = \mathbb K Id_E$ c'est évident, car l'identité est commutative avec elle même et la valeur propre va juste être multiplié par un coefficient multiplicateur n'impactant pas la base de diagonalisation

Autrement si $\mathcal A \not \subset \mathbb K Id_E$, on prend $f \in A$ avec $f \not = \mathbb K Id_E$. On pose $\lambda$ une valeur propre de $f$.
Comme $f$ n'est pas une homothétie, on a que $dim(E_\lambda) <n$
On propose alors de poser $G = \bigoplus_{\mu \in Sp(f), \mu \not = \lambda} G_\mu$
