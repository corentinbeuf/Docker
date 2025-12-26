# Caddy

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Caddy
- Créer le dossier "**caddy**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/caddy
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/caddy
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Caddy/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP`

## Configuration
- Créer ou copier vos fichiers dans le dossier "**html**" (*/docker/caddy/html*) créer lors du démarrage du conteneur. Le conteneur charge automatiquement le contenu ajouté dans le dossier.

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f caddy
```
- Supprimer l'image "**caddy:2.9.1**" présente sur le serveur.
```bash
sudo docker image rm -f caddy:2.9.1
```
- Editer le fichier "**docker-compose.yml**".
```bash
sudo nano /docker/caddy/docker-compose.yml
```
- Modifier l'étiquette de l'image.
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Redémarrer le conteneur.
```bash
cd /docker/caddy && sudo docker compose up -d
```