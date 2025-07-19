# BackupPC
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### BackupPC
- Créer le dossier "**backuppc**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/backuppc
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/backuppc
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/BackupPC/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier le champ suivant dans le fichier :
	- `BACKUPPC_WEB_PASSWD`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP`

## Configuration
- Se rendre sur la page web.
- Se connecter avec le compte renseigner dans le fichier "**docker-compose.yml**".
- Cliquer sur le menu "**Edit Hosts**" pour ajouter les serveurs clients.
- Cliquer sur le menu "**Edit Config**" pour répliquer la même configuration sur l'ensemble des serveurs clients.

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f backuppc
```
- Supprimer l'image "**adferrand/backuppc**" présente sur le serveur.
```bash
sudo docker image rm -f adferrand/backuppc
```
- Redémarrer le conteneur.
```bash
cd /docker/backuppc && sudo docker compose up -d
```