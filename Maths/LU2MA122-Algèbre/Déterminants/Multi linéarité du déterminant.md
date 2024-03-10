## Théorème
Soit $\phi_C : \mathbb K^n \times \dots \times \mathbb K^n \to \mathbb K$ l'application sur les colonnes d'une matrice $M_n$ déterminée par
$(C_1, \dots, C_n) \mapsto det(C_1, \dots, C_n)$. Et soit aussi pour la base canonique de $\mathbb K^n$, la forme $f_{can} \in \Lambda^n\mathbb K^n$ définie par $f(e_1, \dots, e_n) = 1$ #!

On a alors $\phi_C = f_{can}$. Plus particulièrement, $\phi_C$ est une forme $n$-linéaire alternée
Si on pose $\phi_L$ pour les lignes de $M_n$ cette fois, on aura alors $\phi_L = f_{can} \circ tr$ où $tr$ l'application de transposition.

### Preuve
Soit $(C_1, \dots, C_n)$ un $n$-uplet de colonnes, $M$ la matrice associée d'endomorphisme $u_M$.
On a alors par [[Formes n-linéaires alternées#Définition du déterminant|définition]] que
$$f_{can}(C_1, \dots, C_n) = f_{can} \circ u_m(e_1, \dots,e_n) = det(u_m)f_{can}(e_1, \dots, e_n)$$
Or $det(u_m) = det(M)$ comme vu en [[Déterminant matriciel]] d'où...
$$det(u_m)f_{can}(e_1, \dots, e_n) = det(M)f_{can}(e_1, \dots, e_n)= det(M)$$
Or par définition on a:
$$f_can(C_1, \dots, C_n) = det(M) = \phi_C(C_1, \dots, C_n)$$
Pour la remarque sur $\phi_L$, il suffit d'utiliser l'égalité $det(M) = det(^tM)$ (vu en [[]])
$$\tag*{$\blacksquare$}$$
