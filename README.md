.
├── docker-compose.yml
├── dnsmasq.conf
├── scripts/
│   └── dns_test.txt
└── README.md


🛠️ Architecture du Projet
Le lab repose sur deux composants principaux isolés dans un réseau virtuel (172.20.0.0/16) :

Le Serveur DNS (dns-server) : Utilise dnsmasq pour simuler un résolveur d'entreprise avec des entrées personnalisées (app.example.com, etc.).

La Machine de Test (lab-ubuntu) : Une instance Ubuntu équipée des outils dnsutils, iputils-ping et traceroute.

Cloner le dépôt :
git clone https://github.com/votre-nom/dns-lab-production.git
cd dns-lab-production
Lancer l'environnement :
docker compose up -d
Accéder à la machine de test :
docker exec -it lab-ubuntu bash
