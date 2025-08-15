# Feuille de route du projet

Voici un plan de travail structuré pour construire le projet avant de rédiger le rapport :

---

## Étape 1 - Création de l'application Node.js

- Créer une application Node.js simple avec Express
- Ajouter une route `/` qui retourne `"Hello World"`
- Ajouter un fichier `package.json` et `app.js`
- Ajouter un test unitaire basique avec Jest

---

## Étape 2 - Conteneurisation avec Docker

- Créer un `Dockerfile` pour l’application Node.js
- Créer un `docker-compose.yml` (si base de données ou Prometheus local)
- Tester le build et le run en local

---

## Étape 3 - Infrastructure as Code avec Ansible

- Créer un `playbook.yml` pour installer Docker, Git, Node.js (si besoin)
- Automatiser la création du serveur (ex : une VM locale ou VPS)
- Tester l’installation complète via Ansible

---

## Étape 4 - Intégration Continue avec GitLab CI

- Écrire `.gitlab-ci.yml` avec les étapes suivantes :
  1. Build de l’image Docker
  2. Exécution des tests unitaires
  3. Déploiement (optionnel)
- Tester les pipelines avec un push sur GitLab

---

## Étape 5 - Tests

### ✅ Tests unitaires (Node.js)

- Installer Jest : `npm install --save-dev jest`
- Créer un test simple sur la route `/`
- Intégrer les tests dans le pipeline GitLab CI

### ✅ Tests d'infrastructure (Ansible)

- Installer Testinfra ou Molecule
- Écrire un test pour vérifier que Docker est bien installé
- Exécuter les tests à la fin du playbook

---

## Étape 6 - Déploiement continu

- Intégrer dans GitLab CI une étape de déploiement automatique
- Choisir une méthode de déploiement :
  - Push de l’image Docker vers un registre + `docker-compose up`
  - Ou SSH + Ansible pull + redéploiement

---

## Étape 7 - Monitoring avec Prometheus & Grafana

- Ajouter Prometheus dans `docker-compose.yml`
- Ajouter un endpoint `/metrics` à l’application Node.js (avec `prom-client`)
- Configurer Grafana pour lire les métriques Prometheus
- Ajouter un dashboard simple

---

## Étape 8 - Veille technologique

Réaliser un mini état de l’art :

- CI/CD : Jenkins vs GitLab CI
- Monitoring : Prometheus vs Zabbix
- Infrastructure as Code : Ansible vs Terraform

Justifier les choix de chaque outil

---
