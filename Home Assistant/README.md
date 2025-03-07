# Home Assistant
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

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


## Sauvegarde

## Restauration

## Mise à jour