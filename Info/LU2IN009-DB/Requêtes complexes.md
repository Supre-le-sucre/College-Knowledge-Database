En [[SQL]], il est aussi possible de gérer des requêtes plus complexes, sur plusieurs tables en simultanée et ainsi utiliser leur produit cartésien.
La syntaxe est la même, mais avec une énumération de table:

```sql
SELECT Atts
FROM Table1, Table2, ...
WHERE Condition;
```

Il est possible d'avoir la même table concaténé avec elle même. On parle donc d'[[Autojointure]].
En connectant des tables différentes entre elles on utilise alors le principe de [[Jointure]]

## Exemples

On considère la base de donnée suivante:

**Emp**(<u>Eno</u>, Ename, Title, City)
**Project**(<u>Pno</u>, Pname, Budget, City)
**Pay**(<u>Title</u>, Salary)
**Works**(<u>Eno*, Pno*</u>, Resp, Dur)

### Noms et salaires des employés
```sql
SELECT ename, salary
FROM Emp, Pay
WHERE Emp.title = Pay.title;
```

### Noms et titres des employés qui travaillent dans un projet pendant plus de 17 mois ?
```sql
SELECT ename, title
FROM Emp, Works
WHERE Emp.eno = Works.eno AND Works.dur >= 17;
```

**Remarque**: Il est possible d'utiliser des tables qui ne sont pas mentionnées dans le `SELECT`

### Numéros et noms des projets dans lesquels a travaillé l'employé 10
```sql
SELECT Projet.pno, pname
FROM Projet, Works
WHERE Works.eno = 10 AND Projet.pno = Works.pno;
```

**Remarque**: Lorsque une ambiguïté est levée sur le nom d'un attribut, il faut préciser sa table source dans le `SELECT`

### Noms et titres des employés qui travaillent dans un projet à Paris
```sql
SELECT ename, title
FROM Emp, Works, Project
WHERE Projet.city = 'Paris' AND Emp.eno = Works.eno AND Works.pno = Projet.pno; 
```

### Noms des employés originaire de la même ville
```sql
SELECT E1.ename, E2.ename
FROM Emp E1, Emp E2
WHERE E1.City = E2.City AND E1.ename > E2.ename;
```

**Remarque** On utilise ici l'ordre alphabétique pour éviter les redondances que l'on n'aurait pas pu supprimer avec `DISTINCT`
