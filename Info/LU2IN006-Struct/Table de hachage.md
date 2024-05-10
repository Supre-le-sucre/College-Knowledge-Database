## Définition
On définit une table de hachage de la façon suivante: #!

Il s'agit d'un tableau où chaque élément est associé à une clé $k$, et stocké à la case $h(k)$ où $h$ est appelé fonction de hachage, et renvoie pour une clé donnée, un indice valide de la table de hachage
<!--ID: 1715341583391-->


## Fonction de hachage
Une bonne fonction de hachage minimise les collisions

### Le modulo
Une fonction de hachage basique serait d'appliquer un modulo simple sur la clé obtenue: $h(k) = k \;\%\; m$
Pour éviter les collisions le choix de $m$ est ici crucial: #!

Il faut notamment éviter les puissances de deux, et même s'en éloigner le plus possible. Sinon, on se retreint à une valeur simple valeur binaire, qui dépend du codage de la clé $k$
<!--ID: 1715341583394-->


### Fonction de Knuth
La fonction de hachage la plus connue et la plus optimale est celle de Knuth. Le choix de $m$ n'a plus réellement d'importance.

On a alors
$$h(k) = \lfloor m(xA - \lfloor xA\rfloor)$$
Avec $A \in ]0,1[$. Idéalement, on devrait utiliser le nombre d'or auquel on a retiré 1: $A = \frac{\sqrt 5 - 1}{2}$

De manière général, l'idéal est de travailler avec un irrationnel. Car en pratique pour tout $A$ irrationnel, on a que $h(x), h(x+1), \dots, h(x+n)$ sont éloignés les uns des autres.

## Problématique: Collision
Il est impossible d'empêcher les collisions dans une table de hachage en pratique. Il y a différente méthode pour résoudre ces problèmes de collisions.

### Résolution par chaînage
On peut résoudre la collision dans une table de hachage en procédant comme suit: #!

On résout la collision en stockant non plus des éléments dans la table de hachage, mais des listes chaînées d'élément. En cas de collision, l'élément est ajouté en tête de la liste chaînée déjà présente.
<!--ID: 1715341583395-->


#### Complexité
En considérant que le calcul $h(k)$ est en $O(1)$, on en déduit les complexité pour les fonctions de bases d'une table de hachage, où les collisions sont résolus par chaînage: #!

- <u>L'insertion</u> de nouveaux éléments se fait en $O(1)$ (car on insère en tête)
- <u>La suppression</u> d'un élément dont on connaît l'adressage est en $O(1)$ dans le cas de liste doublement chaînée
- <u>La recherche</u> se fait dans le pire cas en $O(n)$ si tous les éléments appartiennent à la même liste chaînée.
<!--ID: 1715341583397-->


##### Facteur de charge
En général, pour une table de hachage résolue par chaînage, on se doit de définir un *"facteur de charge"* pour obtenir des complexités réalistes: #!

On donne le facteur de charge $\alpha = \frac{n}{m}$ où $n$ le nombre d'éléments à stocker, et $m$ la taille de la table de hachage.
<!--ID: 1715341583398-->


##### Complexité selon le facteur de charge
En considérant le facteur de charge d'une table de hachage résolue par chaînage, la complexité est différente: #!

- <u>L'insertion</u> reste en $O(1)$
- <u>La suppression</u> reste en $O(1)$ pour des listes doublement chaînées
- <u>La recherche</u> est en $O(1)$ car au moins proportionnel au facteur de charge $\alpha$
<!--ID: 1715341583400-->


### Résolution par adressage ouvert
Pour effectuer une insertion par adressage ouvert dans une table de hachage: #!

On passe la clé dans la fonction de hachage. Si la case est occupé, on continue de parcourir la table de hachage jusqu'à la prochaine case vide. Il est important alors de stocker l'*"offset"* de notre élément dans la table de hachage.
La fonction de hachage prends alors 2 paramètres.
<!--ID: 1715341583402-->
