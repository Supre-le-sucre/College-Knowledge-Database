## Définition de la convergence
Sur un espace métrique $(X, d)$, on dit que la suite $(x_n)_{n \in \mathbb N}$ converge vers une limite $l \in X$ lorsque: #!

$$\forall \epsilon > 0, \exists N \in \mathbb N, \forall n > N, d(u_n, l) < \epsilon$$
<!--ID: 1729504947001-->



## Caractérisation séquentielle de l'[[Notions de fermé, adhérence et frontière#Définition de l'adhérence|adhérence]]
Soit $(X, d)$ et $E \subseteq X$ #!

$$x \in \overline{E} \Leftrightarrow \exists(x_n)_{n \in\mathbb N}, \lim_{n \to + \infty} x_n = x$$
<!--ID: 1729504947004-->



### Preuve
[[Notions de fermé, adhérence et frontière#Propriété de l'adhérence|Rappelons que]] $x \in \overline{E} \Leftrightarrow \forall \epsilon > 0, B(x , \epsilon) \cap E \not= \emptyset$ 

$\Rightarrow$: Soit $x \in \overline{E}$. On pose $\epsilon = \frac{1}{n}$ Et on a donc $B(x, \frac{1}{n}) \cap E \not = \emptyset$ 
Donc il existe bien $(x_n)_{n \in \mathbb N}$ de $E$ tel que $d(x, x_n) < \frac{1}{n}$
La suite $x_n$ converge donc vers $x$

$\Leftarrow$: Soit $x \in X$ tel que $(x_n)_{n \in \mathbb N}$ de $E$ avec $\lim_{n \to +\infty} x_n = x$
Donc on a lors que
$$\forall \epsilon > 0, \exists N_\epsilon \in \mathbb N, \forall n > N_\epsilon, x_n \in B(x, \epsilon)$$

En particulier $x_ {N_\epsilon} \in B(x, \epsilon), \forall \epsilon > 0$
Donc $\forall \epsilon > 0, B(x, \epsilon) \cap E = \emptyset$
