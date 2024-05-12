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