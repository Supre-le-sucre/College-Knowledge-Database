Si on a [[Convergence d'une suite]] $(u_n)_{n\in\mathbb{N}}$ vers une limite $l$, alors cette limite est unique

## Preuve
Soit $u_n$ une suite convergente vers une limite $l_1 \in \mathbb{R}$ et $l_2 \in \mathbb{R}$
Montrons que $l_1 = l_2$

Par [[Convergence d'une suite]] Soit $\epsilon > 0$, on obtient l'existence $N_1, N_2 \in \mathbb{N}^2$ tel que
$$ \forall n \geq N_1, |u_n - l_1| \leq \epsilon $$
$$\forall n \geq N_2, |u_n - l_2| \leq \epsilon $$
Soit $N = \max(N_1, N_2)$ on alors
$$ \forall n \geq N, |u_n - l_1| \leq \epsilon, |u_n - l_2| \leq \epsilon \Leftrightarrow\forall n \geq N, |u_n- l_1| + |u_n - l_2| \leq 2 \epsilon$$
Par [[Inégalité triangulaire]] de la valeur absolue, on peut alors poser $\forall n \geq N$
$$|u_n -l_1 - (u_n -l_2) | \leq |u_n- l_1| + |u_n - l_2| \leq 2\epsilon$$
$$\Leftrightarrow |u_n -l_1 - u_n +l_2 | \leq 2\epsilon$$
$$\Leftrightarrow |l_2 - l_1| \leq 2\epsilon$$
Ainsi donc, puisque $\epsilon$ aussi petit qu'on veut, on alors que...
$$ |l_2 - l_1| = 0 \Leftrightarrow l_2 = l_1$$
La limite d'une suite convergente est donc unique $Q.E.D$

