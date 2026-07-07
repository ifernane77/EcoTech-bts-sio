# Maquettes fonctionnelles — EcoTech Suivi Chantier

## Objectif

Ce document présente les maquettes fonctionnelles prévues pour l’application EcoTech Suivi Chantier.

Les maquettes sont volontairement simples. Elles servent à préparer le développement des pages principales de l’application.

L’objectif est de montrer les écrans attendus avant de commencer le code.

---

## 1. Maquette — Page de connexion

### Objectif de l’écran

Permettre à un utilisateur EcoTech de se connecter à l’application.

### Utilisateurs concernés

- Administrateur
- Gérant
- Employé

### Éléments affichés

```text
+--------------------------------------------------+
|              EcoTech Suivi Chantier              |
+--------------------------------------------------+

              Connexion à l'application

        Email :
        [____________________________]

        Mot de passe :
        [____________________________]

        [ Se connecter ]

----------------------------------------------------

Message possible :
Identifiants incorrects.
```

### Données affichées

- titre de l’application ;
- champ email ;
- champ mot de passe ;
- bouton de connexion ;
- message d’erreur si les identifiants sont incorrects.

### Règles prévues

- L’utilisateur doit saisir un email et un mot de passe.
- Si les identifiants sont incorrects, un message d’erreur s’affiche.
- Après connexion, l’utilisateur est redirigé selon son rôle.

---

## 2. Maquette — Liste des chantiers

### Objectif de l’écran

Afficher les chantiers enregistrés dans l’application.

### Utilisateurs concernés

- Administrateur
- Gérant
- Employé

### Éléments affichés

```text
+--------------------------------------------------+
| Menu : Tableau de bord | Chantiers | Clients      |
+--------------------------------------------------+

Liste des chantiers

[ + Ajouter un chantier ]

Recherche : [__________________]

+----+-------------------+-------------+------------+
| ID | Nom du chantier   | Client      | Statut     |
+----+-------------------+-------------+------------+
| 1  | Maison Durand     | M. Durand   | En cours   |
| 2  | Villa Saint-Pierre| Mme Payet   | Prévu      |
| 3  | Local entreprise  | SARL Nova   | Terminé    |
+----+-------------------+-------------+------------+

Actions :
[ Voir ] [ Modifier ]
```

### Données affichées

- identifiant du chantier ;
- nom du chantier ;
- client associé ;
- statut du chantier ;
- bouton de consultation ;
- bouton de modification selon le rôle.

### Règles prévues

- Un gérant ou un administrateur peut ajouter un chantier.
- Un employé peut consulter les chantiers.
- La recherche permettra de retrouver un chantier plus rapidement.
- Les actions affichées pourront dépendre du rôle utilisateur.

---

## 3. Maquette — Fiche chantier

### Objectif de l’écran

Afficher les informations principales d’un chantier.

### Utilisateurs concernés

- Administrateur
- Gérant
- Employé

### Éléments affichés

```text
+--------------------------------------------------+
| Fiche chantier : Maison Durand                   |
+--------------------------------------------------+

Client : M. Durand
Adresse : 12 rue Exemple, Saint-Pierre
Statut : En cours
Date de début : 20/08/2026
Date de fin prévue : 15/09/2026

Description :
Rénovation d'une partie de la maison et travaux de maçonnerie.

Onglets :
[ Informations ] [ Documents / Photos ] [ Interventions ] [ Rapport PDF ]

Actions :
[ Modifier le chantier ] [ Ajouter une intervention ]
```

### Données affichées

- nom du chantier ;
- client associé ;
- adresse du chantier ;
- statut ;
- date de début ;
- date de fin prévue ;
- description ;
- accès aux documents et photos ;
- accès à l’historique des interventions ;
- accès au rapport PDF.

### Règles prévues

- Un chantier doit être associé à un client.
- Le statut doit être visible rapidement.
- Les actions disponibles dépendent du rôle utilisateur.
- La fiche chantier centralise les informations importantes.

---

## 4. Maquette — Documents et photos

### Objectif de l’écran

Centraliser les documents PDF et les photos liés à un chantier.

### Utilisateurs concernés

- Administrateur
- Gérant
- Employé selon les droits

### Éléments affichés

```text
+--------------------------------------------------+
| Chantier : Maison Durand                         |
| Onglet : Documents / Photos                      |
+--------------------------------------------------+

Documents PDF

[ + Ajouter un document ]

+----------------------+-------------+-------------+
| Nom du document      | Type        | Date ajout  |
+----------------------+-------------+-------------+
| devis-durand.pdf     | Devis       | 20/08/2026  |
| facture-acompte.pdf  | Facture     | 25/08/2026  |
+----------------------+-------------+-------------+

Photos de chantier

[ + Ajouter une photo ]

+----------------------+---------------------------+
| Photo                | Description               |
+----------------------+---------------------------+
| photo-01.jpg         | Début des travaux         |
| photo-02.jpg         | Avancement maçonnerie     |
+----------------------+---------------------------+
```

