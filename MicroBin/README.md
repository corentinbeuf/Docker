# MicroBin
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Apache
- Créer le dossier "**microbin**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/microbin
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/microbin
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/MicroBin/docker-compose.yml > docker-compose.yml
```
- Télécharger le fichier **.env**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/MicroBin/.env > .env
```
- Démarrer le conteneur.
```bash
docker compose --env-file .env up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:8080`

## Configuration
- NA

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f microbin
```
- Supprimer l'image "**danielszabo99/microbin:latest**" présente sur le serveur.
```bash
sudo docker image rm -f danielszabo99/microbin:latest
```
- Redémarrer le conteneur.
```bash
cd /docker/microbin && sudo docker compose --env-file .env up -d
```