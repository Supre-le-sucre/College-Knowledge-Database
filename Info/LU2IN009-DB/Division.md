## Définition
Une division est une [[Requête]] spécifique qui demande à diviser l'ensemble global en plusieurs sous ensemble de propriété unique.

On exprime cette requête en [[Calcul relationnel de n-uplets]] avec un $\neg \exists ( \neg \exists)$ (autrement dit un $\forall (\exists)$)

*Remarque:* Une division est repérable car la requête cherche une totalité.

## Exemple
Considérant la base de donnée suivante:

**Etudiants**(<u>matricule</u>, nom, prenom, adresse, collaborateur\*)
**Inscriptions**(<u>matricule*, code*</u>)
**Modules**(<u>code</u>, intitule, niveau, salle*)
**Salles**(<u>numero</u>, capacite, précédent*, suivante*)

### Quels étudiants sont inscrits dans tous les modules ?

- On itère sur étudiant
- On parcourt tous les modules ($\forall$)
- Pour lesquels une inscription au matricule de l'étudiant et le module ($\exists$)

$$\set{e.matricule | Etudiants(e) \wedge \forall m(Module(m) \wedge \exists i(Inscription(i) \wedge e.matricule = i.matricule \wedge i.code = m.code))}$$
On l'exprime avec un il existe en appliquant la double négation:

$$\set{e.matricule | Etudiants(e) \wedge \neg\exists m(Module(m) \wedge \neg \exists i(Inscription(i) \wedge e.matricule = i.matricule \wedge i.code = m.code))}$$

### Quels modules de L3 ont une inscription pour tous les étudiants ?

- On itère sur les modules
- On cherche tous les étudiants ($\forall)$
- Pour lesquels une inscription au matricule de l'étudiant et du module ($\exists$)
$$\set{m.code | Module(m) \wedge \forall e(Etudiant(e) \wedge \exists i(Inscription(i) \wedge i.matricule = e.matricule \wedge i.code = m.code))}$$
On l'exprime avec un il existe en appliquant la double négation:
$$\set{m.code | Module(m) \wedge \neg \exists e(Etudiant(e) \wedge \neg\exists i(Inscription(i) \wedge i.matricule = e.matricule \wedge i.code = m.code))}$$