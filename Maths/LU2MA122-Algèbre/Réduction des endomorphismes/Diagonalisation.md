## Définition
Soit $\mathbb K$ un corps avec $E$ un $\mathbb K$-espace vectoriel de ==dimension finie==
On dit que $u \in \mathcal L(E)$ et $M \in M_n(\mathbb K)$ sont diagonalisable si et seulement si: #!

- Pour $u \in \mathcal L(E)$ il existe une base $B$ pour laquelle la matrice $Mat_B(u)$ est diagonale
- Pour $M \in M_n(\mathbb K)$ lorsqu'il existe $P \in GL_n(\mathbb K)$ tel que $PMP^{-1}$ est diagonale
<!--ID: 1715537862477-->


## Théorème
Soit $E$ un $\mathbb K$ espace vectoriel de dimension $n$ et $u \in \mathcal L(E)$, les assertions suivantes sur la diagonalisation sont équivalentes: #!

- $(i)$ $u$ est diagonalisable
- $(ii)$ Il existe une base de vecteurs propres de $E$
- $(iii)$ On a la décomposition en somme directe $E = \bigoplus_{\lambda \in Sp(u)} E_\lambda$ 
- $(iv)$ Le polynôme caractéristique $\mathcal X_u$ est *"scindé"* et $\dim(E_\lambda) = m(\lambda)$, où m donne la multiplicité d'une racine dans $\mathcal X_u$
- $(v)$ Il existe un polynôme $P \in \mathbb K[X]$ scindé à racines simples tel que $P(u)= 0$
<!--ID: 1715537862479-->


### Preuve
On montre $(i) \Leftrightarrow (ii)$

 Si $B = (x_1, \dots, x_n)$ la base dans laquelle $Mat_B(u)$ est diagonale, à coefficient diagonaux $\lambda_i$, alors on a que $u(x_i) = \lambda_ix_i$ donc $x_i$ sont des vecteurs propres.
Réciproquement, en considérant la base de vecteur propre $B=(x_1, \dots, x_n)$ on a que $u(x_i) = \lambda_ix_i$ et donc $Mat_B(u)$ est diagonale à coefficient diagonaux $\lambda_i$

Montrons maintenant $(ii) \Leftrightarrow (iii)$ 
Si $(x_1, \dots, x_n)$ est une base de vecteurs propres, de valeurs propres distinctes $\lambda_1, \dots \lambda_s$.
On considère pour chaque $\lambda_k$, l'espace $E_k = Vect(x_{k_1}, \dots x_{k_l})$ où chaque $x_k$ sont de valeurs propres $\lambda_k$
On a alors $$E = \bigoplus^s_{k=1}E_k \subset \bigoplus_{\lambda \in Sp(u)}E_\lambda \subset E$$Ce qui justifie l'égalité. En particulier $E_k = E_{\lambda_k}$ 
Réciproquement si $E = \bigoplus_{\lambda \in Sp(u)} E_\lambda$ il suffit de prendre pour chaque $\lambda \in Sp(u)$, une base $B_\lambda$ de $E_\lambda$. On aura donc que $\bigcup_{\lambda \in Sp(u)}B_\lambda$ est une base de vecteur propre

On montre $(ii) \implies (iv)$
Soit la base $B$ de vecteurs propres dans laquelle $Mat_B(u)$ est une matrice diagonale de coefficient $\lambda_i$

On obtient que
$$\mathcal X_u = \prod^n_{i=1}(X -\lambda_i) = \prod_{i=1}^s(X-\lambda_i)^{m(\lambda_i)}$$
où $\lambda_1, \dots, \lambda_s$ deux à deux distincts. On a que $m(\lambda_i) = dim(E_{\lambda_i})$

On montre $(iv) \implies (v)$
Si $\mathcal X_u$ est scindé, on l'écrit $\mathcal X_u = \prod_{i=1}^s(X-\mu_i)^{m_i}$ avec $\mu_i$ distincts.
Comme $\mathcal X_u = n$, on a que $\sum_{i=1}^sm_i = n$.
Soit $P=\prod^s_{i=1}(X-\mu_i)$, le polynôme scindé en racine simple. Montrons que $P(u) = 0$

Par le [[Polynômes d'endomorphismes#Lemme des noyaux|lemme des noyaux]] on a que
$$\ker(P(u)) = \bigoplus_{i=1}^sE_{\mu_i}$$
Or par hypothèse on a que $\dim E_{\mu_i} = m_i$, soit alors que $dim(\ker(P(u))) = \sum^s_{i=1}=n$ et $\ker(P(u)) = E$. Donc on a bien $P(u) = 0$

Montrons finalement $(v) \implies (iii)$
Si $P$ est annulateur à racines simples, on a que $P = \prod^s_{i=1}(X -\mu_i)$ avec $P(u) = 0$
d'où $\ker(P(u)) = E$ par le [[Polynômes d'endomorphismes#Lemme des noyaux|lemme des noyaux]] on a bien que $E = \bigoplus_{i=1}^s E_{\mu_i}$
$$\tag*{$\blacksquare$}$$

### Corollaire conséquence de la nilpotence et de la diagonalisation
On observe le corollaire suivant: #!

Soit $u \in \mathcal L(E)$ on suppose $u$ diagonalisable et nilpotent (i.e $\exists r \in \mathbb N, u^r = 0$) alors on a que $u= 0$
<!--ID: 1715537862480-->


#### Preuve
Si $u$ est diagonalisable, alors il admet une base de vecteurs propres.
Soit $\lambda$ une valeur propre de $u$, on a que pour $x$ un vecteur propre associé à cette valeur propre, on a que: $u(x) = \lambda x$
Comme $u$ est nilpotent on observe que pour $r \in \mathbb N$
$$u^r(x) = 0 = \lambda^rx$$
Or comme $x$ n'est pas un vecteur nul, seul $\lambda = 0$
Donc les vecteurs propres de $u$ sont tous nulles.
Dans la base de vecteur propre cela signifie que $u = 0$. Et comme cette base est aussi une base de $E$ on a prouvé la généralité
$$\tag*{$\blacksquare$}$$

