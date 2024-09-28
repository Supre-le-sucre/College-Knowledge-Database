## Définition
On considère un [[Espace mesurable#Définition d'espace mesuré|espace mesuré]] $(E, \mathcal E, \mu)$. On donne les mots de vocabulaire suivants sur la mesure $\mu$: #!

- $\mu(E)$ est la masse de $\mu$ et on dit que $\mu$ est finie si sa masse est finie. 
	Si la masse de $\mu$ vaut 1, alors on dit que $\mu$ est une probabilité
- $\mu$ est qualifiée de $\sigma$-finie s'il existe une suite $(E_n) \in \mathcal E^\mathbb N$ telle que
	$\bigcup E_n = E$ et $\mu(E) < \infty$
- $\mu$ est qualifiée de somme de mesure finie, s'il existe une suite de mesure de $(E, \mathcal E)$ telle que
	$\mu = \sum_{n \in \mathbb N} \mu_n$
- Soit $x \in E$ tel que $\set{x} \in \mathcal E$, on dit que c'est un atome de $\mu$ si
	$\mu(\set{x}) > 0$. Autrement, si $\mu$ n'a pas d'atome, on qualifie alors la mesure de diffuse
<!--ID: 1727551528557-->


## Equivalence des définitions
On observe les équivalences suivantes: #!

i) $\mu$ est $\sigma$-finie
ii) $\exists A_n \in \mathcal E^\mathbb N$ avec $A_n \subseteq A_{n+1}$ tel que $\bigcup A_n = E$ et $\mu(A_n) < \infty \; \; \forall n \in\mathbb N$
iii) $\exists B_n \in \mathcal E^\mathbb N$ 2 à 2 disjoints tel que $\bigcup B_n = E$ et $\mu(B_n) < \infty \; \; \forall n \in\mathbb N$
<!--ID: 1727551528558-->

