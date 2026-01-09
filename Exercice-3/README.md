# Exercice 3 – Déploiement de WordPress avec Docker

## Objectif
L’objectif de cet exercice est de déployer un site WordPress en utilisant
des conteneurs Docker afin de mettre en place une architecture web simple,
moderne et automatisée.

L’environnement comprend :
- un serveur web Nginx,
- un service PHP-FPM,
- une base de données MariaDB,
- un site WordPress accessible via un navigateur.

---

## Environnement utilisé
- Windows 11
- Docker Desktop avec WSL2
- Docker Compose
- Navigateur web (Chrome / Edge)

---

## Architecture de la solution

La solution est basée sur trois conteneurs :
- **nginx** : serveur web qui reçoit les requêtes HTTP,
- **php** : moteur PHP pour WordPress,
- **db** : base de données MariaDB.

Tous les services communiquent entre eux via un réseau Docker privé.

---

## Étapes de réalisation

### 1. Installation de Docker
- Installation de Docker Desktop.
- Activation de WSL2.
- Vérification de l’installation avec la commande :
  docker --version

### 2. Création des fichiers de configuration
- Création du fichier docker-compose.yml pour définir les services.
- Création du fichier nginx.conf pour configurer le serveur web.

### 3. Lancement des conteneurs
- Démarrage de l’environnement avec :
  docker compose up -d

### 4. Installation de WordPress
- Accès à l’URL :
  http://localhost:8080
- Configuration du site WordPress :
  - titre du site,
  - compte administrateur,
  - mot de passe,
  - adresse e-mail.

---

## Vérifications
- Vérification de l’état des conteneurs avec :
  docker ps
- Vérification de l’accès au site WordPress dans le navigateur.
- Test de connexion à l’interface d’administration WordPress.

---

## Résultat
Le site WordPress est fonctionnel.
Les conteneurs sont opérationnels et communiquent correctement entre eux.
L’objectif de déploiement d’une application web avec Docker est atteint.
