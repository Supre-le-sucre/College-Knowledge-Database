## Définition
On définit un arbre de hachage (ou arbre de Merkle) de la façon suivante: #!

Un arbre de hachage est une structure de données qui permet de résumer un ensemble de données et de pouvoir garantir efficacement leur intégrité. On le présente sous la forme d'un [[Arbres]] où chaque feuille correspond à la valeur de hachage d'une partie de ces données obtenu par [[Hachage cryptographique]]. 
La valeur des nœuds internes est obtenue en appliquant la fonction de hachage sur les concaténation des valeurs de hachage de ses fils. ![[Pasted image 20240509185743.png]]

## Remarque sur la construction
On construit un arbre de hachage de la façon suivante: #!

Elle se fait niveau par niveau, de la feuille jusqu'à la racine.
Si un niveau contient un nombre de nœuds impaire, on duplique le hash du dernier nœud pour le concaténer et créer le père. ![[Pasted image 20240509185926.png]]

## Vérification de l'intégrité par l'arbre de Merkel
On énonce le principe suivant: #!
