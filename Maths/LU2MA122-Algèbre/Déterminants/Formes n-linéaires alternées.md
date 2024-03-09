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

## Dimension de l'espace des formes $r$-linéaires alternées
Soit $\Lambda^iE^\vee$ l'espace vectoriel des $i$-formes linéaires alternées. #!

On a alors que $\dim(\Lambda^iE^\vee) = \binom{n}{i}$ 

### Preuve


