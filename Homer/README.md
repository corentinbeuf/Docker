# Homer
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### Homer
- Créer le dossier "**homer**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/homer
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/homer
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Homer/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Quand le conteneur se créé, nous visualisons dans les logs de celui-ci que le dossier "**assets**" manque de permissions.
- Donner tous les droits sur le dossier "assets".
```bash
sudo chmod -R 777 assets/
```
- Redémarrer le conteneur.
```bash
docker compose restart
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:8080`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour