# Parcours utilisateur — EcoTech Suivi Chantier

## Objectif

Ce document décrit les principaux parcours utilisateurs prévus dans l’application EcoTech Suivi Chantier.

Il permet de relier les maquettes aux besoins réels de l’entreprise.

---

## 1. Parcours — Gérant : consulter un chantier

### Acteur

Gérant

### Objectif

Consulter rapidement les informations d’un chantier.

### Étapes

1. Le gérant se connecte.
2. Il arrive sur la liste des chantiers.
3. Il recherche le chantier concerné.
4. Il ouvre la fiche chantier.
5. Il consulte les informations principales.
6. Il consulte les documents, photos et interventions.
7. Il peut générer un rapport PDF si nécessaire.

### Résultat attendu

Le gérant retrouve rapidement les informations du chantier sans chercher dans plusieurs outils.

---

## 2. Parcours — Employé : ajouter une photo

### Acteur

Employé

### Objectif

Ajouter une photo de chantier pour suivre l’avancement.

### Étapes

1. L’employé se connecte.
2. Il ouvre la liste des chantiers.
3. Il sélectionne le chantier concerné.
4. Il ouvre l’onglet documents/photos.
5. Il clique sur “Ajouter une photo”.
6. Il choisit une photo.
7. Il ajoute une description.
8. Il valide l’ajout.

### Résultat attendu

La photo est liée au bon chantier et peut être consultée par l’équipe.

---

## 3. Parcours — Gérant : enregistrer une intervention

### Acteur

Gérant

### Objectif

Ajouter une intervention dans l’historique du chantier.

### Étapes

1. Le gérant se connecte.
2. Il ouvre la fiche chantier.
3. Il va dans l’onglet interventions.
4. Il clique sur “Ajouter une intervention”.
5. Il saisit la date.
6. Il décrit l’action réalisée.
7. Il valide le formulaire.

### Résultat attendu

L’intervention apparaît dans l’historique du chantier.

---

## 4. Parcours — Administrateur : gérer les utilisateurs

### Acteur

Administrateur

### Objectif

Créer ou modifier les comptes utilisateurs.

### Étapes

1. L’administrateur se connecte.
2. Il accède à l’administration des utilisateurs.
3. Il consulte la liste des comptes.
4. Il ajoute ou modifie un utilisateur.
5. Il attribue un rôle.
6. Il valide.

### Résultat attendu

Les accès utilisateurs sont organisés selon les rôles prévus.

---

## 5. Parcours — Gérant : générer un rapport PDF

### Acteur

Gérant

### Objectif

Créer un rapport PDF à partir des informations d’un chantier.

### Étapes

1. Le gérant se connecte.
2. Il ouvre la fiche chantier.
3. Il va dans l’onglet rapport PDF.
4. Il choisit les informations à inclure.
5. Il clique sur “Générer le rapport PDF”.

### Résultat attendu

Un rapport PDF est produit à partir des informations centralisées du chantier.

---

## Synthèse des parcours

| N° | Acteur | Action principale | Écran lié |
|---:|---|---|---|
| 1 | Gérant | Consulter un chantier | Fiche chantier |
| 2 | Employé | Ajouter une photo | Documents et photos |
| 3 | Gérant | Ajouter une intervention | Historique des interventions |
| 4 | Administrateur | Gérer les utilisateurs | Administration des utilisateurs |
| 5 | Gérant | Générer un rapport PDF | Rapport PDF |

## Justification

Ces parcours couvrent les besoins principaux d’EcoTech :

- retrouver les informations ;
- ajouter des preuves photos ;
- suivre les interventions ;
- gérer les accès ;
- produire un rapport.

Ils permettent de préparer le développement sans partir directement dans le code.