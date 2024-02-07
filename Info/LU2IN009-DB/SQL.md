#db 

SQL ou Structured Query Language est le langage le plus répandu pour effectuer des [[Requête]] sur une [[Bases de données relationnelles]].

Avec SQL, il est possible de définir ou modifier un schéma de base de donnée et envoyer des requêtes.
SQL est basé sur l'[[algèbre relationnel]], le [[Calcul relationnel de n-uplets]] et d'autres concept

## Syntaxe

Les 3 mots clés fondamentaux de SQL sont les suivants:
- `SELECT` On précise le résultat attendu
- `FROM` Où sont les informations recherchées
- `WHERE` Quels sont les conditions à respecter.

### Exemples

Soit la base de donnée suivante:

**Emp**(<u>Eno</u>, Ename, Title, City)
**Project**(<u>Pno</u>, Pname, Budget, City)
**Pay**(<u>Title</u>, Salary)
**Works**(<u>Eno*, Pno*</u>, Resp, Dur)

#### Nom de tous les employés
```sql
SELECT Ename FROM Emp;
```

#### Nom et budgets des projets
```sql
SELECT Pname, Budget FROM Project;
```

### Renommage et Alias
Il est possible de renommer les variables

Soit R une table
```sql
SELECT R v1;
```
`v1` est une ligne de la table `R`

On peut attribuer un alias aux attributs avec le mot clé `AS`

### Récupération totale

Pour récupérer la totalité d'un élément, on utilise `*`
### Elimination des doublons
On utilise la close `DISTINCT`
Soit R une tables
```sql
SELECT DISTINCT R;
```

### Exemples

Soit la base de donnée suivante:

**Emp**(<u>Eno</u>, Ename, Title, City)
**Project**(<u>Pno</u>, Pname, Budget, City)
**Pay**(<u>Title</u>, Salary)
**Works**(<u>Eno*, Pno*</u>, Resp, Dur)
#### Toutes les informations sur les employés
```sql
SELECT * FROM Emp
```

#### Toutes les villes des employés sans répétition
```sql
SELECT DISTINCT City FROM Emp
```
