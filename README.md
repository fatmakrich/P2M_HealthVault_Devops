# HealthVault
# EHR Application - Gestion sécurisée des dossiers médicaux électroniques

# Description du projet

Cette application web EHR (Electronic Health Record) vise à fournir une solution sécurisée et efficace pour gérer les dossiers médicaux électroniques. Elle est développée avec une approche DevOps en utilisant des outils tels que Docker et Jenkins pour automatiser le déploiement et la maintenance.
Grâce à une architecture CI/CD robuste, le projet garantit des livraisons rapides, sécurisées et fiables, optimisant ainsi le cycle de vie du développement logiciel.

# Fonctionnalités

- Gestion des dossiers médicaux électroniques : Une interface intuitive pour accéder, mettre à jour et gérer les dossiers patients.
- Sécurité et authentification : Système d'authentification basé sur JWT (JSON Web Tokens) pour protéger les données sensibles.
- Scalabilité et portabilité : Application containerisée pour assurer un déploiement cohérent dans différents environnements.
  
# Technologies utilisées

- Front-end : Développé avec Angular.
- Back-end : API développée avec Express.js.
- Base de données : MongoDB avec interface d'administration Mongo-Express.
- Containerisation : Docker et Docker Compose.
- Automatisation CI/CD : Jenkins orchestrant les pipelines CI/CD.
- Contrôle de version : GitHub pour la gestion du code source.
  
# Architecture CI/CD

- Pipeline CI/CD avec Jenkins
  
1- Jenkins récupère le code source : Chaque commit sur le dépôt GitHub déclenche le pipeline.
  
2- Création d'image Docker.

3- Jenkins construit une image Docker via le Dockerfile.

4- L'image est publiée sur DockerHub.

# Processus de containerisation

1- Dockerfiles :

- Dockerfiles distincts pour le front-end et le back-end, avec leurs dépendances spécifiques.
- Utilisation d'images officielles pour MongoDB et Mongo-Express.
  
2- Docker Compose :

- Fichier docker-compose.yml pour orchestrer les services (front-end, back-end, MongoDB, Mongo-Express) et leurs interactions.
