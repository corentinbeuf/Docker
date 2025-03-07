# Vaultwarden
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### MySQL 
- [MySQL](/documentation/linux/mysql)
{.links-list}

### Vaultwarden
- Créer le dossier "**vaultwarden**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/vaultwarden
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/vaultwarden
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Vaultwarden/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier le champ suivant dans le fichier :
	- `DATABASE_URL`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:8020`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour