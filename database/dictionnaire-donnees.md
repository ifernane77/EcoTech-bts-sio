
---

## `database/dictionnaire-donnees.md`

```md
# Dictionnaire de données — EcoTech Suivi Chantier

## Objectif

Ce document décrit les données principales prévues dans l’application EcoTech Suivi Chantier.

Il permet de mieux comprendre le rôle de chaque table avant la création de la base de données.

## Table roles

| Champ | Type prévu | Description |
|---|---|---|
| id | INT | Identifiant du rôle |
| nom | VARCHAR | Nom du rôle |

Exemples :

- administrateur ;
- gérant ;
- employé.

## Table users

| Champ | Type prévu | Description |
|---|---|---|
| id | INT | Identifiant de l’utilisateur |
| role_id | INT | Rôle associé |
| nom | VARCHAR | Nom de l’utilisateur |
| prenom | VARCHAR | Prénom de l’utilisateur |
| email | VARCHAR | Adresse email |
| mot_de_passe | VARCHAR | Mot de passe hashé plus tard |

## Table clients

| Champ | Type prévu | Description |
|---|---|---|
| id | INT | Identifiant du client |
| nom | VARCHAR | Nom du client |
| prenom | VARCHAR | Prénom ou contact |
| telephone | VARCHAR | Numéro de téléphone |
| email | VARCHAR | Adresse email |
| adresse | VARCHAR | Adresse du client |

## Table statuts

| Champ | Type prévu | Description |
|---|---|---|
| id | INT | Identifiant du statut |
| nom | VARCHAR | Nom du statut |

Exemples :

- prévu ;
- en cours ;
- en attente ;
- terminé ;
- annulé.

## Table chantiers

| Champ | Type prévu | Description |
|---|---|---|
| id | INT | Identifiant du chantier |
| client_id | INT | Client lié au chantier |
| statut_id | INT | Statut du chantier |
| nom | VARCHAR | Nom du chantier |
| adresse | VARCHAR | Adresse du chantier |
| date_debut | DATE | Date de début |
| date_fin_prevue | DATE | Date de fin prévue |
| description | TEXT | Description des travaux |

## Table documents

| Champ | Type prévu | Description |
|---|---|---|
| id | INT | Identifiant du document |
| chantier_id | INT | Chantier associé |
| user_id | INT | Utilisateur ayant ajouté le document |
| nom_fichier | VARCHAR | Nom du fichier stocké |
| type_document | VARCHAR | Type : devis, facture, plan, autre |
| date_ajout | DATETIME | Date d’ajout |

## Table photos

| Champ | Type prévu | Description |
|---|---|---|
| id | INT | Identifiant de la photo |
| chantier_id | INT | Chantier associé |
| user_id | INT | Utilisateur ayant ajouté la photo |
| nom_fichier | VARCHAR | Nom du fichier image |
| description | TEXT | Description facultative |
| date_ajout | DATETIME | Date d’ajout |

## Table interventions

| Champ | Type prévu | Description |
|---|---|---|
| id | INT | Identifiant de l’intervention |
| chantier_id | INT | Chantier associé |
| user_id | INT | Utilisateur ayant enregistré l’intervention |
| date_intervention | DATE | Date de l’intervention |
| description | TEXT | Description de l’intervention |