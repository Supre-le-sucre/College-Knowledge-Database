#probas 
## Définition
On dit que $X \sim Géo(p)$ si et seulement si #!

$X$ est une [[Variables aléatoires discrètes]] à valeurs dans $\mathbb N ^*$ et
$$\forall k \in \mathbb N ^*, \mathbb P(X = k) = p_X(k) = p(1-p)^{k-1}$$
<!--ID: 1707731928086-->


## Lien avec la [[Loi de Bernoulli]]
La loi géométrique a un lien direct avec la loi de Bernoulli: #!

On pose $(u_n)_{n \in \mathbb N}$ une suite de [[Variables aléatoires discrètes]] de [[Loi de Bernoulli |Bernouilli]] de paramètre $p \in ]0,1[$  indépendantes.
On note $T = \min{\set{n \in \mathbb N ^*; u_n = 1}}$, alors on a $T \sim Géo(p)$
<!--ID: 1707731928094-->

### Preuve
On a que dans ce cas $\set{T = k} = \set{u_1 = 0} \cap \cdots \cap \set{u_k = 1}$ 
Or, comme tous les événements sont indépendants: 
$$\mathbb P(T=k) = \prod_{l=1}^{k-1} \mathbb P(X_l = 0) \mathbb{P}(X_k = 1) = p(1-p)^{k-1}$$



## Propriété d'absence de mémoire
Soit $T \sim Géo(p)$ #!

On pose $n, m$ deux entiers quelconques. On a que:
$$\mathbb P(T > n+m\;|\; T > n) = \mathbb P (T > m)$$
La réciproque de cette propriété est vraie
<!--ID: 1707732555568-->

### Preuve
On se propose d'évaluer une partie de pile ou face

On considère les 3 événements suivants:
$\set{T > m}=$ Le 1er pile n'arrive qu'après le $m^{ème}$ lancer = $\set{u_1 = 0} \cap \cdots \cap \set{u_m=1}$  
$\set{T > n}=$ Le 1er pile n'arrive qu'après le $n^{ème}$ lancer = $\set{u_1 = 0} \cap \cdots \cap \set{u_n=1}$  
$\set{T > n + m}=$ Le 1er pile n'arrive qu'après le $(n+m)^{ème}$ lancer = $\set{u_1 = 0} \cap \cdots \cap \set{u_{(n+m)}=1}$

On a par définition de la [[Probabilité conditionnelle]]:
$$\mathbb P(T > n+m\;|\; T > n) = \frac{\mathbb P ( \set{T > n+m} \cap \set{T > n})}{\mathbb P (T > n)} = \frac{\mathbb P(T>n+m)}{\mathbb P(T > n)} $$
$$\frac{\mathbb P(T>n+m)}{\mathbb P(T > n)} = \frac{(1-p)^{n+m}}{(1-p)^n} = (1-p)^m = \mathbb P(T > m)$$
$$\tag*{$\blacksquare$}$$
