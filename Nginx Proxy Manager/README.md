# Nginx Proxy Manager
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### MySQL
- [MySQL](/documentation/linux/mysql)
{.links-list}

### Nginx Proxy Manager
- Créer le dossier "**npm**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/npm
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/npm
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Nginx%20Proxy%20Manager/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier les champs suivants dans le fichier :
	- `DB_MYSQL_HOST`
	- `DB_MYSQL_USER`
	- `DB_MYSQL_PASSWORD`
	- `DB_MYSQL_NAME`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:81`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour