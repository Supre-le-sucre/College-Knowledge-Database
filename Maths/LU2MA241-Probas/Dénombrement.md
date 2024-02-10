#probas
## Définition
On dit qu'un ensemble est dénombrable, s'il est fini, ou qu'il existe une bijection entre cet ensemble et $\mathbb{N}$.
## Lemme de dénombrabilité selon les applications (admis)
On a le lemme suivant:
Soient $A$ et $B$ deux ensembles. 
- S'il existe une injection de $A$ dans $B$ et que $B$ est dénombrable, alors $A$ est dénombrable
- S'il existe une surjection de $A$ dans $B$ et que $A$ est dénombrable, alors $B$ est dénombrable

## Opérations sur les ensembles dénombrables

On a la propriété suivante:
1. Si $A_1, \cdots, A_n$ sont des ensembles dénombrables, alors $A_1 \times \cdots \times A_n$ , $\bigcup^n_{i=1}A_i$, $\bigcap^n_{i=1} A_i$   sont aussi des ensembles dénombrables.
2. Si $(A_i)_{i\in\mathbb{I}}$ est une [[Famille de sous-ensemble|famille]] dénombrable (i.e $I$ est dénombrable) d'ensemble finis ou dénombrables, alors $\bigcup^n_{i\in I}A_i$ est dénombrable. (Mais ceci n'est pas vraie pour l'intersection)

### Preuve
La preuve reposera sur le [[#Lemme de dénombrabilité selon les applications (admis)]]

On montre d'abord l'assertion 1.
Par hypothèse on a que $\rho_1: A_1 \to \mathbb{N}, \cdots ,\rho_n:A_n \to \mathbb{N}$ sont des bijections.

On pose $(p_k)_{k\in\mathbb{N}}$ la suite des nombres premiers. 
On pose $\psi : A_1 \times \cdots \times A_n \to \mathbb{N}$ telle que $\psi : (a_1, \cdots a_n) \mapsto 2^{\rho_1(a_1)}3^{\rho_2(a_2)}\cdots p_n^{\rho_n(n)}$

On a que $\psi$ est injective:
Supposons que $\psi(a_1, \cdots, a_n) = \psi(b_1, \cdots, b_n)$, alors par unicité des facteurs premiers on a...
$\rho_1(a_1) = \rho_1(b_1) \cdots \rho_n(a_n) = \rho_n(b_n)$. Comme les $\rho$ sont injectives: $a_1 = b_1 \cdots a_n = b_n$

Si $\psi$ est injective, sachant que $\mathbb{N}$ est dénombrable, on a par le [[#Lemme de dénombrabilité selon les applications (admis)|lemme]] que $A_1 \times \cdots \times A_n$ est dénombrable.
Les autres propriétés se démontre suivant le même principe.

### Corollaire
$\mathbb{Z}$ et $\mathbb{Q}$ sont dénombrables.
## Injection et Surjection

Soit $A$ et $B$ des ensembles finis. On donne $f: A \to B$ une application quelconque.

- Si $f$ est ==injective==, donc qu'un chaque élément de $A$ est associé au plus à un élément de $B$ , alors $|A| \leq |B|$
- Si $f$ est ==surjective==, donc chaque élément de $B$ est l'image d'au moins un élément de $A$, alors $|A| \geq |B|$
- Evidemment si $f$ est ==bijective== alors indubitablement $|A| = |B|$


