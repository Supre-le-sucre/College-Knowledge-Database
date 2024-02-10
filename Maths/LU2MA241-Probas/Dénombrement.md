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
On pose les applications $\rho_1: A_1 \to \mathbb{N}, \cdots ,\rho_n:A_n \to \mathbb{N}$ 
## Injection et Surjection

Soit $A$ et $B$ des ensembles finis. On donne $f: A \to B$ une application quelconque.

- Si $f$ est ==injective==, donc qu'un chaque élément de $A$ est associé au plus à un élément de $B$ , alors $|A| \leq |B|$
- Si $f$ est ==surjective==, donc chaque élément de $B$ est l'image d'au moins un élément de $A$, alors $|A| \geq |B|$
- Evidemment si $f$ est ==bijective== alors indubitablement $|A| = |B|$


