# Kuvasz
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Kuvasz
- Créer le dossier "**kuvasz**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/kuvasz
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/kuvasz
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Kuvasz/docker-compose.yml > docker-compose.yml
```
- Télécharger le fichier **kuvasz.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Kuvasz/kuvasz.yml > kuvasz.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier les champs suivants dans le fichier :
	- `POSTGRES_PASSWORD`
	- `DATABASE_PASSWORD`
	- `ADMIN_USER`
	- `ADMIN_PASSWORD`
    - `ADMIN_API_KEY`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Editer le fichier kuvasz.yml.
```bash
sudo nano kuvasz.yml
```
- Modifier les champs suivants dans le fichier :
	- `smtp-config.host`
	- `smtp-config.username`
	- `smtp-config.password`
	- `from-address`
    - `to-address`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:4080`

## Configuration
- Se connecter avec les identifiants renseigner dans le fichier "**docker-compose.yml**" puis cliquer sur "**Sign In**".
- Cliquer sur "**New monitor**".
- Renseigner les champs suivants :
    - Name
    - URL
    - Activer "**SSL certificate check**" et définir la durée de validité du certificat.
    - Cocher la notifications par email.
- Cliquer sur "**Save**".

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f kuvasz
```
- Supprimer l'image "**kuvaszmonitoring/kuvasz:latest**" présente sur le serveur.
```bash
sudo docker image rm -f jkuvaszmonitoring/kuvasz:latest
```
- Redémarrer le conteneur.
```bash
cd /docker/kuvasz && sudo docker compose up -d
```