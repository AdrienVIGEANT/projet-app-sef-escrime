# projet-app-sef-escrime

## Présentation du projet

**Badminton Club Manager** est une application web de gestion d'un club de badminton, développée dans le cadre du **BTS SIO (Services Informatiques aux Organisations), option SLAM, 2ᵉ année**, sous la supervision de **Monsieur Lenoble**.

L'objectif du projet est de faciliter la gestion quotidienne d'un club sportif en centralisant les informations concernant les adhérents, les entraîneurs, les entraînements et les compétitions.

L'application propose différents espaces selon le rôle de l'utilisateur : administrateur, entraîneur ou joueur.

## Équipe

Le projet est réalisé par :

- **Adrien VIGEANT**
- **Léa LACROIX**
- **Rafaël BUQUET**
- **Malone PWONO**

## Sujet

### Gestion d'un club de badminton

Le projet consiste à développer une application web permettant de gérer les activités d'un club de badminton.

L'application doit permettre :

- La gestion des adhérents du club.
- La gestion des entraîneurs.
- L'organisation des entraînements.
- La gestion des compétitions.
- Le suivi des objectifs sportifs des joueurs.
- La gestion des comptes utilisateurs et des autorisations.

L'objectif est de proposer une interface simple, intuitive et adaptée aux différents utilisateurs.

## Fonctionnalités principales

### 1. Administrateur

L'administrateur dispose des droits nécessaires à la gestion du club.

Il peut notamment :

- Consulter et gérer les adhérents.
- Ajouter, modifier et supprimer des utilisateurs.
- Gérer les entraîneurs.
- Organiser les compétitions.
- Consulter les informations générales du club.

### 2. Entraîneur

L'entraîneur dispose d'un espace dédié au suivi sportif des joueurs.

Il peut :

- Consulter les joueurs dont il assure le suivi.
- Organiser les séances d'entraînement.
- Définir des objectifs sportifs.
- Suivre la progression des joueurs.
- Consulter les entraînements programmés.

### 3. Joueur

Chaque joueur possède un espace personnel lui permettant de :

- Consulter ses informations personnelles.
- Consulter ses entraînements.
- Suivre ses objectifs sportifs.
- Consulter les compétitions proposées.
- S'inscrire aux compétitions lorsque cette fonctionnalité est disponible.

### 4. Authentification et sécurité

L'application prévoit :

- Un système de connexion et de déconnexion.
- Une gestion des rôles.
- Une restriction d'accès aux pages selon les autorisations.
- Le hachage sécurisé des mots de passe.
- La validation des formulaires.

## Technologies

Le projet utilise les technologies suivantes :

| Technologie | Utilisation |
|---|---|
| PHP 8.4 | Développement côté serveur |
| Symfony 8.1 | Framework PHP |
| Twig | Création des vues |
| HTML5 | Structure des pages |
| CSS3 | Mise en forme de l'interface |
| JavaScript | Interactions côté client |
| MySQL | Gestion de la base de données |
| Doctrine ORM | Communication avec la base de données |
| Composer | Gestion des dépendances |
| Git | Gestion des versions |
| GitHub | Hébergement du code et travail collaboratif |
| Visual Studio Code | Environnement de développement |

## Organisation du projet

Le projet respecte l'architecture MVC (Modèle - Vue - Contrôleur) utilisée par Symfony.

### Arborescence

```text
projet-app-sef-escrime/
│
├── assets/
├── bin/
├── config/
├── docs/
├── migrations/
│
├── public/
│   ├── css/
│   ├── js/
│   ├── images/
│   └── index.php
│
├── src/
│   ├── Controller/
│   ├── Entity/
│   ├── Form/
│   ├── Repository/
│   └── Service/
│
├── templates/
│   ├── accueil/
│   ├── admin/
│   ├── joueur/
│   ├── entraineur/
│   ├── entrainement/
│   ├── competition/
│   └── base.html.twig
│
├── tests/
├── translations/
├── var/
├── vendor/
│
├── .env
├── .gitignore
├── composer.json
├── composer.lock
├── CONTRIBUTING.md
└── README.md
```

Cette arborescence représente la structure cible du projet. Certains dossiers seront créés progressivement au cours du développement.

Les dossiers `vendor/` et `var/` ne doivent pas être versionnés dans Git.

## Gestion du projet

Le projet est développé de manière collaborative avec Git et GitHub.

Les outils utilisés sont :

- **GitHub Issues** : suivi des fonctionnalités et des problèmes.
- **GitHub Projects / Kanban** : organisation des tâches.
- **Branches Git** : développement indépendant des fonctionnalités.
- **Pull Requests** : proposition et intégration des modifications.
- **Revue de code** : vérification du travail avant fusion.

