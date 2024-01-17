Afin de concevoir un [[Système de gestion de bases de données]] il est nécessaire d'en discuter sa structure

Temporellement, la structuration se fait en plusieurs étapes

- Analyse des besoins
		A travers de discussions informelles, qui découle d'une documentation technique, pour savoir comment satisfaire les besoins.
		Ici, on identifie les objets du monde réel et on y associe des liens entre eux

- Modélisation des données
		On traduit ensuite les besoins en des concepts de base, en établissant des entités et des liens entre elles [[Modèle Entité-Association]]

- Implantation des données
		On s'occupe aussi de la partie informatique, en communiquant avec la machine. Notamment avec le  [[Langages pour les DB]] [[SQL]] (Structured Query Language), le standard pour les [[Bases de données relationnelles]]
	On travaille alors sur le [[Modèle relationnel]]

## Etude de cas: DB dans une université

### Les besoins
- Gérer les inscriptions des étudiants aux modules
- Gérer l'affectation des tuteurs et étudiants
- Gérer les plannings des salles

### Les objets à modéliser
- Les étudiants
- Les modules
- Les tuteurs
- Les salles

### Les liens entre les objets
- Les étudiants s'inscrivent à un ou plusieurs modules pour une année universitaire
- Les cours d'un module a lieu dans une salle donnée, débute et se termine à une heure connue