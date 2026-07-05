# MCD brouillon — EcoTech Suivi Chantier

## Objectif

Ce document présente un premier modèle conceptuel de données pour l’application EcoTech Suivi Chantier.

Il s’agit d’un brouillon destiné à préparer la future base de données MySQL.

## Entités principales

Les entités principales identifiées sont :

- rôle ;
- utilisateur ;
- client ;
- statut ;
- chantier ;
- document ;
- photo ;
- intervention.

## Diagramme brouillon

```mermaid
erDiagram
    ROLES ||--o{ USERS : possede
    CLIENTS ||--o{ CHANTIERS : concerne
    STATUTS ||--o{ CHANTIERS : definit
    CHANTIERS ||--o{ DOCUMENTS : contient
    CHANTIERS ||--o{ PHOTOS : contient
    CHANTIERS ||--o{ INTERVENTIONS : possede
    USERS ||--o{ INTERVENTIONS : realise
    USERS ||--o{ DOCUMENTS : ajoute
    USERS ||--o{ PHOTOS : ajoute

    ROLES {
        int id
        string nom
    }

    USERS {
        int id
        int role_id
        string nom
        string prenom
        string email
        string mot_de_passe
    }

    CLIENTS {
        int id
        string nom
        string prenom
        string telephone
        string email
        string adresse
    }

    STATUTS {
        int id
        string nom
    }

    CHANTIERS {
        int id
        int client_id
        int statut_id
        string nom
        string adresse
        date date_debut
        date date_fin_prevue
        text description
    }

    DOCUMENTS {
        int id
        int chantier_id
        int user_id
        string nom_fichier
        string type_document
        date date_ajout
    }

    PHOTOS {
        int id
        int chantier_id
        int user_id
        string nom_fichier
        text description
        date date_ajout
    }

    INTERVENTIONS {
        int id
        int chantier_id
        int user_id
        date date_intervention
        text description
    }
```

## Explication simple

Un client peut avoir plusieurs chantiers.

Un chantier possède un statut, par exemple :

- prévu ;
- en cours ;
- en attente ;
- terminé ;
- annulé.

Un chantier peut contenir plusieurs documents, plusieurs photos et plusieurs interventions.

Un utilisateur peut ajouter des documents, des photos ou enregistrer une intervention.

Chaque utilisateur possède un rôle :

- administrateur ;
- gérant ;
- employé.

## Limite du modèle

Ce modèle reste volontairement simple.

Il pourra être amélioré plus tard si nécessaire, mais il est suffisant pour préparer une première version BTS SIO SLAM.