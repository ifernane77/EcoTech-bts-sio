# Architecture et flux — EcoTech Suivi Chantier

## Objectif du document

Ce document présente les acteurs, les outils utilisés actuellement et les flux d’informations autour du suivi des chantiers chez EcoTech.

L’objectif est de mieux comprendre l’organisation actuelle afin de concevoir une application web simple et adaptée au besoin de l’entreprise.

## Contexte actuel

EcoTech utilise actuellement plusieurs outils pour gérer les informations liées aux chantiers :

- Google Drive ;
- mails professionnels ;
- WhatsApp ;
- ordinateurs personnels ;
- téléphones professionnels.

Les informations ne sont pas forcément perdues, mais elles sont dispersées entre plusieurs supports. Cela peut entraîner une perte de temps lorsqu’un membre de l’équipe doit retrouver un document, une photo, un devis ou une facture.

## Acteurs principaux

Les acteurs identifiés sont :

- les 2 gérants associés ;
- l’employé administratif ;
- l’employé chargé du suivi des chantiers ;
- les prestataires terrain ;
- les clients ;
- l’administrateur de l’application.

## Flux actuels

| Flux | Départ | Arrivée | Support actuel | Problème possible |
|---|---|---|---|---|
| Demande client | Client | Gérant ou employé | Téléphone, mail, WhatsApp | Information difficile à retrouver |
| Devis | Gérant ou employé administratif | Client | Mail, PDF, Drive | Fichiers dispersés |
| Photos chantier | Employé terrain | Gérant / équipe | Téléphone, WhatsApp, Drive | Photos non centralisées |
| Factures | Employé administratif | Client / entreprise | PDF, mail, Drive | Classement variable |
| Suivi chantier | Employé terrain | Gérant | Oral, WhatsApp, photos | Historique incomplet |
| Documents techniques | Gérant / employé | Équipe | PC, Drive, mail | Recherche longue |

## Flux prévus avec l’application

Avec l’application EcoTech Suivi Chantier, les informations importantes seront centralisées.

| Flux | Départ | Arrivée | Support prévu |
|---|---|---|---|
| Création client | Admin / gérant | Application | Base de données |
| Création chantier | Admin / gérant | Application | Base de données |
| Ajout document PDF | Admin / gérant / employé | Chantier concerné | Application |
| Ajout photo | Employé / gérant | Chantier concerné | Application |
| Ajout intervention | Employé / gérant | Historique chantier | Application |
| Génération rapport | Gérant / admin | PDF chantier | Application |

## Schéma simplifié des flux

```mermaid
flowchart TD
    Client[Client] -->|Demande / informations| Gerant[Gérant]
    Gerant -->|Création client et chantier| App[Application EcoTech Suivi Chantier]
    EmployeAdmin[Employé administratif] -->|Documents, devis, factures PDF| App
    EmployeTerrain[Employé terrain] -->|Photos et interventions| App
    Prestataires[Prestataires terrain] -->|Informations transmises à l'équipe| EmployeTerrain
    App -->|Centralisation| BDD[(Base de données MySQL)]
    App -->|Documents et photos| Stockage[(Stockage fichiers)]
    Gerant -->|Consultation / rapport| Rapport[Rapport PDF chantier]