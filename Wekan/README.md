# Wekan
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### Wekan
- Créer le dossier "**wekan**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/wekan
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/wekan
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Wekan/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Quand le conteneur se créé, nous visualisons dans les logs qu'il manque des permissions surles dossiers de Wekan.
- Donner tous les droits sur le dossier "assets".
```bash
sudo chmod -R 777 wekan-*/
```
- Redémarrer le conteneur.
```bash
docker compose restart
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour