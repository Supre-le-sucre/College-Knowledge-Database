## Définition
On définit $E_1, \dots, E_r$ $r$ $\mathbb K$-[[Espaces vectoriels]]
On dit que $f: E_1 \times \cdots \times E_r$ est une forme $r$-linéaire si et seulement si: #!
$$\forall i \in [1, r], f_i: x_i \mapsto(a_1, \cdots,a_{i-1}, x_i, a_{i+1}, \cdots, a_r)$$
On a que $f_i$ est une application linéaire
<!--ID: 1709998087881-->


## Définition
Une forme $r$-linéaire $f: E^r \to F$ est dite alternée si: #!
$$f(x_1, \dots, x_r) = 0 \Rightarrow \exists i,j, i <j, x_i = x_j$$
Autrement dit, on peut noter que $\forall(x_1, \cdots, x_n) \in E^r$
$$f(x_1, \cdots, x_i +x_j, \cdots, x_j +x_i, \cdots, x_n) = 0$$
$$f(x_1, \cdots, x_i, \cdots, x_j, \cdots,  x_n) +f(x_1,\cdots, x_j, \cdots, x_i,\cdots, x_n) = 0$$
<!--ID: 1709998087888-->

## Propriété de permutation
Dans le cas d'une forme $f$ étant $r$-linéaire alternée, on a pour toute permutation $\sigma \in S_n$ du [[Groupe symmétrique]] le résultat suivant: #!
$$f(x_{\sigma(1)}, \cdots, x_{\sigma(r)}) = \epsilon(\sigma)f(x_1, \cdots, x_r)$$
où $\epsilon$ la [[Signature]] de $\sigma$
<!--ID: 1709999896083-->


## Dimension de l'espace des formes $r$-linéaires alternées
Soit $\Lambda^iE^\vee$ l'espace vectoriel des $i$-formes linéaires alternées. #!

On a alors que $\dim(\Lambda^iE^\vee) = \binom{n}{i}$ 
<!--ID: 1709999896090-->


### Preuve
Soit $i \in \mathbb N^*, f \in \Lambda^iE^\vee$. On pose $(e_1, \cdots, e_n)$ une base de $E$
Par $i$-linéarité, $f$ est déterminée par son image sur les $i$-uplets $(e_{l_1}, \cdots, e_{l_i})$

Si $i > n$, alors on a obligatoirement, dans un tel $i$-uplet, au moins deux fois le même vecteur.
Comme $f$ est une forme alternée, $f = 0$ partout, et donc $\Lambda^iE^\vee = \set{0}$

Si $i \leq n$, alors à nouveau, comme $f$ est alternées, elle sera déterminée par $(e_{l_1}, \cdots, e_{l_i})$ tous distincts.
En effectuant des permutations sur ce $i$-uplet, $f$ a toujours la même valeur à plus ou moins 1 près d'après [[#Propriété de permutation]]. L'important  est donc le choix des $e_k$ dans ce $i$-uplet, peu importe l'ordre dans lequel ils se trouvent.

Pour compter le nombre de $i$-uplet qu'il est possible de construire alors, cela à choisir $i$ éléments parmi $n$, soit $\binom{n}{i}$ 
$$\tag*{$\blacksquare$}$$
**Remarque**: Dans le cas où $E$ est de dimension $n$, tout forme $n$-linéaire alternée de $E$ est pleinement défini par $f(b_1, \cdots, b_n)$ pour une base $(b_1, \cdots, b_n)$ de $E$ 

## Définition du déterminant
Soit $E$ un $\mathbb K$-espace vectoriel de dimension finie $n$ avec $u \in \mathcal{L}(E)$, alors il existe un unique élément $det(u) \in \mathbb K$ tel que $\forall f \in \Lambda^nE^\vee$ on a: #!
$$f \circ u = det(u)f$$
**Remarque**:
Ceci nous donne immédiatement que $det(Id_E) = 1$ et que $det(0_E) = 0$ (on rappelle que $f$ étant une forme $n$-linéaire alternée)
<!--ID: 1709999896094-->

### Preuve
Tout d'abord, il va de soi de de dire que si $u \in \mathcal L(E)$ et $f \in \Lambda^n E^\vee$, $f \circ u \in \Lambda^nE^\vee$
On sait aussi également que $dim(\Lambda ^nE^\vee) = 1$ d'après [[#Dimension de l'espace des formes $r$-linéaires alternées]], on a l'existence de $f_0$ tel que $\forall f \in \Lambda^nE^\vee, f= \lambda f_0$ et $\lambda \in \mathbb K$

Si l'on montre qu'il existe un unique $det(u)$ tel que $f_0 \circ u = det(u)f_0$, on aura aussi montré ceci pour tout $f$ (car le $\lambda$ s'annulera des deux côté de l'égalité (il est inversible car dans un corps))

Or $f_0$ est une forme $n$-linéaire, tout comme $f_0 \circ u$. Elles sont donc différentes à un coefficient près. Ce coefficient est bien $det(u)$

## Propriété du déterminant sur la composition
Soit $E$ un $\mathbb K$-[[Espaces vectoriels]] de dimension $n$, $u,v \in \mathcal L(E)$, alors on a l'égalité suivante sur la composition: #!

$$det(u \circ v ) = det(u)det(v)$$

### Preuve
Soit $f \in \Lambda^nE^\vee$ non-nulle, on a par la [[#Définition du déterminant]] que:
$$f \circ u \circ v = det(u\circ v)f$$
Puisque $f \circ u \in \Lambda^nE^\vee$ on a donc aussi:
$$f \circ u \circ v = det(v)f \circ u = det(v)det(u)f$$
d'où finalement l'égalité, car $f$ non nulle
$$det(u\circ v)f = det(v)det(u)f \Leftrightarrow det(u \circ v) = det(u)det(v)$$

### Corollaire
Soit $E$ un $\mathbb K$-[[Espaces vectoriels]] de dimension finie, $u \in \mathcal L(E)$, alors on a l'équivalence suivante pour $det(u)$: #!
$det(u) \in \mathbb K^\times$, si et seulement si $u$ est bijectif, et $det(u^{-1}) = det(u)^{-1}$

**Remarque:** puisque que $\mathbb K$ est un [[Corps]], on a que $\mathbb K^\times =\mathbb K - \set{0}$
#### Preuve
$\Leftarrow$
Si $u$ est une bijection, alors on peut noter $u^{-1}$ son application inverse
On observe alors par [[#Propriété du déterminant sur la composition]] et sachant que $det(Id_E) = 1$
$$det(u)det(u^{-1}) = 1$$
Ceci montrant donc que $det(u)$ admet un inverse et donc que $det(u) \in \mathbb K^\times$
On peut donc, comme cet inverse est unique, poser sans problème: $det(u^{-1}) = det(u)^{-1}$

$\Rightarrow$
On propose de raisonner par la contraposée, à savoir: $u$ n'est pas bijectif $\Rightarrow$ $det(u) \not \in \mathbb K^\times$ 
On prends alors $u$ non bijectif.

$u$ ne peut pas être injectif, car comme $u \in \mathcal L(E)$, elle serait bijective dans ce cas
Posons $x \in Ker(u)$ non-nul, alors on le complète en une base $(x, b_2, \dots, b_n)$ de $E$, de telle sorte que si $f$ est une forme $n$-linéaire alternée non-nulle:
$$f \circ u (x, b_2, \dots, b_n) = f(u(x), u(b_2), \dots, u(b_n)) = 0 = det(u)f(x, b_2, \dots, b_n)$$
Car comme $u(x) = 0$, donc la forme $f$ est nulle en premier paramètre.
or puisqu'aucun élément $(x, b_2, \dots, b_n)$ n'est nulle et qu'elle détermine $f$, on a $f(x, b_2, \dots, b_n) \not = 0$ car $f \not = 0$.
On a alors $det(u) = 0$, mais alors $det(u) \not \in \mathbb K^\times$

## Proposition