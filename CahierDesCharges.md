# Cahier des charges – Projet AP SIO2

## Application Web de gestion d'un club d'escrime

**Projet :** SEF Escrime – M2L (Maison des Ligues de Lorraine)  
**Formation :** BTS SIO 2 – Option SLAM  
**Technologie principale :** Symfony 7.1  
**État actuel :** Installation de Symfony commencée sur une machine virtuelle

---

## 1. Présentation du projet

Dans le cadre de notre formation en BTS SIO, nous devons développer une application Web permettant de gérer un club d'escrime.

Cette application est destinée à trois types d'utilisateurs : les sportifs (adhérents), les entraîneurs (animateurs) et les administrateurs.

Elle permettra de faciliter la gestion du club, le suivi des entraînements, l'organisation des compétitions et la progression des sportifs.

Le projet doit être développé avec Symfony et utiliser une base de données MySQL.

## 2. Objectifs du projet

Les principaux objectifs sont :

- Développer une application Web fonctionnelle et responsive.
- Permettre aux utilisateurs de se connecter de manière sécurisée.
- Gérer les adhérents, les entraîneurs et les compétitions.
- Permettre aux entraîneurs de suivre les sportifs.
- Permettre aux sportifs de consulter leurs objectifs.
- Mettre en place une base de données MySQL.
- Protéger les informations personnelles des utilisateurs.
- Proposer une première version bêta pour décembre, conformément au sujet.

L'application devra être sous licence GPL afin de permettre sa réutilisation par d'autres clubs.

## 3. Technologies utilisées

| Technologie | Utilisation |
|---|---|
| Symfony 7.1 | Framework PHP pour développer l'application |
| PHP | Développement du backend |
| MySQL | Stockage des données |
| Doctrine ORM | Gestion de la base de données |
| Twig | Création des pages Web |
| HTML / CSS | Structure et mise en forme |
| JavaScript | Interactions côté utilisateur |
| Bootstrap (possible) | Interface responsive |
| GitHub ou GitLab | Stockage et suivi du code |
| Machine virtuelle | Hébergement de l'environnement de développement |

L'application devra séparer clairement le frontend (interface utilisateur) du backend (traitement des données).

## 4. Fonctionnalités à développer

### 4.1 Authentification – Obligatoire V1

- Créer une page de connexion `/login`.
- Créer une fonctionnalité de déconnexion `/logout`.
- Mettre en place trois rôles : administrateur, entraîneur et sportif.
- Sécuriser les mots de passe.
- Limiter l'accès aux pages selon le rôle de l'utilisateur.

### 4.2 Interface administrateur – Obligatoire V1

L'administrateur doit pouvoir :

- Consulter la liste des adhérents.
- Ajouter, modifier et supprimer des adhérents.
- Gérer les comptes des entraîneurs.
- Ajouter, modifier et supprimer des compétitions.
- Consulter les informations nécessaires à la gestion du club.

Pour cela, nous utiliserons les opérations CRUD avec Doctrine.

### 4.3 Interface entraîneur – Obligatoire V1

L'entraîneur doit pouvoir :

- Consulter les sportifs.
- Suivre les entraînements.
- Gérer les équipes.
- Gérer les inscriptions aux compétitions.
- Définir les objectifs sportifs de chaque adhérent.

### 4.4 Interface sportif – Obligatoire V1

Le sportif doit pouvoir :

- Se connecter à son espace.
- Consulter les objectifs fixés par son entraîneur.

### 4.5 Fonctionnalités complémentaires

Ces fonctionnalités sont mentionnées dans le sujet, mais ne sont pas toutes prioritaires pour la première version :

- Consulter son profil `/profil`.
- Consulter les objectifs sur `/objectifs`.
- Suivre son indice de performance.
- Permettre aux entraîneurs d'ajouter des commentaires.
- Afficher des statistiques sous forme de graphiques.
- Générer une fiche sportive au format PDF.
- Importer des données XML ou JSON.

## 5. Base de données

Nous devons créer une base de données MySQL afin de stocker les informations de l'application.

**Tables envisagées :**

| Table | Contenu |
|---|---|
| utilisateurs | Identifiants, noms, emails, mots de passe, rôles |
| sportifs | Informations propres aux adhérents sportifs |
| entraineurs | Informations sur les entraîneurs |
| competitions | Informations et dates des compétitions |
| inscriptions | Inscriptions des sportifs aux compétitions |
| entrainements | Séances d'entraînement |
| equipes | Équipes sportives |
| objectifs | Objectifs fixés aux sportifs |
| competences | Compétences à acquérir ou valider |

Ces tables constituent une proposition de départ. Leur structure définitive sera réalisée lors de la conception de la base de données.

## 6. Sécurité

L'application doit respecter plusieurs exigences :

- Authentification sécurisée.
- Mots de passe stockés sous forme de hash.
- Protection des routes selon les rôles.
- Vérification des données envoyées par les formulaires.
- Protection contre les injections SQL et les failles courantes.
- Respect du RGPD pour les données personnelles.
- Accès limité aux informations confidentielles.

## 7. Étapes de réalisation

### Étape 1 – Installation de l'environnement

**Statut : En cours**

- [x] Commencer l'installation de Symfony sur la VM.
- [ ] Vérifier le fonctionnement de Symfony.
- [ ] Vérifier la version de PHP et les dépendances.
- [ ] Installer et configurer MySQL si nécessaire.
- [ ] Configurer la connexion entre Symfony et MySQL.
- [ ] Créer le dépôt GitHub ou GitLab.

### Étape 2 – Conception de l'application

**Statut : À faire**

- [ ] Définir les besoins des trois types d'utilisateurs.
- [ ] Réaliser le schéma de la base de données.
- [ ] Créer les entités Doctrine.
- [ ] Créer les migrations.
- [ ] Préparer l'organisation des dossiers Symfony.

### Étape 3 – Authentification

**Statut : À faire**

- [ ] Créer l'entité User.
- [ ] Mettre en place les trois rôles.
- [ ] Créer la page de connexion.
- [ ] Ajouter la déconnexion.
- [ ] Protéger les routes de chaque interface.
- [ ] Tester les connexions avec plusieurs comptes.

### Étape 4 – Interface administrateur

**Statut : À faire**

- [ ] Créer le tableau de bord administrateur.
- [ ] Développer la gestion des sportifs.
- [ ] Développer la gestion des entraîneurs.
- [ ] Développer la gestion des compétitions.
- [ ] Ajouter les formulaires avec Symfony et Doctrine.

### Étape 5 – Interface entraîneur

**Statut : À faire**

- [ ] Créer le tableau de bord entraîneur.
- [ ] Afficher les sportifs suivis.
- [ ] Gérer les entraînements.
- [ ] Gérer les équipes.
- [ ] Gérer les inscriptions aux compétitions.
- [ ] Ajouter les objectifs des sportifs.

### Étape 6 – Interface sportif

**Statut : À faire**

- [ ] Créer l'espace sportif.
- [ ] Afficher les objectifs personnels.
- [ ] Prévoir l'affichage du profil et des performances pour les versions suivantes.

### Étape 7 – Tests et corrections

**Statut : À faire**

- [ ] Vérifier le fonctionnement de la connexion.
- [ ] Tester les droits des différents utilisateurs.
- [ ] Vérifier les fonctionnalités CRUD.
- [ ] Vérifier les données enregistrées dans MySQL.
- [ ] Tester l'affichage sur ordinateur et téléphone.
- [ ] Corriger les erreurs rencontrées.

## 8. Planning prévisionnel

| Phase | Travail prévu | Priorité |
|---|---|---|
| 1 | Terminer l'installation Symfony sur la VM | Haute |
| 2 | Créer la base de données et les entités | Haute |
| 3 | Développer l'authentification et les rôles | Haute |
| 4 | Créer l'interface administrateur | Haute |
| 5 | Créer l'interface entraîneur | Haute |
| 6 | Créer l'interface sportif | Haute |
| 7 | Effectuer les tests et corrections | Haute |
| 8 | Ajouter les statistiques et fonctionnalités avancées | Secondaire |

**Échéance indiquée dans le sujet :** une version bêta en décembre.

## 9. Livrables attendus

À la fin du projet, nous devrons disposer de :

- Une application Symfony fonctionnelle.
- Une base de données MySQL opérationnelle.
- Trois interfaces adaptées aux rôles.
- Un système d'authentification sécurisé.
- Des fonctionnalités de gestion des sportifs et compétitions.
- Un dépôt GitHub ou GitLab contenant l'intégralité du code source.
- Une application pouvant être présentée et testée.

## 10. Conclusion

Ce projet a pour but de développer une application Web de gestion de club d'escrime en utilisant Symfony.

Notre première priorité est de terminer la configuration de Symfony sur notre machine virtuelle et de préparer la base de données.

Nous pourrons ensuite développer progressivement les fonctionnalités obligatoires, en commençant par l'authentification, puis les interfaces administrateur, entraîneur et sportif.

Une fois ces éléments fonctionnels, nous pourrons améliorer l'application en ajoutant des statistiques, des rapports PDF et un suivi plus complet des performances sportives.