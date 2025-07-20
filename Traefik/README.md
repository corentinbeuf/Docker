# Traefik
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Traefik
- Créer le dossier "**traefik**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/traefik
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/traefik
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Traefik/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:8080`

## Configuration
- Pour chaque application Docker exposant une interface web, rajouter les commandes suivantes dans le fichier "**docker-compose.yml**" :
```yml
labels:
      - "traefik.http.routers.frontend-URL.rule=Host(`www.example.com`)"
      - "traefik.http.routers.frontend-URL.tls.certresolver=cert_cert"
      - "traefik.http.routers.frontend-URL.entrypoints=websecure"
```

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f traefik
```
- Supprimer l'image "**traefik:v2.9**" présente sur le serveur.
```bash
sudo docker image rm -f traefik:v2.9
```
- Editer le fichier "**docker-compose.yml**".
```bash
sudo nano /docker/caddy/docker-compose.yml
```
- Modifier l'étiquette de l'image.
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Redémarrer le conteneur.
```bash
cd /docker/traefik && sudo docker compose up -d
```