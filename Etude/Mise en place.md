# 1. Installer Docker sur Debian 12 (Bookworm)

Pourquoi ? Docker permet d’isoler ton application Node.js dans un conteneur, standardisant l’environnement de dev, de test et de production.

# Étapes principales :

## Mets à jour ta VM (requis par tous les outils).

sudo apt update && sudo apt upgrade -y


## Installe les dépendances nécessaires à l'ajout d'un repo HTTPS.

sudo apt install apt-transport-https ca-certificates curl gnupg lsb-release


## Ajoute la clé GPG officielle de Docker :

curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg


## Ajoute le dépôt Docker stable :

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update


## Installe Docker et ses composants utiles :

sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin


## Lance Docker et active-le au démarrage :

sudo systemctl start docker
sudo systemctl enable docker


## Vérifie que tout est opérationnel :

sudo docker run hello-world
docker --version
docker compose version


### Optionnel : ajoute ton utilisateur au groupe docker pour éviter sudo à chaque commande :

sudo usermod -aG docker $USER

