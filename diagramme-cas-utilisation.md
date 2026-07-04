# Diagramme des cas d’utilisation — EcoTech Suivi Chantier

## Objectif

Ce document présente un schéma simplifié des cas d’utilisation principaux de l’application EcoTech Suivi Chantier.

Le schéma est volontairement simple afin de rester adapté au niveau BTS SIO SLAM.

## Diagramme simplifié

```mermaid
flowchart LR
    Admin[Administrateur]
    Gerant[Gérant]
    Employe[Employé]

    UC1[Créer un client]
    UC2[Créer un chantier]
    UC3[Ajouter un document PDF]
    UC4[Ajouter une photo]
    UC5[Enregistrer une intervention]
    UC6[Générer un rapport PDF]
    UC7[Gérer les utilisateurs]
    UC8[Consulter un chantier]

    Admin --> UC1
    Admin --> UC2
    Admin --> UC3
    Admin --> UC4
    Admin --> UC5
    Admin --> UC6
    Admin --> UC7
    Admin --> UC8

    Gerant --> UC1
    Gerant --> UC2
    Gerant --> UC3
    Gerant --> UC4
    Gerant --> UC5
    Gerant --> UC6
    Gerant --> UC8

    Employe --> UC3
    Employe --> UC4
    Employe --> UC5
    Employe --> UC8
```

## Lecture du diagramme

L’administrateur possède tous les droits.  
Le gérant peut gérer les clients, les chantiers, les documents, les photos, les interventions et les rapports.  
L’employé dispose de droits plus limités : il peut consulter les chantiers, ajouter des photos, ajouter des interventions et déposer certains documents.

## Justification des rôles

Le projet doit rester simple et réaliste. C’est pour cela que seuls trois rôles sont prévus :

- administrateur ;
- gérant ;
- employé.

Aucun accès client n’est prévu dans la première version.

## Lien avec E6 SLAM

Ce diagramme prépare la conception de la solution applicative. Il permet d’identifier les fonctionnalités principales avant de créer les maquettes, la base de données et les pages PHP.