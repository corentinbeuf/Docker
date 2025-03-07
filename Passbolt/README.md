# Passbolt
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### Passbolt
- Créer le dossier "**passbolt**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/passbolt
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/passbolt
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Passbolt/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier les champs suivants dans le fichier :
	- `MYSQL_PASSWORD`
	- `DATASOURCES_DEFAULT_PASSWORD`
  - `EMAIL_DEFAULT_FROM_NAME`
  - `EMAIL_DEFAULT_FROM`
  - `EMAIL_TRANSPORT_DEFAULT_HOST`
  - `EMAIL_TRANSPORT_DEFAULT_PORT`
  - `EMAIL_TRANSPORT_DEFAULT_USERNAME`
  - `EMAIL_TRANSPORT_DEFAULT_PASSWORD`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Créer un utilisateur avec les droits **administrateur**.
```bash
sudo docker compose -f /docker/passbolt/docker-compose.yml exec passbolt su -m -c "/usr/share/php/passbolt/bin/cake passbolt register_user -u admin@example.com -f Admin -l Example -r admin" -s /bin/sh www-data
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:8010`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour