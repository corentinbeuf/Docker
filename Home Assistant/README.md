# Home Assistant
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Home Assistant
- Créer le dossier "**homeassistant**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/homeassistant
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/homeassistant
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl https://raw.githubusercontent.com/corentinbeuf/Docker/main/Home%20Assistant/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur en spécifiant l'URL d'accès.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour accéder à l'application : `http://IP:8123`

## Configuration
- Se rendre sur la page web.
- Cliquer sur "**Créer ma maison connectée**".
- Créer un utilisateur puis cliquer sur "**Créer un compte**".
- Renseigner l'emplacement de votre maison puis cliquer sur "**Suivant**".
- Cliquer sur "**Terminer**".

### Ajouter des équipements
- Cliquer sur le bouton "**Paramètres**" dans le menu de gauche.
- Cliquer sur "**Appareils et services**".
- Cliquer sur le bouton "**Ajouter une intégration**".
- Rechercher votre équipemnt puis cliquer dessus.
- Renseigner les informations demandées pour finaliser l'intégration de l'équipement.

### Création de pièces/étages
- Cliquer sur le bouton "**Paramètres**" dans le menu de gauche.
- Cliquer sur "**Pièces, libellés et zones**".
- Cliquer sur le bouton "**Créer un étage**" ou "**Créer une pièce**".

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f homeassistant
```
- Supprimer l'image "**ghcr.io/home-assistant/home-assistant:stable**" présente sur le serveur.
```bash
sudo docker image rm -f ghcr.io/home-assistant/home-assistant:stable
```
- Redémarrer le conteneur.
```bash
cd /docker/homeassistant && sudo docker compose up -d
```