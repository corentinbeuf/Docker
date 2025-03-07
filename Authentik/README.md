# Authentik
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### Authentik
- Créer le dossier "**authentik**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/authentik
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/authentik
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Authentik/docker-compose.yml > docker-compose.yml
```
- Installer le paquet "**pwgen**".
```bash
sudo apt-get install pwgen -y
```
- Ajouter les champs suivant dans un fichier "**.env**".
```bash
echo "PG_PASS=$(pwgen -s 40 1)" >> .env
echo "AUTHENTIK_SECRET_KEY=$(pwgen -s 50 1)" >> .env
echo "AUTHENTIK_ERROR_REPORTING__ENABLED=true" >> .env
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:9000/if/flow/initial-setup/`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour