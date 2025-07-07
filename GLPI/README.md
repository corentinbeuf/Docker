# GLPI
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### GLPI
- Créer le dossier "**glpi**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/glpi
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/glpi
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/GLPI/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier les champs suivants dans le fichier :
	- `MYSQL_ROOT_PASSWORD`
	- `MYSQL_PASSWORD`
	- `VERSION_GLPI`
	- `TIMEZONE`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:8090`

## Configuration
### Première installation
- Se rendre sur la page web.
- Sélectionner la langue puis cliquer sur "**OK**".
- Cliquer sur "**Continuer**".
- Cliquer sur "**Installer**".
- Cliquer sur "**Continuer**".
- Renseigner les informations suivantes pour la connexion à la base de données :
    - Serveur SQL : **mysql**
    - Utilisateur SQL : **glpi_user**
    - Mot de passe SQL : *renseigner votre mot de passe*
- Cliquer sur "**Continuer**".
- Sélectionner la base de données puis cliquer sur "**Continuer**".
- Une fois la base de données initialisée, cliquer sur "**Continuer**".
- Désactiver l'envoi de données puis cliquer sur "**Continuer**".
- Cliquer sur "**Continuer**".
- Cliquer sur "**Utiliser GLPI**".
- Se connecter avec les comptes par défaut.

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f mysql glpi
```
- Supprimer l'image "**diouxx/glpi**" présente sur le serveur.
```bash
sudo docker image rm -f diouxx/glpi
```
- Redémarrer le conteneur.
```bash
cd /docker/glpi && sudo docker compose up -d
```