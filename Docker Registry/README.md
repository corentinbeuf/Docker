# Docker Registry

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Prérequis
- Mettre à jour les sources.
```bash
sudo apt-get update
```
- Installer le paquet "**apache2-utils**".
```bash
sudo apt-get install apache2-utis -y
```

### Docker Regsitry
- Créer le dossier "**regsitry**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/registry
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/registry
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Docker Registry/docker-compose.yml > docker-compose.yml
```
- Créer un dossier nommé "**auth**".
```bash
sudo mkdir auth
```
- Se rendre dans le dossier "**auth**".
```bash
cd auth/
```
- Créer un utilisateur pour se connecter à l'interface web.
```bash
sudo htpasswd -Bc registry.password nom_utilisateur
```
- Editer le fichier docker-compose.yml.
```bash
cd ..
sudo nano docker-compose.yml
```
- Modifier le champ suivant dans le fichier :
	- `ENV_DOCKER_REGISTRY_HOST`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour accéder à l'application : `http://IP:8080`

## Configuration
### Connexion à la registry
- Se connecter en SSH sur un serveur avec **Docker** d'installé.
- Se connecter à la registry :
```bash
docker login 192.168.122.231:5000
```

### Envoyer une image à la registry
- Créer votre image ou télécharger une image.
```bash
docker pull alpine
```
- Ajouter une étiquette à votre image.
```bash
docker tag alpine 192.168.122.231:5000/my-alpine
```
- Pousser l'image créé vers la registry.
```bash
docker push 192.168.122.231:5000/my-alpine
```

### Récupérer une image présente sur la registry
- Télécharger l'image.
```bash
docker pull 192.168.122.231:5000/my-alpine
```

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer les conteneurs en cours d'exécution.
```bash
sudo docker rm -f registry registry-ui
```
- Supprimer l'image "**https**" présente sur le serveur.
```bash
sudo docker image rm -f registry:2.8.1 konradkleine/docker-registry-frontend:v2
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano /docker/registry/docker-compose.yml
```
- Modifier les étiquettes des images.
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Redémarrer les conteneurs.
```bash
cd /docker/registry && sudo docker compose up -d
```