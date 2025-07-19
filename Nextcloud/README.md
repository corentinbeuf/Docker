# Nextcloud
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Nextcloud
- Créer le dossier "**nextcloud**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/nextcloud
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/nextcloud
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Nextcloud/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:22080`

## Configuration
- Se rendre sur la page web.
- Créer un compte puis cliquer sur "**Installer**".
- Sélectionner les applications que vous souhaitez installer puis cliquer sur "**Installer les applications recommandées**". Sinon, cliquer sur "**Ignorer**".

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer les conteneurs en cours d'exécution.
```bash
sudo docker rm -f nextcloud_cron nextcloud_app 
```
- Supprimer l'image "**nextcloud**" présente sur le serveur.
```bash
sudo docker image rm -f nextcloud
```
- Redémarrer le conteneur.
```bash
cd /docker/nextcloud && sudo docker compose up -d
```
