#db
Une autojointure est une [[Requête]] qui demande à lier une table avec elle même.
Elle se différencie donc d'une [[Jointure]] qui lieu deux tables différents entre elles.

## Exemple

Considérant la base de donnée suivante:

**Etudiants**(<u>matricule</u>, nom, prenom, adresse, collaborateur\*)
**Inscriptions**(<u>matricule*, code*</u>)
**Modules**(<u>code</u>, intitule, niveau, salle*)
**Salles**(<u>numero</u>, capacite, précédent*, suivante*)

### Quels sont les étudiants inscrits dans au moins deux modules ?

- On cherche ici dans une inscription.

$$\set{i_1.matricule | Inscriptions(i_1) \wedge \exists i_2(Inscription(i_2) \wedge i_2.matricule = i_1.matricule \wedge i_2.code \not= i_1.code) }$$

Les jointure sont les conditions d'égalité.

### Quels sont les étudiants inscrits à au moins  deux modules de niveau L3 ? (Retourner son prénom)


- Pour savoir s'il sont de niveau L3, il faut regarder dans modules

$$\set{e.prenom | Etudiants(e) \wedge \exists i_1, i_2 (Inscriptions(i_1) \wedge Inscriptions(i_2), i_1.matricule = e.matricule \wegde i_2.matricule = e.matricule \wedge i_1.code \not= i_2.code \wedge \exists m_1, m_2 (Modules(m_1) \wedge Modules(m_2) \wegde m_1.code = i_1.code \wedge m_2.code =i_2.code \wegde m_1.niveau =\text{'L3'} \wegde m_2.niveau = \text{'L3'}))}$$

