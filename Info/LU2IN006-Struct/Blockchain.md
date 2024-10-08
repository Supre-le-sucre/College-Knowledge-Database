## Définition
On définit une blockchain de la façon suivante: #!

Une blockchain est une structure de donnée distribuée et sécurisée qui fonctionne sans organe de contrôle. Autrement dit, il s'agit d'une structure de donnée disponible partout et géré seulement par ses utilisateurs.
Une blockchain organise donc ses données en bloc. Chaque bloc contient une partie des données à stocker et des *métadonnées* faisant notamment référence au bloc précédent. On obtient cette référence en appliquant une fonction de [[Hachage cryptographique]] sur les métadonnées du bloc précédent.
<!--ID: 1715276081962-->


## Comparaison à la liste chaînée
Pour une blockchain il est possible de la comparer simplement à une liste chaînée de la façon suivante: #!

Chaque bloc est un élément de la liste, les pointeurs précédents sont des valeurs de hachage. Toutefois notons que la représentation est trop simpliste car dans une blockchain il est difficile:
- De modifier un bloc quelconque. Car une telle modification changerait sa valeur de hachage et impacterait le bloc suivant, puis le bloc d'après etc.
- De supprimer et d'ajouter des blocs à des positions quelconque. Car on aura des changement de métadonnées à répercuté de la même façon que précédemment.
Une blockchain ne permet donc en pratique que des ajouts en fin de liste.
<!--ID: 1715276081967-->


## Contenu d'un bloc

### En-tête (ou métadonnées)
L'en-tête d'un bloc de blockchain contient plusieurs informations. Les principales étant: #!

- Une référence au bloc précédent (valeur de hachage de son en-tête)
- Un résumé des données du bloc (sous forme d'[[Arbres de hachage (ou arbre de Merkle)|arbre de hachage]])
	Notons qu'il suffit simplement de stocker la racine de l'arbre, car en cas de perte d'intégrité, la racine changera indubitablement.
- La date de création du bloc (sous format UNIX)
- Un mesure de la quantité de travail nécessaire à sa conception
<!--ID: 1715276081969-->


### Données
Dans une blockchain, on appelle souvent les données, des "transactions". Chaque transaction contient notamment les données suivantes: #!

- La donnée en elle-même évidemment
- Une signature électronique (généré par la clé privée de l'utilisateur)
- Un moyen d'identifier l'auteur (la clé publique de l'utilisateur)
<!--ID: 1715276081970-->


### Schématisation
![[Pasted image 20240509191958.png]]

## Fonctionnement
Une blockchain fonctionne de la façon suivante: #!

Chaque utilisateur possède une copie intégrale de la blockchain en local, ainsi qu'une clé privée permettant de signer ses transactions, et une clé publique pour permettre aux autres utilisateurs de l'identifier. Certains utilisateurs, appelés "mineurs" ont pour rôle de créer les blocs regroupant les transaction valides en attente.
Quand un bloc est créé par un mineur, il est horodaté et tous les utilisateurs doivent l'ajouter à leur blockchain locale.
<!--ID: 1715276081972-->


### Algorithme de consensus
Pour sécuriser une blockchain et la  rendre fiable, on met en place en algorithme de consensus: #!

C'est un mécanisme permettant de mettre d'accord les utilisateurs sur la création et l'enchaînement des blocs en cas de bifurcations/nouvelles branches.
Le plus connu est le consensus *"proof of work"*: il est demandé aux mineurs de réaliser un travail nécessitant une certaine puissance. On choisit ensuite la chaîne ayant demandé le plus de travail accumulée. De cette manière un agent malveillant souhaitant faire accepter sa branche doit fournir une puissance de calcul équivalente aux autres mineurs légitime mettant leur puissance en commun.
<!--ID: 1715276081974-->


## Défis liés à la blockchain
On peut observer les défis suivants: #!

- <u>Identité numérique</u>: Il est nécessaire de pouvoir certifier l'identité des utilisateurs, tout en garantissant l'anonymat et la traçabilité des transactions
- <u>Le passage à l'échelle</u>: Les validations peuvent prendre du temps selon l'algorithme de consensus utilisé. Notamment le *"proof of work"* ne permet que de valider quelques transactions par seconde, car une puissance de calcul conséquente doit être fournie par chacun
- <u>Enjeu environnemental</u>: La création et validation d'un bloc sont extrêmement énergivore. Il faut trouver des algorithmes de consensus et des moyens de calculs permettant d'optimiser les ressources énergétiques et de maximiser la sécurité.
<!--ID: 1715276081976-->
