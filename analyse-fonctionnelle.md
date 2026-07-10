# Analyse fonctionnelle — EcoTech Suivi Chantier

## Objectif

Ce document présente les utilisateurs de l’application, leurs rôles et les principales fonctionnalités prévues.

## Acteurs

### Administrateur

L’administrateur peut :

- gérer les utilisateurs ;
- attribuer les rôles ;
- consulter les clients ;
- consulter les chantiers ;
- gérer les documents et les photos ;
- accéder à l’ensemble des fonctionnalités.

### Gérant

Le gérant peut :

- consulter et gérer les clients ;
- créer et modifier les chantiers ;
- consulter les documents ;
- ajouter des documents et des photos ;
- suivre les interventions ;
- générer un rapport de chantier.

### Employé

L’employé peut :

- consulter les chantiers ;
- ajouter des photos ;
- ajouter des interventions ;
- consulter certains documents selon ses droits.

## Principaux cas d’utilisation

| Fonctionnalité | Administrateur | Gérant | Employé |
|---|---:|---:|---:|
| Se connecter | Oui | Oui | Oui |
| Gérer les utilisateurs | Oui | Non | Non |
| Gérer les clients | Oui | Oui | Non |
| Gérer les chantiers | Oui | Oui | Consultation |
| Ajouter une intervention | Oui | Oui | Oui |
| Ajouter une photo | Oui | Oui | Oui |
| Ajouter un document | Oui | Oui | Selon les droits |
| Générer un rapport PDF | Oui | Oui | Non |

## Parcours principal

1. L’utilisateur se connecte.
2. Il accède au tableau de bord.
3. Il consulte la liste des chantiers.
4. Il ouvre la fiche d’un chantier.
5. Il consulte les informations disponibles.
6. Selon son rôle, il peut ajouter une intervention, une photo ou un document.
7. Le gérant peut générer un rapport simple.

## Pages prévues

| Page | Utilité |
|---|---|
| Connexion | Authentifier l’utilisateur |
| Tableau de bord | Afficher une vue générale |
| Utilisateurs | Gérer les comptes et les rôles |
| Clients | Ajouter, modifier et consulter les clients |
| Chantiers | Ajouter, modifier et consulter les chantiers |
| Détail d’un chantier | Consulter les interventions, documents et photos |
| Documents | Ajouter et télécharger des fichiers |
| Rapport | Générer un rapport PDF simple |

## Règles fonctionnelles

- Un utilisateur doit être connecté pour accéder à l’application.
- Les droits dépendent du rôle.
- Un chantier est associé à un client.
- Une intervention est associée à un chantier.
- Une photo ou un document est associé à un chantier.
- Les clients n’ont pas accès à l’application.

## Limites

L’application ne prévoit pas :

- d’espace client ;
- de messagerie interne ;
- de paiement ;
- de devis ou factures générés automatiquement ;
- de suivi GPS ;
- de fonctionnalités mobiles complexes.