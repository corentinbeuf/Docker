# Wekan

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Wekan
- Créer le dossier "**wekan**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/wekan
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/wekan
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Wekan/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier le champ suivant dans le fichier :
	- `ROOT_URL`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Quand le conteneur se créé, nous visualisons dans les logs qu'il manque des permissions sur les dossiers de Wekan.
- Donner tous les droits sur le dossier "assets".
```bash
sudo chmod -R 777 wekan-*/
```
- Redémarrer le conteneur.
```bash
docker compose restart
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP`

## Configuration
- Se créer un compte.
- Une fois connecter, créer des tableaux et compléter les.

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f wekan-db wekan
```
- Supprimer les images présentent sur le serveur.
```bash
sudo docker image rm -f mongo:6 wekanteam/wekan:latest
```
- Editer le fichier "**docker-compose.yml**".
```bash
sudo nano /docker/caddy/docker-compose.yml
```
- Modifier les étiquettes des images.
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Redémarrer le conteneur.
```bash
cd /docker/wekan && sudo docker compose up -d
```