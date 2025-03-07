# Nextcloud
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

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


## Sauvegarde

## Restauration

## Mise à jour