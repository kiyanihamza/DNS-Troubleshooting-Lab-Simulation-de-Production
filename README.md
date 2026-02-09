# 🌐 DNS Troubleshooting Lab : Simulation de Production

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E9431E?style=for-the-badge&logo=ubuntu&logoColor=white)

> **Le saviez-vous ?** Environ 30% des pannes de services sont causées par des problèmes DNS. 

Ce projet construit un laboratoire réseau complet via Docker pour simuler un environnement de production. L'objectif est d'apprendre à valider des configurations critiques et à diagnostiquer des erreurs de résolution de noms en conditions réelles.

---

## 🛠️ Architecture du Projet
Le lab repose sur deux composants principaux isolés dans un réseau virtuel (`172.20.0.0/16`) :

* **Le Serveur DNS (`dns-server`)** : Basé sur `dnsmasq`, il simule un résolveur d'entreprise avec des entrées personnalisées.
* **La Machine de Test (`lab-ubuntu`)** : Une instance Ubuntu équipée des outils de diagnostic (`dnsutils`, `iputils-ping`, `traceroute`).



---

## 🚀 Pourquoi ce Lab ?

En production, la commande `dig +short` est un "annuaire téléphonique automatique". Chez des géants comme **Netflix**, des scripts similaires valident les configurations DNS avant chaque déploiement. 

Le format `+short` offre une réponse épurée, idéale pour l'automatisation : c'est demander juste le numéro de téléphone sans les détails administratifs inutiles.

---

## 💻 Installation Rapide (WSL2 / Linux)

### 1. Cloner le dépôt
```bash
git clone [https://github.com/votre-nom/dns-lab-production.git](https://github.com/votre-nom/dns-lab-production.git)
cd dns-lab-production
