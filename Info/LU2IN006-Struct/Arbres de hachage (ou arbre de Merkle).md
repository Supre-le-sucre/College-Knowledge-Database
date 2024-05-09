## Définition
On définit un arbre de hachage (ou arbre de Merkle) de la façon suivante: #!

Un arbre de hachage est une structure de données qui permet de résumer un ensemble de données et de pouvoir garantir efficacement leur intégrité. On le présente sous la forme d'un [[Arbres]] où chaque feuille correspond à la valeur de hachage d'une partie de ces données obtenu par [[Hachage cryptographique]]. 
La valeur des nœuds internes est obtenue en appliquant la fonction de hachage sur les concaténation des valeurs de hachage de ses fils. ![[Pasted image 20240509185743.png]]
<!--ID: 1715276081978-->


## Remarque sur la construction
On construit un arbre de hachage de la façon suivante: #!

Elle se fait niveau par niveau, de la feuille jusqu'à la racine.
Si un niveau contient un nombre de nœuds impaire, on duplique le hash du dernier nœud pour le concaténer et créer le père. ![[Pasted image 20240509185926.png]]
<!--ID: 1715276081979-->


## Vérification de l'intégrité par l'arbre de Merkel
On énonce le principe suivant: #!

Pour vérifier l'intégrité des données, il suffit de connaître la valeur de hachage de la racine de l'arbre et la fonction de hachage utilisée. En effet, si le hash est différent à la racine, c'est que des données ont été corrompues.
En cas de doute sur une partie des données, il suffit de connaître la valeur de hachage des nœuds intervenant dans la construction du chemin de la feuille concernée vers la racine.
<!--ID: 1715276081981-->
