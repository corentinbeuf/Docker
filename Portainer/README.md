# Portainer
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### Portainer
- Créer le dossier "**portainer**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/portainer
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/portainer
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Portianer/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `https://IP:9443`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour