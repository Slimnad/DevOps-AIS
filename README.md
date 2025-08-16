# Projet DevOps

## 📌 Objectif

Mettre en place une chaîne complète DevOps pour une application Node.js, incluant :
- Conteneurisation (Docker)
- Infrastructure as Code (Ansible)
- Intégration et déploiement continu (GitLab CI)
- Monitoring (Prometheus & Grafana)

---

## Description

Ce dépôt contient un projet DevOps complet intégrant :
- Une application Node.js
- Une infrastructure Docker & Docker Compose
- Des playbooks Ansible pour la gestion de l'infrastructure
- Un pipeline CI/CD via GitLab CI
- Une configuration de monitoring avec Prometheus et Grafana

---

## Prérequis

- Docker & Docker Compose
- Node.js (14+)
- Ansible (2.9+)
- Un compte GitLab avec CI/CD activé

---

##  Structure du projet

projet-devops/
├── app/ # Application Node.js + tests Jest
├── Dockerfile # Image de l'application
├── docker-compose.yml # Orchestration des services
├── ansible/ # Playbook + tests d'infra
├── .gitlab-ci.yml # Pipeline GitLab
├── monitoring/ # Prometheus + Grafana
└── README.md # Documentation

---

## Sources :

*https://docs.docker.com*

*https://docs.ansible.com*

*https://docs.gitlab.com/ee/ci/*

*https://prometheus.io/docs*

*https://grafana.com/docs/*

---

## Veille technologique 

| Besoin           | Outil choisi        | Justification rapide                       |
| ---------------- | ------------------- | ------------------------------------------ |
| CI/CD            | GitLab CI           | Intégré à GitLab, facile à configurer      |
| Conteneurisation | Docker, Compose     | Standard du marché, rapide à déployer      |
| IaC              | Ansible             | Simple, lisible, sans agent                |
| Tests            | Jest, Testinfra     | Léger et adapté à Node.js et à l’infra     |
| Monitoring       | Prometheus, Grafana | Open-source, extensible, facile à intégrer |


---

Licence

Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus de détails.

