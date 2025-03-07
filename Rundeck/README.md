# Rundeck
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### Rundeck
- Créer le dossier "**rundeck**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/rundeck
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/rundeck
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Rundeck/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:4440`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour