## Définition
On définit une blockchain de la façon suivante: #!

Une blockchain est une structure de donnée distribuée et sécurisée qui fonctionne sans organe de contrôle. Autrement dit, il s'agit d'une structure de donnée disponible partout et géré seulement par ses utilisateurs.
Une blockchain organise donc ses données en bloc. Chaque bloc contient une partie des données à stocker et des *métadonnées* faisant notamment référence au bloc précédent. On obtient cette référence en appliquant une fonction de [[Hachage cryptographique]] sur les métadonnées du bloc précédent.

## Comparaison à la liste chaînée
Pour une blockchain il est possible de la comparer simplement à une liste chaînée de la façon suivante: #!

Chaque bloc est un élément de la liste, les pointeurs précédents sont des valeurs de hachage. Toutefois notons que la représentation est trop simpliste car dans une blockchain il est difficile:
- De modifier un bloc quelconque. Car une telle modification changerait sa valeur de hachage et impacterait le bloc suivant, puis le bloc d'après etc.
- De supprimer et d'ajouter des blocs à des positions quelconque. Car on aura des changement de métadonnées à répercuté de la même façon que précédemment.
Une blockchain ne permet donc en pratique que des ajouts en fin de liste.

## Contenu d'un bloc

### En-tête (ou métadonnées)
L'en-tête d'un bloc de blockchain contient plusieurs informations. Les principales étant: #!

- Une référence au bloc précédent (valeur de hachage de son en-tête)
- Un résumé des données du bloc (sous forme d'[[Arbres de hachage (ou arbre de Merkle)|arbre de hachage]])
	Notons qu'il suffit simplement de stocker la racine de l'arbre, car en cas de perte d'intégrité, la racine changera indubitablement.
- La date de création du bloc (sous format UNIX)
- Un mesure de la quantité de travail nécessaire à sa conception

### Données
Dans une blockchain, on appelle souvent les données, des "transactions". Chaque transaction contient notamment les données suivantes: #!

- La donnée en elle-même évidemment
- Une signature électronique (généré par la clé privée de l'utilisateur)
- Un moyen d'identifier l'auteur (la clé publique de l'utilisateur)

### Schématisation
![[Pasted image 20240509191958.png]]
