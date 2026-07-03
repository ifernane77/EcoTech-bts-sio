
---

## Fichier `acteurs-et-roles.md`

```md
# Acteurs et rôles — EcoTech Suivi Chantier

## Objectif

Ce document identifie les acteurs concernés par le projet EcoTech Suivi Chantier et leurs rôles dans l’application.

## Acteurs de l’entreprise

| Acteur | Rôle dans l’entreprise | Besoin principal |
|---|---|---|
| Gérant | Suit l’activité, échange avec les clients, supervise les chantiers | Avoir une vue globale sur les chantiers |
| Employé administratif | Gère les documents, devis, factures et parfois les échanges clients | Retrouver rapidement les documents |
| Employé terrain | Suit les chantiers et prend des photos | Ajouter photos et interventions |
| Prestataire terrain | Intervient ponctuellement sur les chantiers | Transmettre des informations à l’équipe |
| Client | Demande des travaux et reçoit des documents | Recevoir les informations via l’équipe EcoTech |

## Rôles prévus dans l’application

| Rôle applicatif | Droits prévus |
|---|---|
| Administrateur | Gérer les utilisateurs, les rôles, les clients, les chantiers et les paramètres |
| Gérant | Gérer les clients, les chantiers, les documents, les photos, les interventions et les rapports |
| Employé | Consulter les chantiers, ajouter des photos, ajouter des interventions et déposer certains documents |

## Rôles non prévus

Dans la première version, il n’est pas prévu de créer un accès client.

Le client ne se connectera pas à l’application. Les informations lui seront transmises par l’équipe EcoTech.

## Justification

Le choix de limiter les rôles à administrateur, gérant et employé permet de garder un projet simple et réaliste pour le BTS SIO SLAM.

Cela permet aussi de mieux contrôler les accès et d’éviter de rendre le projet trop complexe.