# Heimdall
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Heimdall
- Créer le dossier "**heimdall**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/heimdall
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/heimdall
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl https://raw.githubusercontent.com/corentinbeuf/Docker/main/Heimdall/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour accéder à l'application : `http://IP`

## Configuration
- NA

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f heimdall
```
- Supprimer l'image "**lscr.io/linuxserver/heimdall:latest**" présente sur le serveur.
```bash
sudo docker image rm -f lscr.io/linuxserver/heimdall:latest
```
- Redémarrer le conteneur.
```bash
cd /docker/heimdall && sudo docker compose up -d
```