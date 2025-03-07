# PHPldapadmin
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### PHPldapadmin
- Créer le dossier "**phpldapadmin**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/phpldapadmin
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/phpldapadmin
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/PHPldapadmin/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier les champs suivants dans le fichier :
	- `LDAP_HOST`
	- `LDAP_BASE_DN`
	- `LDAP_LOGIN_DN`
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