# Portainer
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)

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
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Portainer/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `https://IP:9443`

## Configuration
- Se rendre sur la page web.
- Créer un compte administrateur pour la plateforme.
- Connecter votre environnement Docker en cliquant sur "**Get Started**".

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f portainer
```
- Supprimer l'image "**portainer/portainer-ce:latest**" présente sur le serveur.
```bash
sudo docker image rm -f portainer/portainer-ce:latest
```
- Redémarrer le conteneur.
```bash
cd /docker/portainer && sudo docker compose up -d
```
