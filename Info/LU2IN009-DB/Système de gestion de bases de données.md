#db
## Différence entre un SGBD et un système de fichiers
Les différences entre la gestion d'une base de données et celle d'un système de fichiers sont multiples, bien qu'ils sont similaires.

**Remarque**: Le SGBD (Système de gestion de base de données) est appelé en anglais DataBase management system (DBMS)

### Accès aux fichiers
Les données sont accessibles de manières plus claires, basées sur la donnée recherchée elle même.
Elles sont aussi accessible plus rapidement, au lieu de charger un fichier très volumineux, il est possible de centraliser sa recherche sur des éléments précis.

### Redondance
La redondance de fichiers est aussi de mise, la même donnée est répétée dans différents fichiers dans un système de fichiers contrairement à une base de donnée qui les centralise.

### Cohérence
La cohérence des données est plus efficace dans une base de donnée, car il est possible de les connecter avec d'autres données

### Concurrence
Une base de donnée maximise la concurrence pour permettre un meilleur temps d'exécution. Cependant, contrairement à un système de fichier classique, la concurrence est maîtrisée, et les sections critiques sont synchronisées sans lever de problème de cohérence.

### Sécurité
Une base de donnée peut gérer différentes sensibilités de données différentes, là où un système de fichier ne peut que les protéger par utilisateurs.