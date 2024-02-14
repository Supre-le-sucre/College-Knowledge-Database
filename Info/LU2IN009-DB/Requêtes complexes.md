En [[SQL]], il est aussi possible de gérer des requêtes plus complexes, sur plusieurs tables en simultanée et ainsi utiliser leur produit cartésien.
La syntaxe est la même, mais avec une énumération de table:

```sql
SELECT Atts
FROM Table1, Table2, ...
WHERE Condition
```

Il est possible d'avoir la même table concaténé avec elle même. On parle donc d'[[Autojointure]].
En connectant des tables différentes entre elles on utilise alors le principe de [[Jointure]]