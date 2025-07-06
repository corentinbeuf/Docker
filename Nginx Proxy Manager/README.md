# Nginx Proxy Manager
Your content here

## Présentation

## Installation
### Docker
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/Docker/install_docker.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)

### MySQL
- [Script d'installation](https://raw.githubusercontent.com/corentinbeuf/Bash/refs/heads/main/MySQL/install_mysql.sh)
- [Documentation officiel](https://docs.docker.com/engine/install/)
- Se connecter à MySQL en ligne de commande.
```bash
mysql -u root -p
```
- Créer la base de données "**npm**".
```sql
CREATE DATABASE npm;
```
- Créer l'utilisateur "**npm**".
```sql
CREATE USER 'npm'@'%' IDENTIFIED WITH mysql_native_password BY 'le_mot_de_passe';
```
- Donner les droits à l'utilisateur "**npm**" sur la base de données du même nom.
```sql
GRANT ALL ON *.* TO 'npm'@'%';
```
- Recharger les permissions.
```sql
FLUSH PRIVILEGES;
```
- Quitter MySQL.
```sql
quit
```

### Nginx Proxy Manager
- Créer le dossier "**npm**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/npm
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/npm
```
- Télécharger le fichier **docker-compose.yml**.
```bash
sudo curl 
https://raw.githubusercontent.com/corentinbeuf/Docker/main/Nginx%20Proxy%20Manager/docker-compose.yml > docker-compose.yml
```
- Editer le fichier docker-compose.yml.
```bash
sudo nano docker-compose.yml
```
- Modifier les champs suivants dans le fichier :
	- `DB_MYSQL_HOST`
	- `DB_MYSQL_USER`
	- `DB_MYSQL_PASSWORD`
	- `DB_MYSQL_NAME`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pour sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour créer son compte et accéder à l'application : `http://IP:81`

## Configuration
- Se connecter avec les identifiants par défaut :
	- Email address : **admin@example.com**
	- Password : **changeme**
- Cliquer sur "**Sign In**".
- Renseigner les bonnes informations pour le compte d'administration. Cliquer sur "**Save**".
- Changer le mot de passe par défaut. Cliquer sur "**Save**".

### Proxy Hosts
- Cliquer sur l'onglet "**Hosts**" puis sur "**Proxy Hosts**".
- Cliquer sur "**Add Proxy Hosts**".
- Renseigner les champs suivants :
	- Domain Names
	- Scheme
	- Forward Hostname / IP
	- Forward Port
	- Pour séléectionner un certificat, aller dans l'onglet **SSL**
	- Pour faire une réécriture d'URL, aller dans l'onglet **Advanced**
- Cliquer sur Save.


## Sauvegarde
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Restauration
- Voir la documentation sur le repository [Docker](https://github.com/corentinbeuf/Bash/blob/main/Docker/README.md)

## Mise à jour
- Supprimer le conteneur en cours d'exécution.
```bash
sudo docker rm -f reverseproxy
```
- Supprimer l'image "**jc21/nginx-proxy-manager:latest**" présente sur le serveur.
```bash
sudo docker image rm -f jc21/nginx-proxy-manager:latest
```
- Redémarrer le conteneur.
```bash
cd /docker/npm && sudo docker compose up -d
```