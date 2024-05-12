## Théorème
Pour $E$ un $\mathbb K$-espace vectoriel de dimension finie, soit $u \in \mathcal L(E)$, les assertions suivantes sur la trigonalisation de $u$ sont équivalentes: #!

- $(i)$ $u$ est trigonalisable
- $(ii)$ $\mathcal X_u$ est scindé
- $(iii)$ Il existe un [[Polynômes d'endomorphismes]] $P \in \mathbb K[X]$ scindé tel que $P(u) = 0$

### Preuve
On montre d'abord que $(i) \implies (ii)$

Si $u$ est trigonalisables avec de valeurs propres $\lambda_i$ alors pour calculer son polynôme caractéristique il suffit de le faire dans la base de trigonalisation:
$$\mathcal X_u = \prod_{i=1}^n(X-\lambda_i)$$ avec donc $\mathcal X_u$ scindé

Montrons $(ii) \implies (iii)$
On applique [[Polynôme caractéristique#Théorème de Cayley-Hamilton|Cayley-Hamilton]], $X_u(u) = 0$ 

Enfin montrons que $(iii) \implies (i)$
On pose $P$ scindé tel que $P(u) = 0$
On considère le lemme intermédiaire suivant:

#### Lemme
Il existe un hyperplan $H$ de $E$ stable par $u$

##### Preuve
On a que $P(u) = P(^tu) = 0$. Or comme $P$ est scindé, on l'écrit de la forme suivante
$P = \prod_{i=1}^n(X-\lambda_i)$ d'où alors que
$$(^tu-\lambda_1Id_E) \circ \cdots \circ (^tu-\lambda_nId_E) = 0$$

Donc il existe $i_0$ tel que $(^tu-\lambda_{i_0}Id_E)$ ne soit pas injective (car l'une d'entre vaudra 0 pour un certain $x$ non nul).
On a donc que $\lambda_{i_0}$ est une valeur propre de $^tu$. Soit $f \in E^\vee$, un vecteur propre de $^tu$ associée à $\lambda_{i_0}$. On prends alors $H = (f)^\circ$, c'est bien un hyperplan (cf. [[Orthogonale d'un espace vectoriel]]). Montrons qu'il est stable par $x$.

On a par définition que
$$H = \{x \in E, f(x) = 0\}$$
Soit alors:
$$\langle u(x), f \rangle = \langle x, \;^tu(f) \rangle = \langle x, \lambda_{i_0}f\rangle = 0$$
et $u(x) \in H$ donc ok
$$\tag*{$\blacksquare$}$$

On retourne maintenant à la preuve de départ,
On procède par récurrence avec $n = \dim(E)$
Si $n=0, 1$ c'est clair
Etudions maintenant, le cas de récurrence

Soit $H$ un hyperplan stable de $f$, alors $P(f_{|H}) = 0$ et donc $f_{|H}$ est trigonalisable par hypothèse de récurrence. Soit $(\epsilon_2, \dots, \epsilon_n)$ sa base de trigonalisation
On considère $\epsilon_1$ tel que:
$$E=\mathbb K\epsilon_1 \oplus H$$
Alors dans la base $(\epsilon_1, \dots, \epsilon_n)$ la matrice est triangulaire inférieure donc $f$ trigonalisable

### Corollaire
Des équivalence de la trigonalisation, on en déduit le corollaire sur les réductions: #!

Soit $u \in \mathcal L(E)$ trigonalisable, et $F \subset E$ un sous-espace vectoriel, alors on a que $u_{|F}$ est trigonalisable. Si de plus $E = F \bigoplus G$, avec $F, G$ stables par $u$ alors $u$ est trigonalisable si et seulement si $u_{|F}$ et $u_{|G}$ le sont

#### Preuve
Si $u$ est trigonalisable, alors il annule le polynôme scindé $P$ et comme $F$ est stable, on a donc que $P(u_{|F}) = 0_F$ donc il est diagonalisable

Pour la deuxième insertion, le sens direct vient d'être vu, la réciproque se fait en prenant l'union des deux bases de trigonalisation (l'union forme $E$)