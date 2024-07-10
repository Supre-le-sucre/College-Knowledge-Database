Ocaml est un langage fortement typé, et les opérations entre variables doivent donc utiliser les bons types

# Opérateurs
Les opérateurs suivants sont infixes, cela signifie qu'il se mettent entre les deux valeurs à opérer.

| Opérations...  | Entre entiers  | Entre floattants |
| -------------- | -------------- | ---------------- |
| addition       | +              | +.               |
| soustraction   | -              | -.               |
| multiplication | *              | *.               |
| division       | / (entière)    | /.               |
| modulo         | mod            | *N'existe pas*   |
| puissance      | *N'existe pas* | **               |
Il est possible de rendre ces opérateurs suffixes en les mettant entre parenthèses:
```
# (+) 3 2 ;;
- : int = 5

# (-) 3 2 ;;
- : int = 1

# (-) 2 3 ;;
- : int = -1
``` 
