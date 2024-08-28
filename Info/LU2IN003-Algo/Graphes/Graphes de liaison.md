#algo 
## Définition
On définit $\mathcal A(L) = (V(L), H(L))$ un graphe de liaison associé à un [[Parcours#Sous-parcours|sous parcours]] $L$ si tout sommet $v \in V(L)$ sont dans le parcours $L$ et $H$ l'ensemble des arcs tel que le sommet initial du parcours $L$ est une [[Graphes orientés#Définition de la racine|racine]] 

## Théorème d'existence 
A tout sous-parcours $L$ de $G$, on peut y associer un graphe de liaison $\mathcal A(L) = (V(L), H(L))$

### Preuve
Par récurrence sur $n \in \mathbb N^*$ $\Pi(n):$ "A tout sous parcours de longueur $n on eut associer au moins un graphe de liaison"

(I): Soit $L = [v]$ un sous parcours de longueur $1$. Le graphe $(\{v\}, \emptyset)$ est un graphe de liaison

(H): Soit $\Pi(n)$ montrons $\Pi(n+1)$
Soit $L$ un sous-parcours de longueur $n+1$. On considère le sous parcours `L[:n]` est un sous-parcours de longueur $n$ donc il admet un graphe de liaison par H.R que l'on nomme $G=(V, A)$.

Soit $v$ le $(n+1)^{ème}$ sommet de $L$. Comme $L$ est un sous-parcours, on a que $v$ admet un prédécesseur avant lui, donc dans $V$.
Le graphe $(V \cup \{v\}, A \cup \{(u,v)\})$ est donc bien un graphe de liaison de $L$
