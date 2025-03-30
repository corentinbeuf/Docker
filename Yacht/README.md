# Yacht

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### Yacht
- Créer le dossier "**yacht**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/yacht
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/yacht
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Yacht/docker-compose.yml > docker-compose.yml
```
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:8000`

## Configuration
- Se connecter avec les identifiants par défaut :
    - Nom d'utilisateur : *admin@yacht.local*
    - Mot de passe : *pass*

### Changement du mot de passe
- Une fois connecté, cliquer sur le compte en haut à droite puis cliquer sur "**User**".
- Cliquer sur l'onglet "**Change password**".
- Renseigner et confirmer le nouveau mot de passe puis cliquer sur "**Chnage user info**".

## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f yacht
```
- Supprimer l'image "**selfhostedpro/yacht**" présente sur le serveur.
```bash
sudo docker image rm -f selfhostedpro/yacht
```
- Redémarrer le conteneur.
```bash
cd /docker/yacht && sudo docker compose up -d
```