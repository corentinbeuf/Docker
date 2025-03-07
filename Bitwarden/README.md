# Bitwarden
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### Bitwarden
- Créer le dossier "**bitwarden**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/bitwarden
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/bitwarden
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Bitwarden/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier les champs suivants dans le fichier :
	- `SMTP_HOST`
	- `SMTP_FROM`
	- `SMTP_PORT`
  - `SMTP_SECURITY`
  - `SMTP_USERNAME`
  - `SMTP_PASSWORD`
  - `DOMAIN`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:8010`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour