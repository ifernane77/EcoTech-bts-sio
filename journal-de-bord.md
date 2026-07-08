# Journal de bord — EcoTech Suivi Chantier

## Semaine 1 — Cadrage initial du projet

### Objectif de la semaine

L’objectif de cette semaine était d’organiser le projet EcoTech Suivi Chantier et de poser les premières bases documentaires.

Cette semaine correspond à une phase de cadrage : analyse du contexte, expression du besoin, définition des objectifs et création d’un backlog initial.

### Travail réalisé

- Création ou vérification du dossier projet.
- Création ou vérification du dépôt GitHub.
- Rédaction du contexte entreprise.
- Rédaction de l’expression du besoin.
- Définition des objectifs du projet.
- Création du backlog initial.
- Préparation des premières preuves pour le portfolio.

### Difficultés rencontrées

J’ai dû comprendre la différence entre le dossier local, le dépôt Git local et le dépôt distant GitHub.

J’ai aussi compris que la commande `git init` sert à créer un dépôt Git local, mais qu’il faut également créer un dépôt sur GitHub pour pouvoir envoyer le projet en ligne.

### Solutions apportées

J’ai vérifié l’état du dépôt avec `git status`, puis le lien GitHub avec `git remote -v`.

J’ai ensuite préparé les fichiers Markdown du projet afin d’avoir une documentation claire et exploitable.

### Résultat obtenu

Le projet dispose maintenant d’une première documentation structurée :

- présentation du projet ;
- contexte de l’entreprise ;
- expression du besoin ;
- objectifs ;
- backlog initial ;
- journal de bord.

### Preuves produites

- Capture du dossier local.
- Capture du dépôt GitHub.
- Capture des fichiers Markdown dans VS Code.
- Capture du backlog.
- Capture du commit Git.
- Capture du README affiché sur GitHub.

### Lien avec le BTS SIO

Cette semaine permet de préparer l’épreuve E6 SLAM car elle pose les bases d’une solution applicative.

Elle peut aussi servir partiellement pour E5 grâce au travail d’organisation, de documentation et de cadrage dans un contexte professionnel.

## Semaine 2 — Architecture et flux autour de l’application

### Objectif de la semaine

L’objectif de cette semaine était de comprendre les flux d’informations autour du suivi de chantier chez EcoTech.

J’ai identifié les acteurs principaux, les outils actuellement utilisés et les problèmes liés à la dispersion des informations.

### Travail réalisé

- Identification des acteurs : gérants, employés, prestataires terrain et clients.
- Analyse des flux actuels : documents, photos, devis, factures et échanges.
- Description du stockage actuel : Google Drive, mails, WhatsApp et PC personnels.
- Préparation d’un schéma simplifié des flux.
- Rédaction de questions à poser au gérant pour confirmer le besoin.

### Difficultés rencontrées

La difficulté principale a été de bien distinguer les flux actuels et les flux prévus avec la future application.

### Résultat obtenu

Cette semaine m’a permis de mieux comprendre comment les informations circulent actuellement chez EcoTech.

J’ai produit une première cartographie des flux qui servira ensuite pour la conception de la base de données, des rôles et des fonctionnalités de l’application.

### Preuves produites

- architecture-et-flux.md
- acteurs-et-roles.md
- stockage-actuel.md
- questions-gerant.md
- capture du schéma Mermaid sur GitHub
- capture du commit Git

## Semaine 3 — Cas d’utilisation et architecture applicative

### Objectif de la semaine

L’objectif de cette semaine était de définir les principaux cas d’utilisation de l’application EcoTech Suivi Chantier.

Ce travail permet de préparer la conception fonctionnelle de l’application avant de passer aux maquettes, au modèle de données et au développement.

### Travail réalisé

- Rédaction des cas d’utilisation principaux.
- Identification des acteurs concernés.
- Création d’un diagramme simplifié des cas d’utilisation.
- Rédaction de l’architecture applicative prévue.
- Justification des rôles : administrateur, gérant et employé.
- Mise à jour de la documentation du projet.

### Cas d’utilisation rédigés

- Créer un client.
- Créer un chantier.
- Ajouter un document PDF.
- Ajouter une photo de chantier.
- Enregistrer une intervention.
- Générer un rapport PDF.

### Difficultés rencontrées

La difficulté principale a été de garder un périmètre réaliste. Certaines fonctionnalités pourraient être plus avancées, mais j’ai choisi de conserver une version simple et adaptée au BTS SIO SLAM.

### Résultat obtenu

Le projet dispose maintenant d’une base fonctionnelle plus claire. Les cas d’utilisation vont servir à préparer les maquettes, le MCD, la base de données et les pages PHP.

### Preuves produites

- cas-utilisation.md
- diagramme-cas-utilisation.md
- architecture-application.md
- capture du diagramme sur GitHub
- capture du commit Git

### Lien avec le BTS SIO

Cette semaine est liée à l’épreuve E6 SLAM, car elle prépare la conception d’une solution applicative.

## Semaine 4 — Préparation de l’environnement technique

### Objectif de la semaine

L’objectif de cette semaine était de préparer l’environnement technique du projet EcoTech Suivi Chantier avant de commencer le développement.

### Travail réalisé

- Création d’un fichier `installation.md`.
- Création d’un fichier `environnement-technique.md`.
- Création d’un fichier `conventions-nommage.md`.
- Préparation d’un dossier `database`.
- Préparation d’un dossier `storage/documents`.
- Préparation d’un dossier `storage/photos`.
- Mise à jour de la documentation du projet.

### Difficultés rencontrées

J’ai compris qu’il ne fallait pas commencer directement par le code, mais d’abord préparer une structure propre et une documentation claire.

### Résultat obtenu

Le projet dispose maintenant d’une base technique préparée pour les prochaines étapes.

Le développement PHP, la base de données et les tests locaux seront réalisés plus tard.

### Preuves produites

- `installation.md`
- `environnement-technique.md`
- `conventions-nommage.md`
- capture de l’arborescence VS Code
- capture GitHub
- commit Git

### Lien avec le BTS SIO

Cette semaine prépare l’épreuve E6 SLAM car elle organise l’environnement nécessaire au futur développement de l’application.

## Semaine 5 — Conception du modèle de données

### Objectif de la semaine

L’objectif de cette semaine était de préparer le modèle de données du projet EcoTech Suivi Chantier.

Cette étape permet d’identifier les futures tables nécessaires avant la création de la base MySQL.

### Travail réalisé

- Création d’un MCD brouillon.
- Création d’un MLD brouillon.
- Rédaction d’un dictionnaire de données.
- Rédaction des règles de gestion.
- Identification des principales entités : utilisateurs, rôles, clients, chantiers, statuts, documents, photos et interventions.
- Mise à jour de la documentation du projet.

### Difficultés rencontrées

La difficulté principale a été de rester simple et de ne pas prévoir trop de tables.

J’ai choisi un modèle adapté à une première version BTS SIO SLAM, avec uniquement les données nécessaires au suivi de chantier.

### Résultat obtenu

Le projet dispose maintenant d’une première conception de base de données.

Cette conception servira ensuite à créer le script SQL et à développer les premières fonctionnalités de l’application.

### Preuves produites

- `database/mcd-brouillon.md`
- `database/mld-brouillon.md`
- `database/dictionnaire-donnees.md`
- `database/regles-gestion.md`
- capture du diagramme Mermaid
- capture GitHub
- commit Git

### Lien avec le BTS SIO

Cette semaine est liée à l’épreuve E6 SLAM, car elle prépare la conception de la solution applicative et la future gestion des données.

## Semaine 6 — Maquettes fonctionnelles de l’application

### Objectif de la semaine

L’objectif de cette semaine était de créer les maquettes fonctionnelles du projet EcoTech Suivi Chantier.

Ces maquettes permettent de visualiser les écrans principaux avant le développement.

### Travail réalisé

- Création du dossier `maquettes`.
- Création du fichier `maquettes-fonctionnelles.md`.
- Préparation de la maquette 1 : page de connexion.
- Préparation de la maquette 2 : liste des chantiers.
- Préparation de la maquette 3 : fiche chantier.
- Préparation de la maquette 4 : documents et photos.
- Préparation de la maquette 5 : historique des interventions.
- Préparation de la maquette 6 : rapport PDF.
- Préparation de la maquette 7 : administration des utilisateurs.
- Création du fichier `parcours-utilisateur.md`.
- Création du fichier `justification-maquettes.md`.

### Difficultés rencontrées

La difficulté principale a été de rester simple.

J’ai évité de prévoir trop d’écrans ou des fonctionnalités trop avancées afin de garder un projet réaliste pour le BTS SIO SLAM.

### Résultat obtenu

Le projet dispose maintenant de maquettes fonctionnelles claires.

Ces maquettes serviront de base pour développer les futures pages PHP de l’application.

### Preuves produites

- `maquettes/maquettes-fonctionnelles.md`
- `maquettes/parcours-utilisateur.md`
- `maquettes/justification-maquettes.md`
- capture VS Code
- capture GitHub
- commit Git

### Lien avec le BTS SIO

Cette semaine est liée à l’épreuve E6 SLAM, car elle prépare la conception de l’interface et des fonctionnalités de l’application.

## Semaine 7 — Préparation de la structure applicative

### Objectif de la semaine

L’objectif de cette semaine était de préparer la structure applicative prévue pour le projet EcoTech Suivi Chantier.

Le développement PHP n’a pas encore commencé, car les leçons HTML, CSS, SQL et PHP seront étudiées plus tard dans le planning.

### Travail réalisé

- Création du dossier `public`.
- Création du dossier `src`.
- Création des sous-dossiers `config`, `controllers`, `models` et `views`.
- Préparation des dossiers `storage/documents` et `storage/photos`.
- Création du fichier `structure-applicative-prevue.md`.
- Création du fichier `pages-prevues.md`.
- Création du fichier `preparation-developpement.md`.
- Mise à jour de la documentation du projet.

### Difficultés rencontrées

La difficulté principale a été de ne pas commencer le développement trop tôt.

J’ai choisi de préparer une structure propre sans copier de code PHP ou HTML que je n’ai pas encore étudié.

### Résultat obtenu

Le projet dispose maintenant d’une arborescence technique claire.

Cette structure servira de base pour le développement futur de l’application, lorsque les notions de développement web auront été étudiées.

### Preuves produites

- `structure-applicative-prevue.md`
- `pages-prevues.md`
- `preparation-developpement.md`
- capture de l’arborescence VS Code
- capture GitHub
- commit Git

### Lien avec le BTS SIO

Cette semaine prépare l’épreuve E6 SLAM, car elle organise la future solution applicative avant le développement.

Elle montre aussi une démarche de projet réaliste et progressive.

## Semaine 8 — Préparation de la page portfolio EcoTech

### Objectif de la semaine

L’objectif de cette semaine était de préparer une première page portfolio pour le projet EcoTech Suivi Chantier.

Cette semaine est liée à l’identité professionnelle, au portfolio et à la préparation de l’oral.

### Travail réalisé

- Création du dossier `portfolio`.
- Création du fichier `presentation-portfolio-ecotech.md`.
- Création du fichier `preuves-portfolio.md`.
- Création du fichier `script-oral-ecotech.md`.
- Résumé du contexte EcoTech.
- Résumé du besoin métier.
- Présentation du périmètre du projet.
- Liste des preuves déjà produites.
- Préparation d’un court script oral.

### Difficultés rencontrées

La difficulté principale a été de présenter le projet simplement.

J’ai évité d’écrire une présentation trop longue ou trop professionnelle pour garder un niveau réaliste de BTS.

### Résultat obtenu

Le projet dispose maintenant d’une première base pour le portfolio.

Cette page pourra être reprise plus tard dans mon portfolio final avec des captures, des liens GitHub et les preuves importantes.

### Preuves produites

- `portfolio/presentation-portfolio-ecotech.md`
- `portfolio/preuves-portfolio.md`
- `portfolio/script-oral-ecotech.md`
- capture VS Code
- capture GitHub
- commit Git

### Lien avec le BTS SIO

Cette semaine prépare le portfolio et l’oral.

Elle permet aussi de relier le projet EcoTech aux compétences E6 SLAM et au stage.