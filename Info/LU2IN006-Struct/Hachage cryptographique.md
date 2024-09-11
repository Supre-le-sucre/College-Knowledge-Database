## Définition
On peut définir une fonction de hachage cryptographique de la manière suivante: #!

Il s'agit d'une fonction de hachage déterministe qui retourne une valeur de hachage de ==taille fixe== et ce, qu'importe la taille de la donnée en entrée. Elle doit être "facile" à calculer mais impossible à inverser en pratique. On peut aussi désirer d'autres propriétés: 
- Modifier légèrement la donnée d'entrée renvoie une valeur hachée très différente
- Deux données différente ne devraient pas avoir la même valeur hachée
On connaît notamment les fonctions de hachage suivante: Message Digest (MD4, MD5) ou Secure Hash Algorithm (SHA-1, SHA-2)
<!--ID: 1715276081983-->


## Applications courantes
Une fonction de hachage cryptographique sert dans les cas suivants: #!

- <u>La vérification de mot de passe:</u> Le stockage de mot de passe en clair n'étant pas recommandable, on stocke plutôt la valeur haché d'un mot de passe et on compare la valeur hachée de la donnée envoyé par l'utilisateur avec la valeur hachée du mot de passe stocké.
- <u>Catalogue de donnée complexe</u>: Comme une fonction de hachage cryptographique a une taille fixe, peu importe la donnée passée en paramètre, il est possible de stocker des résultats de tels fonctions de hachage pour vérifier si une structure de donnée complexe se trouve dans une base de donnée, en comparant les différents hash
- <u>Signature électronique</u>: On peut chiffrer la valeur de hachage envoyé par un message. Ce chiffrement correspond à notre signature. Pour vérifier l'identité de l'émetteur, on vérifie donc si le déchiffrage de la valeur haché du message renvoie la valeur hachée attendue.
<!--ID: 1715276081985-->


## Utilité sur les logiciel de gestion de versions

### Définition d'un VCS (Version Control System)
On le définit de la façon suivante: #!

Un logiciel de gestion de version (ou VCS) permet de stocker un ensemble de fichier tout en conservant l'historique des modifications. En particulier, il permet de créer et de conserver le code source relative à différentes versions d'un projet ou d'une application.
Le plus connu est `Git`
<!--ID: 1715276081986-->


### Intérêt du hachage cryptographique dans les VCS
On peut observer l'intérêt suivant: #!

Comme la fonction de hachage cryptographique renvoie une valeur différente lorsqu'une donnée différente est passée en paramètre, on peut donc stocker les modifications en hachant les fichiers et en les stockant dans les dossiers de versions correspondants.
<!--ID: 1715276081988-->



