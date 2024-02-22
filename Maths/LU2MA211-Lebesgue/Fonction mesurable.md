## Définition
Soit $(\Omega, \mathcal F)$ et $(\Omega', \mathcal F')$ deux espaces mesurables. Une application de $f: \Omega \to \Omega'$ est dite mesurable si et seulement si
$$\forall A \in \mathcal F', f^{-1}(A) \in \mathcal F$$
Remarquons que la mesurabilité d'une fonction ne dépend aucunement de la mesure.
### Exemple
Tout application constante de $\Omega$ dans $\mathbb R$ est mesurable
En effet pour $f = k$ si on considère l'espace mesurable $(\Omega, \mathcal F)$ on a que
$\forall A \in \mathcal P(\Omega)$, si $k \in A$, alors $f^{-1}(A) = \Omega \in \mathcal F$, sinon $f^{-1}(A) = \emptyset \in \mathcal F$ (cf. [[Maths/LU2MA211-Lebesgue/Tribu#Propriétés issue de la définition|Tribu]])


### Similitude avec la définition de continuité topologique
Une application $f: E \to E'$ entre deux espaces métriques est continue si et seulement si
$$\forall \mathcal O \subset E' \text{ ouvert}, f^{-1}(\mathcal O) \subset E \text{ ouvert}$$
C'est en réalité une simple généralisation de la propriété de continuité sur $\mathbb R$ 