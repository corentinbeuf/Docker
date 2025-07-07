# Homepage
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Homepage
- Créer le dossier "**homepage**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/homepage
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/homepage
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/homepage/Homepage/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier le champ suivant dans le fichier :
	- `HOMEPAGE_ALLOWED_HOSTS`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour accéder à l'application : `http://IP:3000`

## Configuration
- Pour modifier la disposition de la page web, modifier les fichiers de configuration présent dans le dossier "**config**".

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f homepage
```
- Supprimer l'image "**ghcr.io/gethomepage/homepage:latest**" présente sur le serveur.
```bash
sudo docker image rm -f ghcr.io/gethomepage/homepage:latest
```
- Redémarrer le conteneur.
```bash
cd /docker/homepage && sudo docker compose up -d
```