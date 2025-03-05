# Docuseal
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### Docuseal
- Créer le dossier "**docuseal**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/docuseal
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/docuseal
```
- Télécharger le fichier **docker-compose.yml** fournit par les développeurs.
```bash
sudo curl https://raw.githubusercontent.com/docusealco/docuseal/master/docker-compose.yml > docker-compose.yml
```
- Editer le fichier **docker-compose.yml**.
```bash
sudo nano docker-compose.yml
```
- Modifier les champs suivants dans le fichier :
	- `POSTGRES_USER`
  - `POSTGRES_PASSWORD`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pous sauvegarder puis quitter le fichier.
- Démarrer le conteneur en spécifiant l'URL d'accès.
```bash
HOST=docuseal.cbf.lan docker compose up -d
```
- Se connecter sur l'adresse suivante pour accéder à l'application : `http://docuseal.cbf.lan:3000`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour