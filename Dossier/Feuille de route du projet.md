Feuille de route du projet

Voici un plan de travail structuré pour construire le projet avant de rédiger le rapport :

Étape 1 - Création de l'application Node.js

 Créer une app Node.js simple avec Express

 Ajouter une route / qui retourne "Hello World"

 Ajouter un fichier package.json + app.js

 Ajouter un test unitaire basique avec Jest

Étape 2 - Conteneurisation avec Docker

 Créer un Dockerfile pour Node.js

 Créer un docker-compose.yml (si base de données ou Prometheus local)

 Tester le build + run en local

Étape 3 - Infrastructure as Code avec Ansible

 Créer un playbook.yml pour installer Docker, Git, Node.js (si besoin)

 Automatiser la création du serveur (ex: une VM locale ou VPS)

 Tester l’installation complète via Ansible

Étape 4 - Intégration Continue avec GitLab CI

 Écrire .gitlab-ci.yml

 Étape 1 : build image Docker

 Étape 2 : exécuter les tests unitaires

 Étape 3 : déploiement (optionnel)

 Tester les pipelines avec un push sur GitLab

Étape 5 - Tests

✅ Unitaires (Node.js) :

 Installer Jest : npm install --save-dev jest

 Créer un test simple sur la route /

 Intégrer dans le pipeline GitLab CI

✅ Infra (Ansible) :

 Installer Testinfra ou Molecule

 Écrire un test pour vérifier que Docker est bien installé

 Exécuter les tests à la fin du playbook

Étape 6 - Déploiement continu

 Intégrer dans GitLab CI une étape de déploiement automatique

 Choisir une méthode :

Push image Docker vers registry + docker-compose up

Ou SSH + Ansible pull + redéploiement

Étape 7 - Monitoring avec Prometheus & Grafana

 Ajouter Prometheus dans docker-compose.yml

 Ajouter un endpoint /metrics à l’app Node.js (avec prom-client)

 Configurer Grafana pour lire les métriques Prometheus

 Ajouter un dashboard simple

Étape 8 - Veille technologique

 Réaliser un mini état de l’art :

CI/CD : Jenkins vs GitLab CI

Monitoring : Prometheus vs Zabbix

Infra : Ansible vs Terraform

 Justifier pourquoi tu as choisi chaque outil