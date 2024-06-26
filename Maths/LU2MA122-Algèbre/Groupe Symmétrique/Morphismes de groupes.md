#algebre 
## Définition
Soit $(A, .), (B, .)$ deux [[Groupe|groupes]], on note $1_A$ et $1_B$ leurs éléments neutres respectifs.
Un morphisme de [[Groupe |groupe]] est une fonction entre [[Groupe|groupes]]: $f: A \to B$ telle que
$$f(1_A) = 1_B, f(x.y) = f(x).f(y)$$
*Exemples:* $z \mapsto |z|$ de $(\mathbb{C}^*, .) \to (\mathbb{R}^*, .)$ ou $x \mapsto e^x$ de $(\mathbb{R}, +) \to (\mathbb{R}^*, .)$ sont des morphismes de groupes.
### Remarques importantes

Observons que l'on a automatiquement, pour ces mêmes groupes: $$f(x).f(x^{-1}) = f(x.x^{-1}) = 1_B$$ 
En effet, $f(1_A) = f(x.x^{-1}) = f(x).f(x^{-1}) = 1_B$
Ainsi donc $f(x^{-1}) = f(x)^{-1}$ (En effet, rappelons nous que $f(x) \in B$)

## Vocabulaire
Soit $f: G \to H$, un morphisme de groupes. On dit que...
1. $f$ est un <u>endomorphisme</u> si $G=H$
2. $f$ est un <u>isomorphisme</u> si elle est bijective
3. $f$ est un <u>automorphisme</u> si c'est un endomorphisme bijectif

*Exemples:*
- $x \mapsto x^2$ est un endomorphisme de groupe de $(\mathbb{R}^*, \times)$
- $x \mapsto e^x$ est une bijection de $(\mathbb{R}, +)$ sur $(\mathbb{R}^*_+, \times)$. On peut donc aussi dire que ces groupes sont ==isomorphes== 

### Exemple important, automorphisme intérieur
Soit un groupe $G$ et $x \in G$, $\phi_x: G \to G$ donné par $y \mapsto xyx^{-1}$ est un automorphisme de $G$.
On appelle un tel automorphisme, un <u>automorphisme intérieur</u>.
Si $x=1_G$, alors il s'agit de l'automorphisme identité: $Id_G$ donné par $y \mapsto y$

## L'ensemble des automorphismes est un groupe

### Propriété
Soit $G$, un groupe. L'ensemble $Aut(G)$ des automorphismes de $G$, couplé avec la <u>composition</u> des applications comme [[Loi de composition interne (LCI)|LCI]] est un [[Groupe|groupe]].

#### Démonstration
On rappelle qu'un [[Groupe|groupe]] est un [[Monoïde|monoïde]] admettant un inverse pour chaque élément.

On doit montrer l'associativité et l'élément neutre pour montrer que $(Aut(G), \psi)$ est un [[Monoïde]].
La loi de composition $\psi$, comme composition des application est associative, car chacune d'elle est associative.
On remarque que $\forall \sigma \in Aut(G), Id_G\circ\sigma = \sigma \circ Id_G = \sigma$ donc $Id_G$ est l'élément neutre.

Montrons maintenant qu'il existe un inverse pour chaque élément de $Aut(G)$

Comme $\sigma$ est bijective, on note $\sigma^{-1}$ son inverse et on a $\sigma \circ \sigma^{-1} = \sigma^{-1} \circ \sigma = Id$.
Montrons que $\sigma^{-1} \in Aut(G)$. Vérifions d'abord qu'il s'agit ici d'un morphisme de groupe.

Considérons $1_G$, l'élément neutre du groupe $G$. Montrons que $\sigma^{-1}(1_G) = 1_G$
On a par définition $\sigma(1_G) = 1_G$, de la même manière alors $\sigma^{-1}(1_G) = 1_G$

Maintenant, on cherche à montrer que $\forall (x,y) \in G^2, \sigma^{-1}(x.y) = \sigma^{-1}(x).\sigma^{-1}(y)$ 
On sait que $\sigma$ est un automorphisme. De fait.
$$ \sigma(\sigma^{-1}(x).\sigma^{-1}(y)) = \sigma(\sigma^{-1}(x)).\sigma(\sigma^{-1}(y)) = x.y$$
Et on sait aussi que, par définition
$$ x.y = \sigma(\sigma^{-1}(x.y))$$
Comme $\sigma$ est un automorphisme, $\sigma$ est bijective, et donc injective.
Soit alors l'assertion suivante:
$$ \sigma(\sigma^{-1}(x).\sigma^{-1}(y)) = \sigma(\sigma^{-1}(x.y)) \Rightarrow \sigma^{-1}(x).\sigma^{-1}(y) = \sigma^{-1}(x.y)$$
Ainsi donc $\sigma^{-1}$ est un morphisme de groupe.
Remarquons aussi, que par définition $\sigma^{-1}$ est un endomorphisme sur $G$
Et que par définition également $\sigma^{-1}$ est aussi bijective.

