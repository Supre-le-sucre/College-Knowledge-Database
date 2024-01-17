#db
Un identifiant est un sous-ensemble d'[[Attributs]] d'une [[Classe d'entités]]

Notamment, elle permet de distinguer une entité de la même classe, l'identifiant est donc unique, une [[Entités]] d'une [[Classe d'entités]] a un identifiant unique.

Chaque [[Classe d'entités]] doit aussi avoir un identifiant unique

Un identifiant peut être de deux types différents:

- Naturel, construit à partir des [[Attributs]] de la classe
- Artificiel, rajouté aux [[Attributs]] de la classe, lorsque les [[Attributs]] de la classe ne permettent pas de définir un identifiant

Par exemple: un matricule, le numéro d'une salle et son emplacement, un prénom (si chaque prénom est différent)

## Identifiant d'une association

Une [[Association]] est identifiée au moyen des identifiants des entités qu'elle met en relation. 

Puisqu'on ne peut pas associer des entités avec la même association sémantique, un identifiant classique d'une association est simplement la concaténation des deux identifiants des [[Entités]] associée.

Si une [[Association]] possède un [[Attributs]], alors il est nécessaire de les différencier. On peut dans ce cas, intégrer cette attribut dans l'identifiant de l'[[Association]]