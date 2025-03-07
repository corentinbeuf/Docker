# Web Check
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### Web Check
- Créer le dossier "**webcheck**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/webcheck
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/webcheck
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl https://raw.githubusercontent.com/corentinbeuf/Docker/main/Web%20check/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour accéder à l'application : `http://IP:3000`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour