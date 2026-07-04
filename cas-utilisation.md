# Cas d’utilisation — EcoTech Suivi Chantier

## Objectif du document

Ce document présente les principaux cas d’utilisation de l’application EcoTech Suivi Chantier.

Il sert à préparer la conception de l’application avant le développement. Les cas d’utilisation permettent d’identifier les actions principales réalisées par les utilisateurs.

## Acteurs concernés

| Acteur | Description |
|---|---|
| Administrateur | Gère les utilisateurs, les rôles et l’ensemble des données |
| Gérant | Suit les clients, les chantiers, les documents, les photos et les rapports |
| Employé | Ajoute des photos, des documents et des interventions selon ses droits |

Dans la première version, aucun accès client n’est prévu.

---

# CU01 — Créer un client

## Objectif

Permettre à un administrateur ou à un gérant d’enregistrer un nouveau client dans l’application.

## Acteur principal

- Administrateur
- Gérant

## Préconditions

- L’utilisateur est connecté.
- L’utilisateur possède les droits nécessaires.
- Le client n’existe pas déjà dans l’application.

## Scénario nominal

1. L’utilisateur accède à la page de gestion des clients.
2. Il clique sur le bouton “Ajouter un client”.
3. Il saisit les informations du client.
4. Il valide le formulaire.
5. Le système vérifie les champs obligatoires.
6. Le client est enregistré en base de données.
7. Le client apparaît dans la liste des clients.

## Données nécessaires

- Nom du client
- Prénom ou raison sociale
- Téléphone
- Email
- Adresse
- Remarques éventuelles

## Exceptions possibles

| Situation | Réaction du système |
|---|---|
| Champ obligatoire vide | Afficher un message d’erreur |
| Email invalide | Refuser l’enregistrement |
| Client déjà existant | Prévenir l’utilisateur |

## Résultat attendu

Le client est enregistré et peut être associé à un chantier.

---

# CU02 — Créer un chantier

## Objectif

Permettre à un administrateur ou à un gérant de créer un nouveau chantier.

## Acteur principal

- Administrateur
- Gérant

## Préconditions

- L’utilisateur est connecté.
- Un client existe déjà dans l’application.
- L’utilisateur possède les droits nécessaires.

## Scénario nominal

1. L’utilisateur accède à la page des chantiers.
2. Il clique sur “Créer un chantier”.
3. Il sélectionne le client concerné.
4. Il renseigne les informations du chantier.
5. Il choisit un statut initial.
6. Il valide le formulaire.
7. Le chantier est enregistré.
8. Le chantier apparaît dans la liste des chantiers.

## Données nécessaires

- Nom du chantier
- Client associé
- Adresse du chantier
- Date de début prévue
- Date de fin prévue si connue
- Statut du chantier
- Description des travaux

## Statuts possibles

- Prévu
- En cours
- En attente
- Terminé
- Annulé

## Exceptions possibles

| Situation | Réaction du système |
|---|---|
| Client non sélectionné | Afficher un message d’erreur |
| Nom du chantier vide | Refuser l’enregistrement |
| Date incorrecte | Afficher une erreur de saisie |

## Résultat attendu

Le chantier est créé et peut recevoir des documents, des photos et des interventions.

---

# CU03 — Ajouter un document PDF

## Objectif

Permettre à un utilisateur autorisé d’ajouter un document PDF à un chantier.

## Acteur principal

- Administrateur
- Gérant
- Employé selon les droits

## Préconditions

- L’utilisateur est connecté.
- Le chantier existe.
- L’utilisateur possède les droits nécessaires.
- Le fichier est au format PDF.

## Scénario nominal

1. L’utilisateur ouvre la fiche d’un chantier.
2. Il clique sur “Ajouter un document”.
3. Il sélectionne un fichier PDF.
4. Il indique le type de document.
5. Il valide l’envoi.
6. Le système vérifie le format du fichier.
7. Le document est enregistré et associé au chantier.
8. Le document apparaît dans la liste des documents du chantier.

## Types de documents possibles

- Devis
- Facture
- Plan
- Document administratif
- Autre document

## Exceptions possibles

| Situation | Réaction du système |
|---|---|
| Format non PDF | Refuser le fichier |
| Fichier trop lourd | Afficher un message d’erreur |
| Chantier inexistant | Refuser l’ajout |
| Droits insuffisants | Bloquer l’action |

## Résultat attendu

Le document PDF est disponible dans la fiche du chantier.

---

# CU04 — Ajouter une photo de chantier

## Objectif

Permettre à un utilisateur autorisé d’ajouter une photo liée à un chantier.

## Acteur principal

- Gérant
- Employé
- Administrateur

## Préconditions

- L’utilisateur est connecté.
- Le chantier existe.
- La photo respecte les formats autorisés.
- L’utilisateur possède les droits nécessaires.

## Scénario nominal

1. L’utilisateur ouvre la fiche d’un chantier.
2. Il clique sur “Ajouter une photo”.
3. Il sélectionne une photo.
4. Il ajoute une description si nécessaire.
5. Il valide l’envoi.
6. Le système vérifie le format du fichier.
7. La photo est enregistrée.
8. La photo apparaît dans la galerie du chantier.

## Formats autorisés prévus

- JPG
- JPEG
- PNG

## Données nécessaires

- Fichier image
- Date d’ajout
- Description facultative
- Utilisateur ayant ajouté la photo

## Exceptions possibles

| Situation | Réaction du système |
|---|---|
| Format non autorisé | Refuser le fichier |
| Fichier trop lourd | Afficher une erreur |
| Droits insuffisants | Bloquer l’ajout |

## Résultat attendu

La photo est associée au chantier et permet de suivre l’avancement des travaux.

---

# CU05 — Enregistrer une intervention

## Objectif

Permettre à un utilisateur autorisé d’ajouter une intervention dans l’historique d’un chantier.

## Acteur principal

- Gérant
- Employé
- Administrateur

## Préconditions

- L’utilisateur est connecté.
- Le chantier existe.
- L’utilisateur possède les droits nécessaires.

## Scénario nominal

1. L’utilisateur ouvre la fiche d’un chantier.
2. Il clique sur “Ajouter une intervention”.
3. Il saisit la date de l’intervention.
4. Il décrit l’action réalisée.
5. Il indique éventuellement le statut du chantier.
6. Il valide le formulaire.
7. L’intervention est enregistrée en base de données.
8. L’intervention apparaît dans l’historique du chantier.

## Données nécessaires

- Chantier concerné
- Date de l’intervention
- Description
- Utilisateur concerné
- Statut éventuel
- Remarques éventuelles

## Exceptions possibles

| Situation | Réaction du système |
|---|---|
| Description vide | Refuser l’enregistrement |
| Date invalide | Afficher une erreur |
| Droits insuffisants | Bloquer l’action |

## Résultat attendu

L’historique du chantier est mis à jour.

---

# CU06 — Générer un rapport PDF de chantier

## Objectif

Permettre à un administrateur ou à un gérant de générer un rapport PDF récapitulatif d’un chantier.

## Acteur principal

- Administrateur
- Gérant

## Préconditions

- L’utilisateur est connecté.
- Le chantier existe.
- Le chantier contient des informations exploitables.
- L’utilisateur possède les droits nécessaires.

## Scénario nominal

1. L’utilisateur ouvre la fiche du chantier.
2. Il clique sur “Générer le rapport PDF”.
3. Le système récupère les informations du chantier.
4. Le système récupère les interventions.
5. Le système ajoute éventuellement les documents et photos liés.
6. Le PDF est généré.
7. L’utilisateur peut télécharger le rapport.

## Informations prévues dans le rapport

- Nom du chantier
- Client concerné
- Adresse du chantier
- Statut
- Dates importantes
- Description des travaux
- Historique des interventions
- Liste des documents
- Liste ou aperçu des photos

## Exceptions possibles

| Situation | Réaction du système |
|---|---|
| Chantier inexistant | Afficher une erreur |
| Aucune donnée disponible | Générer un rapport minimal |
| Droits insuffisants | Bloquer l’action |

## Résultat attendu

Un rapport PDF est généré et peut être utilisé comme preuve de suivi de chantier.

---

# Synthèse des cas d’utilisation

| Code | Cas d’utilisation | Acteur principal | Priorité |
|---|---|---|---|
| CU01 | Créer un client | Admin / Gérant | Haute |
| CU02 | Créer un chantier | Admin / Gérant | Haute |
| CU03 | Ajouter un document PDF | Admin / Gérant / Employé | Haute |
| CU04 | Ajouter une photo | Admin / Gérant / Employé | Haute |
| CU05 | Enregistrer une intervention | Admin / Gérant / Employé | Haute |
| CU06 | Générer un rapport PDF | Admin / Gérant | Moyenne |

## Lien avec la suite du projet

Ces cas d’utilisation serviront à préparer :

- les maquettes ;
- le modèle de données ;
- les tables MySQL ;
- les pages PHP ;
- les tests fonctionnels ;
- la démonstration devant le jury.