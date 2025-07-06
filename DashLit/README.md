# DashLit

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### DashLit
- Créer le dossier "**dashlit**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/dashlit
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/dashlit
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/DashLit/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier les champs suivant dans le fichier :
	- `ORIGIN`
    - `PASSWORD`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour accéder à l'application : `http://IP:3024`

## Configuration
- Se connecter sur la page web avec le mot de passe renseigner dans le fichier "**docker-compose.yml**".
- Cliquer sur "**Add group**" puis renseigner un titre et une description. Cliquer sur le bouton "**Save**".
- Cliquer sur "**Add item**" puis renseigner les champs suivants :
    - Titre
    - Description
    - L'URL d'accès et comment l'ouvrir
    - Si l'URL doit être afficher ou non
    - L'icône de l'application
- Cliquer sur "**Save**".

- NB : étapes à reproduire pour chaque application et/ou groupe à créer/ajouter !

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f dashlit
```
- Supprimer l'image "**ghcr.io/codewec/dashlit:latest**" présente sur le serveur.
```bash
sudo docker image rm -f ghcr.io/codewec/dashlit:latest
```
- Redémarrer le conteneur.
```bash
cd /docker/dashlit && sudo docker compose up -d
```