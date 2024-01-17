Une association est un lien entre des [[Entités]], et il est possible d'avoir plusieurs associations entre les mêmes entités.

Une association est unique, mais peut se regrouper avec d'autres associations de même type dans des [[Classe d'associations]]

### La cardinalité d'une association

Pour certaines association, il est nécessaire de limiter son nombre et/ou de rendre obligatoire sa création un certain nombre de fois.

Par exemple, dans le cas d'un étudiant inscrit à l'université. Son inscription dans un module est obligatoire, et il ne peut pas être inscrit dans plus de 7 modules. Ainsi, la cardinalité d'une telle association est de [1, 7] de l'étudiant vers le module.