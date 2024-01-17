#db
Dans la majorité des [[Système de gestion de bases de données]], il est nécessaire de développer différents niveaux d'abstraction pour s'adapter aux données stockées.

Il existe 3 différents niveaux d'abstractions nécessaires à la conception d'une base de données.

- Niveau des vues (accessible à l'utilisateur)
		C'est ce qui gère les données visible -> [[Schéma]] externe

- Niveau logique (concepteur et programmeur)
		Quelles données vont être stockée -> [[Schéma]] logique

- Niveau physique (concepteur et administrateur)
		Comment les données sont stockée -> [[Schéma]] physique
		Ce niveau d'abstraction est aussi appelé _database engine_

La notion d'indépendances entre ces niveaux est fondamental pour la sécurité des données et leur accessibilité

- L'indépendance physique des données
		Le [[Schéma]] physique n'affecte pas le [[Schéma]] logique

- L'indépendance logique
		Le [[Schéma]] logique n'affecte pas le [[Schéma]] externe