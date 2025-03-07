# PHPipam
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### PHPipam
- Créer le dossier "**phpipam**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/phpipam
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/phpipam
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/PHPipam/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:8010`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour