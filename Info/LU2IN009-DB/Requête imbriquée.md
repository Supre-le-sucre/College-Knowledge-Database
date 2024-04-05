#db
Une requête imbriquée est la combinaison entre une requête et une autre connectée par un opérateur de connection
- `IN`
- `EXISTS`
## Exemples

On considère la base de donnée suivante:

**Emp**(<u>Eno</u>, Ename, Title, City)
**Project**(<u>Pno</u>, Pname, Budget, City)
**Pay**(<u>Title</u>, Salary)
**Works**(<u>Eno*, Pno*</u>, Resp, Dur)

### Noms des employés qui habitent dans une ville sans projet
```sql
SELECT ename
FROM Emp
WHERE NOT EXISTS(
	SELECT * 
	FROM Project
	WHERE p.city = e.city
);
```

Ou bien
```sql
SELECT ename
FROM Emp
WHERE city NOT IN(
	SELECT city 
	FROM Project
);
```

### Noms des projets ayant le plus gros budget
```sql
SELECT pname
FROM Project p1
WHERE NOT EXISTS(
	SELECT *
	FROM Project p2
	WHERE p2.buget > p1.budget
);
```