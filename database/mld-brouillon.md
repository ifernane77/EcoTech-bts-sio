# MLD brouillon — EcoTech Suivi Chantier

## Objectif

Ce document présente une première version du modèle logique de données du projet EcoTech Suivi Chantier.

Le MLD permet de préparer la future base de données MySQL à partir du MCD.  
Il indique les tables prévues, leurs champs principaux, les clés primaires et les clés étrangères.

Cette version reste un brouillon. Elle pourra être améliorée lors de la création du script SQL.

---

## Modèle logique de données

```text
roles(
    id,
    nom
)

users(
    id,
    role_id,
    nom,
    prenom,
    email,
    mot_de_passe
)

clients(
    id,
    nom,
    prenom,
    telephone,
    email,
    adresse
)

statuts(
    id,
    nom
)

chantiers(
    id,
    client_id,
    statut_id,
    nom,
    adresse,
    date_debut,
    date_fin_prevue,
    description
)

documents(
    id,
    chantier_id,
    user_id,
    nom_fichier,
    type_document,
    date_ajout
)

photos(
    id,
    chantier_id,
    user_id,
    nom_fichier,
    description,
    date_ajout
)

interventions(
    id,
    chantier_id,
    user_id,
    date_intervention,
    description
)
```

---

## Clés primaires

Chaque table possède une clé primaire appelée `id`.

```text
roles.id
users.id
clients.id
statuts.id
chantiers.id
documents.id
photos.id
interventions.id
```

---

## Clés étrangères

```text
users.role_id → roles.id

chantiers.client_id → clients.id
chantiers.statut_id → statuts.id

documents.chantier_id → chantiers.id
documents.user_id → users.id

photos.chantier_id → chantiers.id
photos.user_id → users.id

interventions.chantier_id → chantiers.id
interventions.user_id → users.id
```

---

## Explication des relations

| Relation | Explication |
|---|---|
| `roles` → `users` | Un rôle peut être attribué à plusieurs utilisateurs |
| `clients` → `chantiers` | Un client peut avoir plusieurs chantiers |
| `statuts` → `chantiers` | Un statut peut être utilisé par plusieurs chantiers |
| `chantiers` → `documents` | Un chantier peut contenir plusieurs documents |
| `chantiers` → `photos` | Un chantier peut contenir plusieurs photos |
| `chantiers` → `interventions` | Un chantier peut avoir plusieurs interventions |
| `users` → `documents` | Un utilisateur peut ajouter plusieurs documents |
| `users` → `photos` | Un utilisateur peut ajouter plusieurs photos |
| `users` → `interventions` | Un utilisateur peut enregistrer plusieurs interventions |

---

## Justification du modèle

Le modèle reste volontairement simple pour correspondre au niveau attendu en BTS SIO SLAM.

Il permet de gérer les éléments essentiels du projet :

- les utilisateurs ;
- les rôles ;
- les clients ;
- les chantiers ;
- les statuts ;
- les documents PDF ;
- les photos de chantier ;
- les interventions.

Ce modèle prépare la future création de la base de données MySQL.

---

## Limites du modèle

Cette version ne contient pas encore :

- les contraintes SQL détaillées ;
- les types exacts des champs ;
- les index ;
- les règles de suppression ;
- les données de test.

Ces éléments seront ajoutés plus tard dans le script SQL.