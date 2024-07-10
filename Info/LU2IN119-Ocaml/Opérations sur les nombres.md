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

# Fonctions
On observe l'existence des fonctions suivantes dans le langage:

- `ceil x`: Renvoie la partie entière supérieure de `x`
- `floor x`: Renvoie la partie entière inférieure de `x`
- `sqrt x`: Renvoie la racine carrée de `x`
- `log x`: Renvoie le logarithme népérien de `x`
- `log10 x`: Renvoie le logarithme en base 10 de `x`
- `cos x` Renvoie le cosinus de `x` en radiant
- `sin x` Renvoie le sinus de `x` en radiant
- `tan x` Renvoie la tangente de `x` en radiant
- `acos x` Renvoie l'arccosinus de `x` en radiant
- `asin x` Renvoie l'arcsinus de `x` en radiant
- `atan x` Renvoie l'arctangente de `x` en radiant
# Egalités

On observe l'existence des opérateurs booléens suivants
- `=` assure l'égalité structurelle (C'est celle qu'on utilise le plus)
- `==` assure l'égalité référentielle (C'est celle qu'on utilise le moins)
- `<>` est l'inverse de `=`
- `!=` est l'inverse de `==`
- `<` et `<=` assure l'infériorité (et/ou l'égalité)
- `>` et `>=` assure la supériorité (et/ou l'égalité)
