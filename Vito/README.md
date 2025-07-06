# Vito

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Vito
- Créer le dossier "**vito**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/vito
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/vito
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Vito/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier le champ suivant dans le fichier :
	- `APP_URL`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour accéder à l'application : `http://IP:9999`

## Configuration
- Editer le fichier "**docker-compose.yml**".
```bash
sudo nano /docker/vito/docker-compose.yml
```
- Modifier le champ suivant dans le fichier, si vous souhaitez que les liens soient accessible plus longtemps :
	- `SECRETS_LIFETIME_IN_MINUTES`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Redémarrer le conteneur pour la bonne prise en compte des modifications.
```bash
docker compose restart vito
```

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f vito
```
- Supprimer l'image "**globusgroup/vito:latest**" présente sur le serveur.
```bash
sudo docker image rm -f globusgroup/vito:latest
```
- Redémarrer le conteneur.
```bash
cd /docker/vito && sudo docker compose up -d
```