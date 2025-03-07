# BackupPC
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### BackupPC
- Créer le dossier "**backuppc**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/backuppc
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/backuppc
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/BackupPC/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour