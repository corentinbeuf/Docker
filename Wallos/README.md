# Wallos
Your content here 

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Wallos
- Créer le dossier "**wallos**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/wallos
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/wallos
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Wallos/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:8282`

## Configuration
- Se créer un compte en renseignant les champs suivants :
    - Username
    - First name
    - Last name
    - Email
    - Password
    - Confirm Password
    - Main Currency
    - Language
- Cliquer sur "**Register**".
- Se connecter avec l'utilisateur créé.
- Cliquer sur "**Ajouter le premier abonnement**".
- Renseigner les informations sur l'abonnement puis cliquer sur "**Enregistrer**".

- NB : étapes à reproduire pour chaque abonnement.


## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f wallos
```
- Supprimer l'image "**bellamy/wallos:latest**" présente sur le serveur.
```bash
sudo docker image rm -f bellamy/wallos:latest
```
- Redémarrer le conteneur.
```bash
cd /docker/wallos && sudo docker compose up -d
```