Ainsi donc $\sigma^{-1}$ est un automorphisme, d'où $\sigma^{-1} \in Aut(G)$.
Il existe donc bien un inverse à tout élément de $Aut(G)$; la fonction inverse de ce dit élément: $Aut(G)$ est un groupe.
$$\tag*{$\blacksquare$}$$
## Définition de l'image et du noyau

Soit $\phi: G \to H$ un morphisme de groupe.
$1_G$ et $1_H$ respectivement les éléments neutres de $G$ et $H$

1. On définit son image, noté $Im(\phi)$ comme étant le sous groupe $\phi(G) \subset H$. On a $Im(\phi) = H$ si et seulement si $\phi$ est surjective
2. On définit son noyau, noté $Ker(\phi)$ comme étant le sous groupe $\phi^{-1}({1_H}) \subset G$

*Exemple:*
- $\phi: \mathbb{C} \to \mathbb{R}$ donnée par $z \mapsto \Re(z)$ est surjectif. Donc $Im(\phi) = \mathbb{R}$. De plus, $Ker(\phi) = i\mathbb{R}$
- $\phi: (\mathbb{R}, +) \to (\mathbb{U}, \times)$ est surjectif, de noyau $2\pi\mathbb{Z}$

## Injectivité par le noyau

### Proposition
Soit $\phi : G \to H$ un morphisme de groupes. Alors $\phi$ est injectif si et seulement si $Ker(\phi) = \set{1_G}$

#### Démonstration

$\Rightarrow$: Soit $x \in G$ tel que $\phi(x) = 1_H = \phi(1_G)$
Par injectivité de $\phi$, $x = 1_G$, donc $Ker(\phi) = \set{1_G}$

$\Leftarrow$: 
Soit $(x, x') \in G^2$, on a $\phi(x) = \phi(x')$, alors $\phi(x).\phi(x')^{-1} = 1_H$
D'après les [[Morphismes de groupes#Remarques importantes|remarques importantes]] on a donc $\phi(x.x'^{-1}) = 1_H$

Par hypothèse que $Ker(\phi) = \set{1_G}$, on sait que $x.x'^{-1} \in \set{1_G}$, donc $x.x'^{-1} = 1_G$
Soit alors $x = x'$. Donc $\phi$ est injective
$$\tag*{$\blacksquare$}$$
## Equivalence entre injection et surjection en groupe fini de même cardinal

### Proposition
Soit $\phi : G \to H$ un morphisme de groupes finis de même cardinal, alors on a l'équivalence suivante:
$$ \phi \text{ injective} \Leftrightarrow \phi \text{ surjective} \Leftrightarrow \phi \text{ bijective}$$
#### Démonstration
On prouvera $(1) \Rightarrow (2) \Rightarrow (3) \Rightarrow (1)$

$(1) \Rightarrow (2)$:
Soit $\phi$ injective. On a donc $|G| = |\phi(G)|$, or $|G| = |H|$ donc $|\phi(G)| = |H|$
Comme $\phi(G) \subseteq H$, on a bien $\phi(G) = H$ et donc $\phi$ est surjective ([[Morphismes de groupes#Définition de l'image et du noyau|d'après la définition.]])

$(2) \Rightarrow (3)$:
Soit $\phi$ surjective, alors $\phi(G) = H$. Si $\phi$ n'était pas injective, alors on aurait que $|H| = |\phi(G)| < |G|$. Ceci contredit l'hypothèse de cardinalité égale. 
Donc $\phi$ est injective.
Comme elle est à la fois surjective et injective, $\phi$ est bijective.

$(3) \Rightarrow (1)$
Si $\phi$ est bijective, alors elle est trivialement injective
$$\tag*{$\blacksquare$}$$

## Lemme sur l'existence d'une puissance neutre autre que 0

### Lemme
Soit $G$ est un groupe fini,, alors $\forall x \in G, \exists n \in \mathbb{N}^*$ tel que $x^n =  1_G$

### Démonstration
Admettons que ce ne soit pas le cas.
Supposons le [[Morphismes de groupes]] tel que:
$$ f: (\mathbb{Z}, +) \to (G, \times)$$
$$f: k \mapsto x^k$$
Il s'agit bien d'un morphisme de groupe car on a bien
<u>La stabilité de l'élément neutre:</u>
$$f(1_\mathbb{Z}) = f(0) = x^0 = 1_G$$
<u>La stabilité de la </u>[[Loi de composition interne (LCI)|LCI]]:
$$\forall p,q \in \mathbb{Z}, f(p+q) = x^{p+q} = x^p\times x^q = f(p)\times f(q)$$
S'il n'existe pas de $n \in \mathbb{N}^*$ tel que $x^n = 1_G$, alors ce morphisme est injectif.
Car en effet $f^{-1}(1_\mathbb{G}) = \set{1_\mathbb{Z}}$ (cf.[[#Définition de l'image et du noyau]])

Or ceci impliquerait que le groupe $G$ est infini, car $\mathbb{Z}$ est infini. Ceci entre en contradiction avec l'hypothèse que $G$ soit fini.
$$\tag*{$\blacksquare$}$$

