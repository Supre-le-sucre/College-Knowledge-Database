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