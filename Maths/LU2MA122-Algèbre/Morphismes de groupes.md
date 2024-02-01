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
Soit $G$, un groupe. L'ensemble $Aut(G)$ des automorphismes de $G$, couplé avec la <u>composition</u> des applications comme [[Loi de composition interne (LCI)|LCI]] est un groupe.

#### Démonstration
La loi de composition est associative: $\forall \sigma \in Aut(G), Id_G\circ\sigma = \sigma \circ Id_G = \sigma$
De plus comme $\sigma$ est bijective
