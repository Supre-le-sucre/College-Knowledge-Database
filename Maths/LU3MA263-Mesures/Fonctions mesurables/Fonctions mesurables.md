## Définition
Pour $(E, \mathcal E)$ et $(E', \mathcal E')$ deux espaces mesurables et $f: E \to E'$. On qualifie $f$ de $(\mathcal E, \mathcal E')$-mesurable si et seulement si: #!

$$\forall B \in \mathcal E', f^{-1}(B) \in \mathcal E$$
<!--ID: 1729505135351-->



## Propriété de la composition
Une fonction mesurable peut être obtenue comme suit: #!

En considérant $(E, \mathcal E)$, $(E', \mathcal E')$, $(E'', \mathcal E'')$ trois espaces mesurables et 2 fonctions $f$ et $g$ telles que:
- $f$ est $(\mathcal E, \mathcal E')$-mesurable
- $g$ est $(\mathcal E', \mathcal E'')$-mesurable
Alors dans ce cas $f\circ g$ est $(\mathcal E, \mathcal E'')$-mesurable
<!--ID: 1729505135353-->



### Preuve
Soit $B'' \in \mathcal E''$. On veut montrer que $(g \circ f)^{-1}(B'') \in \mathcal E$

Soit $x \in (g \circ f)^{-1}(B'')$
Donc $g \circ f(x) \in B''$ soit $g(f(x)) \in B''$

Donc dans ce cas $f(x) \in g^{-1}(B'')$ et $x \in f^{-1}(g^{-1}(B''))$ 
Or $g$ est mesurable donc $B' = g^{-1}(B'') \in \mathcal E'$
Et $f$ est mesurable donc $B = f^{-1}(B') \in \mathcal E$
$$\tag*{$\blacksquare$}$$

## Propriété [[Tribu]] engendrée et mesurabilité
On peut déterminer la mesurabilité d'une fonction comme suit: #!

Soit $(E, \mathcal E)$ et $(E', \mathcal E')$, 2 espaces mesurables et $\mathcal R' \subseteq \mathcal E'$ tel que $\sigma(\mathcal R') = \mathcal E'$
Alors $f: E \to E'$ est $(\mathcal E, \mathcal E')$-mesurable si et seulement si $$\forall B \in \mathcal R', f^{-1}(B) \in \mathcal E$$
<!--ID: 1729505135355-->



### Preuve
$\Rightarrow$: Trivial, cela découle de la définition
$\Leftarrow$: Soit $f: E \to E'$ tel que $\forall B \in \mathcal R', f^{-1}(B) \in \mathcal E$

On pose alors $\mathcal G = \set{B \in \mathcal E', f^{-1}(B) \in \mathcal E}$
Si on montre que $\mathcal G = \mathcal E'$ alors on aura démontrer la mesurabilité de $f$

L'inclusion $\mathcal G \subseteq \mathcal E'$ est donnée par définition
Par hypothèse on sait que $\mathcal R' \subseteq \mathcal G$. Si on montre que $\mathcal G$ est une tribu, alors on saura que $\sigma(\mathcal R') \subseteq \mathcal G$ et donc que $\mathcal E' \subseteq \mathcal G$.

Montrons donc que $\mathcal G$ est un tribu...

i) On a que $f^{-1}(E') = E \in \mathcal E$, donc $E' \in \mathcal G$

ii) Stabilité par complémentaire
Soit $B' \in \mathcal G$ et $f^{-1}(E' \setminus B') = E \setminus f^{-1}(B)$ par [[Pré-image#Propriétés de base|propriété de la pré-image]] 
Or $f^{-1}(B') \in \mathcal E$ car $B' \in \mathcal G$
Et comme $\mathcal E$ est stable par complémentaire on a bien que $E \setminus f^{-1}(B) \in \mathcal E$ donc que $f^{-1}(E' \setminus B') \in \mathcal E$ et donc $E' \setminus B' \in \mathcal G$

iii) Stabilité par union dénombrable
Soit $B_n \in \mathcal G^\mathbb N$, on veut que $\bigcup B_n \in \mathcal G$
Or par [[Pré-image#Propriétés de base|propriété de la pré-image]] $f^{-1}(\bigcup B_n) = \bigcup f^{-1}(B_n)$
Et comme $\mathcal E$ est stable par union dénombrable on a que $\bigcup f^{-1}(B_n) \in \mathcal E$
Donc $f^{-1}(\bigcup B_n) \in \mathcal E$ soit finalement $\bigcup B_n \in \mathcal G$
$$\tag*{$\blacksquare$}$$

## Continuité sur des topologie
On peut déduire la mesurabilité de $f$ par cette propriété: #!

Soit $(E, \tau)$ et $(E', \tau')$ deux espaces topologiques. Soit $f: E \to E'$ [[Pré-image#Continuité topologique de $f$|continue par rapport à ces topologies]]. Alors $f$ est $(\mathcal B(E), \mathcal B(E'))$-mesurable
<!--ID: 1729505135356-->



### Preuve
On utilise ici la définition d'une [[Boréliens#Tribu borélienne sur $ mathbb R$|tribu borélienne]].
En effet si $f$ continue, alors $\forall O \in \tau'$, $f^{-1}(O) \in \tau$ et comme $\sigma(\tau) = \mathcal B(E)$ on a que $f^{-1}(O) \in \mathcal B(E)$.

Ainsi d'après la propriété précédente le résultat est valide
$$\tag*{$\blacksquare$}$$


## Stabilité des fonctions mesurables sur la deuxième dimension
Soit $(E, \mathcal E)$ un espace mesurable avec $f,g:E \to \mathbb R$. On pose $h(x) = (f(x), g(x))$: #!

$h$ est $(\mathcal E, \mathcal B(\mathbb{R}^2))$-mesurable si et seulement si $f$ et $g$ sont $(\mathcal E, \mathcal B(\mathbb{R}^2))$

### Preuve
$\Rightarrow$: Cette preuve est assez basique, il suffit de poser la projet $proj_{1}: \mathbb R^2 \to \mathbb{R}$ tel que $proj_{1}: (x,y) \mapsto x$.
Cette fonction est continue, donc en particulier elle est donc $(\mathcal B(\mathbb{R}^2), \mathcal B(\mathbb{R}))$-mesurable.
Or $f = proj_{1} \circ h$ donc la propriété de la composition nous donne bien que si $h$ mesurable, $f$ le sera aussi

On refait la même chose avec $proj_{2}$ pour montrer la mesurabilité de $g$

$$