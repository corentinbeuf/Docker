# Apache
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Apache
- Créer le dossier "**apache**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/apache
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/apache
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Apache/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:8080`

## Configuration
- Créer ou copier vos fichiers dans le dossier "**website**" (*/docker/apache/website*) créer lors du démarrage du conteneur. Le conteneur charge automatiquement le contenu ajouté dans le dossier.

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f my-apache-app
```
- Supprimer l'image "**https**" présente sur le serveur.
```bash
sudo docker image rm -f httpd
```
- Télécharger la nouvelle image Docker.
```bash
sudo docker pull httpd:latest
```
- Redémarrer le conteneur.
```bash
cd /docker/apache && sudo docker compose up -d
```