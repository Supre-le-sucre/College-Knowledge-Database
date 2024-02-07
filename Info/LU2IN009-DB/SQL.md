#db 

SQL ou Structured Query Language est le langage le plus répandu pour effectuer des [[Requête]] sur une [[Bases de données relationnelles]].

Avec SQL, il est possible de définir ou modifier un schéma de base de donnée et envoyer des requêtes.
SQL est basé sur l'[[algèbre relationnel]], le [[Calcul relationnel de n-uplets]] et d'autres concept

## Syntaxe

Les 3 mots clés fondamentaux de SQL sont les suivants:
- `SELECT` On précise le résultat attendu
- `FROM` Où sont les informations recherchées
- `WHERE` Quels sont les conditions à respecter. On y met des prédicats:
	- `AND`
	- `OR`
	- `NOT`

### Exemples basiques

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
SELECT * FROM Emp;
```

#### Toutes les villes des employés sans répétition
```sql
SELECT DISTINCT City FROM Emp;
```

### `IN`, `BETWEEN`, `LIKE`

- `IN` permet de vérifier l'appartenance à un ensemble de valeur
- `BETWEEN` l'appartenance entre deux valeurs
- `LIKE` ayant un motif particulier
	- `_` n'importe quel caractère
	- `%` n'importe quel suite de caractère
### Exemples avec prédicats

Soit la base de donnée suivante:

**Emp**(<u>Eno</u>, Ename, Title, City)
**Project**(<u>Pno</u>, Pname, Budget, City)
**Pay**(<u>Title</u>, Salary)
**Works**(<u>Eno*, Pno*</u>, Resp, Dur)
#### Les employés de titre 'Elect. Eng'
```sql
SELECT * FROM Emp WHERE Title='Elect. Eng';
```

#### Professions qui gagnent plus de 50 000€ par an
```sql
SELECT Title FROM Pay WHERE Salary > 50000;
```

#### Numéros des managers d'un projet pendant plus de 17 mois
```sql
SELECT Resp FROM Works WHERE Dur > 17;
```

#### Noms des projets de Paris, Lyon ou Nantes
```sql
SELECT Pname FROM Project WHERE City='Lyon' OR City='Paris' OR City='Nantes';
```
Ou bien avec `IN`:
```sql
SELECT Pname FROM Project WHERE City IN ('LYON', 'PARIS', 'Nantes');
```

#### Noms des projets ayant un budget compris entre 5M et 10M €

#### Noms des employés commençant par C
```sql
SELECT Ename FROM Emp WHERE Ename LIKE 'C%';
```

#### Noms des employés dont le 2e chiffre du numéro est un 5
```sql
SELECT Ename FROM Emp WHERE Eno LIKE '_5%'
```


### Le tri

On peut trier les résultats avec la close `ORDER BY` en indquant le nom des colonnes, l'expressions des colonnes ou bien encore le numéro de la colonne dans la close `SELECT`
Dans lequel on peut aller dans le sens ascendant (par défaut) `ASC` ou descendant `DESC` après avoir spécifié l'attribut

#### Exemple de tri

Soit la base de donnée suivante:

**Emp**(<u>Eno</u>, Ename, Title, City)
**Project**(<u>Pno</u>, Pname, Budget, City)
**Pay**(<u>Title</u>, Salary)
**Works**(<u>Eno*, Pno*</u>, Resp, Dur)
##### Noms, budgets et villes des projets de budget supérieur à 250 000€ en ordonnant le résultat par ordre décroissant et par nom en ordre croissant.
```sql
SELECT Pname, Budget, City FROM Project WHERE Budget > 250000 ORDER BY Budget DESC, Pname;
```

##### Noms, Budget TTC (TVA 20%) et villes des projets ordonnant le résultat par ordre décroissant du budget TTC

```sql
SELECT Pname, 1.2*Budget, City FROM Project ORDER BY 2 DESC;
```
Ou bien en utilisant un alias avec `AS`:
```sql
SELECT Pname, 1.2*Budget AS TTC, City FROM Project ORDER BY TTC DESC;
```



### Opérations ensemblistes

Il s'agit de faire une opérations d'ensemble entre 2 requêtes.
Le schéma `SELECT` des deux requêtes doivent être les mêmes
- `UNION`
- `INTERSECTION`
- `EXCEPT`

#### Exemples d'opérations
Soit la base de donnée suivante:

**Emp**(<u>Eno</u>, Ename, Title, City)
**Project**(<u>Pno</u>, Pname, Budget, City)
**Pay**(<u>Title</u>, Salary)
**Works**(<u>Eno*, Pno*</u>, Resp, Dur)

##### Noms des villes où habitent des employés ou où sont localisés des projets
```sql
(SELECT City From Emp) UNION (Select Town From Project);
```