### Données affichées

- nom du document ;
- type du document ;
- date d’ajout ;
- nom de la photo ;
- description de la photo ;
- chantier associé.

### Règles prévues

- Les documents seront principalement au format PDF.
- Les photos seront au format JPG, JPEG ou PNG.
- Chaque fichier sera lié à un chantier.
- Les fichiers doivent être bien nommés pour être retrouvés facilement.

---

## 5. Maquette — Historique des interventions

### Objectif de l’écran

Afficher les interventions réalisées sur un chantier.

### Utilisateurs concernés

- Administrateur
- Gérant
- Employé

### Éléments affichés

```text
+--------------------------------------------------+
| Chantier : Maison Durand                         |
| Onglet : Interventions                           |
+--------------------------------------------------+

[ + Ajouter une intervention ]

+-------------+----------------------+--------------+
| Date        | Intervention         | Ajouté par   |
+-------------+----------------------+--------------+
| 20/08/2026  | Début du chantier    | Employé 1    |
| 22/08/2026  | Terrassement terminé | Employé 1    |
| 25/08/2026  | Ajout fondations     | Gérant       |
+-------------+----------------------+--------------+
```

### Données affichées

- date de l’intervention ;
- description de l’intervention ;
- utilisateur ayant ajouté l’intervention ;
- chantier concerné.

### Règles prévues

- Une intervention est liée à un chantier.
- Une intervention doit contenir une date et une description.
- L’historique permet de suivre l’avancement du chantier.
- Les interventions doivent être visibles par l’équipe interne.

---

## 6. Maquette — Rapport PDF

### Objectif de l’écran

Préparer la génération d’un rapport PDF de chantier.

### Utilisateurs concernés

- Administrateur
- Gérant

### Éléments affichés

```text
+--------------------------------------------------+
| Rapport PDF — Maison Durand                      |
+--------------------------------------------------+

Informations chantier :
- Client : M. Durand
- Adresse : 12 rue Exemple, Saint-Pierre
- Statut : En cours
- Date de début : 20/08/2026

Contenu du rapport :
[ x ] Informations générales
[ x ] Historique des interventions
[ x ] Liste des documents
[ x ] Photos de chantier

[ Générer le rapport PDF ]
```

### Données affichées

- informations générales du chantier ;
- client ;
- adresse ;
- statut ;
- date de début ;
- historique des interventions ;
- documents ;
- photos.

### Règles prévues

- Le rapport PDF sera généré à partir des informations du chantier.
- L’accès au rapport sera réservé au gérant et à l’administrateur.
- La première version restera simple.
- Le rapport permettra d’avoir une synthèse exploitable du chantier.

---

## 7. Maquette — Administration des utilisateurs

### Objectif de l’écran

Permettre à l’administrateur de gérer les utilisateurs de l’application.

### Utilisateur concerné

- Administrateur

### Éléments affichés

```text
+--------------------------------------------------+
| Administration des utilisateurs                  |
+--------------------------------------------------+

[ + Ajouter un utilisateur ]

+----+----------+----------+----------------+------------+
| ID | Nom      | Prénom   | Email          | Rôle       |
+----+----------+----------+----------------+------------+
| 1  | Admin    | EcoTech  | admin@test.fr  | Admin      |
| 2  | Payet    | Jean     | gerant@test.fr | Gérant     |
| 3  | Hoarau   | Marc     | employe@test.fr| Employé    |
+----+----------+----------+----------------+------------+

Actions :
[ Modifier ] [ Désactiver ]
```

### Données affichées

- identifiant de l’utilisateur ;
- nom ;
- prénom ;
- email ;
- rôle ;
- actions possibles.

### Règles prévues

- Seul l’administrateur peut gérer les utilisateurs.
- Chaque utilisateur possède un rôle.
- Les rôles prévus sont : administrateur, gérant et employé.
- Aucun accès client n’est prévu dans la première version.

---

## Synthèse des maquettes

| N° | Écran | Objectif | Priorité |
|---:|---|---|---|
| 1 | Page de connexion | Accéder à l’application | Haute |
| 2 | Liste des chantiers | Consulter les chantiers | Haute |
| 3 | Fiche chantier | Voir les informations d’un chantier | Haute |
| 4 | Documents et photos | Centraliser les fichiers | Haute |
| 5 | Historique des interventions | Suivre l’avancement du chantier | Haute |
| 6 | Rapport PDF | Générer une synthèse | Moyenne |
| 7 | Administration des utilisateurs | Gérer les rôles et accès | Moyenne |

## Remarque

Ces maquettes sont des maquettes fonctionnelles en texte.

Elles ne correspondent pas encore à du code HTML, CSS ou PHP.

Elles seront utilisées pour préparer les futures pages de l’application.

