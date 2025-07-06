# Web Check
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

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
- Renseigner une URL dans le champ de saisie puis cliquer sur "**Analyse**".

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f webcheck
```
- Supprimer l'image "**lissy93/web-check**" présente sur le serveur.
```bash
sudo docker image rm -f lissy93/web-check
```
- Redémarrer le conteneur.
```bash
cd /docker/webcheck && sudo docker compose up -d
```