Les règles de travail (branches, commits, Pull Requests, relectures) sont détaillées dans [CONTRIBUTING.md](CONTRIBUTING.md).

### Organisation des branches

La branche `main` contient la version principale du projet.

Chaque fonctionnalité est développée sur une branche spécifique.

Exemples :

```text
main
│
├── feature/1-accueil
├── feature/2-layout
├── feature/3-base-donnees
├── feature/4-entites
├── feature/5-authentification
├── feature/6-admin
├── feature/7-entraineur
├── feature/8-joueur
├── feature/9-competitions
└── feature/10-tests-docs
```

Les numéros des branches sont à adapter aux numéros réels des issues GitHub.

### Issues prévues

| Tâche | Description |
|---|---|
| Page d'accueil | Création du contrôleur, de la vue Twig et du CSS |
| Navigation et layout | Menu, footer et structure commune |
| Base de données | Configuration de MySQL et Doctrine |
| Entités et relations | Modélisation des données |
| Authentification | Connexion, inscription et gestion des rôles |
| Espace administrateur | Gestion des adhérents et du club |
| Espace entraîneur | Gestion des entraînements et objectifs |
| Espace joueur | Consultation du profil et des activités |
| Compétitions | Organisation et gestion des inscriptions |
| Tests et documentation | Vérification et documentation du projet |

### Cycle de développement

Pour chaque fonctionnalité :

1. Créer une issue GitHub.
2. Créer une branche dédiée depuis `main`.
3. Développer la fonctionnalité.
4. Tester les modifications localement.
5. Effectuer les commits et le push.
6. Créer une Pull Request.
7. Faire relire et valider le code.
8. Fusionner la branche dans `main`.
9. Clôturer l'issue correspondante.

## Lancer le projet

### Prérequis

Pour exécuter le projet en local, il est nécessaire de disposer de :

- PHP 8.4 ou version compatible.
- Composer.
- Symfony CLI.
- Git.
- MySQL pour les fonctionnalités utilisant la base de données.

### 1. Cloner le repository

```bash
git clone https://github.com/lealacroix5/projet-app-sef-escrime.git
```

Puis accéder au dossier :

```bash
cd projet-app-sef-escrime
```

### 2. Installer les dépendances

```bash
composer install
```

### 3. Configurer les variables d'environnement

Créer un fichier `.env.local` à la racine du projet.

Configurer notamment la variable `DATABASE_URL` selon l'installation locale de MySQL.

Les identifiants et mots de passe ne doivent pas être publiés sur GitHub.

### 4. Créer la base de données

Lorsque les entités et migrations auront été développées :

```bash
php bin/console doctrine:database:create
php bin/console doctrine:migrations:migrate
```

### 5. Lancer le serveur Symfony

```bash
symfony server:start
```

Accéder ensuite à l'adresse indiquée par Symfony, généralement :

http://127.0.0.1:8000

## Membres

Les responsabilités seront réparties entre les membres de l'équipe au cours du développement.

| Nom | Rôle principal | Fonctionnalités principales | Issues |
|---|---|---|---|
| Léa LACROIX | Développeuse Frontend / Intégration | Page d'accueil, navigation, Twig, CSS et espace joueur | #1, #2, #8 |
| Rafaël BUQUET | Développeur Backend / Base de données | MySQL, Doctrine, entités, relations et migrations | #3, #4 |
| Adrien VIGEANT | Développeur Backend / Sécurité | Authentification, rôles, comptes utilisateurs et espace administrateur | #5, #6 |
| Malone PWONO | Développeur Fonctionnalités métier | Espace entraîneur, entraînements, objectifs sportifs et compétitions | #7, #9 |
| Toute l'équipe | Tests / Documentation | Tests, corrections, documentation et préparation du déploiement | #10 |

Chaque membre participe au développement, aux tests, à la documentation et à la revue de code.

## Déploiement

L'application sera développée et testée localement, puis pourra être déployée sur une machine virtuelle Linux.

Le déploiement devra respecter les bonnes pratiques de sécurité :

- Ne pas exécuter le site ou le serveur web en tant qu'utilisateur `root`.
- Utiliser un compte disposant uniquement des permissions nécessaires.
- Protéger les identifiants et les données sensibles.
- Configurer correctement les permissions des fichiers.
- Utiliser un environnement de production adapté.

## État du projet

**Phase actuelle : initialisation et préparation du développement.**

L'environnement Symfony est installé et une première arborescence a été préparée.

Les prochaines étapes consistent à mettre en place les issues GitHub et à développer les premières pages de l'application.
