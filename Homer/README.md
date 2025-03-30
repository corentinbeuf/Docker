# Homer

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

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
- Editer le fichier "**config.yml**".
```bash
sudo nano /docker/homer/assets/config.yml
```
- Modifier le contenu de ce fichier pour modifier la page web.
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Redémarrer le conteneur pour la bonne prise en compte des modifications.
```bash
docker compose restart homer
```

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f homer
```
- Supprimer l'image "**b4bz/homer**" présente sur le serveur.
```bash
sudo docker image rm -f b4bz/homer
```
- Redémarrer le conteneur.
```bash
cd /docker/homer && sudo docker compose up -d
```