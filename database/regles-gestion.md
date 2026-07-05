# Règles de gestion — EcoTech Suivi Chantier

## Objectif

Ce document présente les principales règles de gestion prévues pour l’application EcoTech Suivi Chantier.

Ces règles permettent de préparer la conception de la base de données et le futur développement.

## Règles liées aux utilisateurs

- Un utilisateur possède un seul rôle.
- Un rôle peut être attribué à plusieurs utilisateurs.
- Les rôles prévus sont : administrateur, gérant et employé.
- Un utilisateur devra se connecter pour accéder à l’application.

## Règles liées aux clients

- Un client peut avoir plusieurs chantiers.
- Un chantier est lié à un seul client.
- Un client doit avoir au minimum un nom ou une raison sociale.

## Règles liées aux chantiers

- Un chantier possède un statut.
- Un statut peut être utilisé par plusieurs chantiers.
- Les statuts prévus sont : prévu, en cours, en attente, terminé et annulé.
- Un chantier peut contenir plusieurs documents.
- Un chantier peut contenir plusieurs photos.
- Un chantier peut avoir plusieurs interventions.

## Règles liées aux documents

- Un document est lié à un seul chantier.
- Un document est ajouté par un utilisateur.
- Les documents prévus sont principalement des PDF.
- Les devis et factures sont stockés comme documents joints.

## Règles liées aux photos

- Une photo est liée à un seul chantier.
- Une photo est ajoutée par un utilisateur.
- Les photos permettent de suivre l’avancement du chantier.
- Une description peut être ajoutée à une photo.

## Règles liées aux interventions

- Une intervention est liée à un seul chantier.
- Une intervention est enregistrée par un utilisateur.
- Une intervention contient une date et une description.
- L’historique des interventions permet de suivre l’évolution du chantier.

## Règles liées aux droits

- L’administrateur peut tout gérer.
- Le gérant peut gérer les clients, chantiers, documents, photos et interventions.
- L’employé peut consulter les chantiers et ajouter des photos ou interventions selon ses droits.
- Aucun accès client n’est prévu dans la première version.

## Limites

Ces règles sont adaptées à une première version simple.

Elles pourront être ajustées après les échanges avec le gérant d’EcoTech.