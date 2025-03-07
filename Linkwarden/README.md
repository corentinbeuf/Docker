# Linkwarden
Your content here

## Présentation

## Installation
### Docker
- [Docker](/documentation/linux/docker)
{.links-list}

### Linkwarden
- Installer **Git**.
```bash
sudo apt-get install git -y
```
- Créer le dossier "**linkwarden**" dans le répertoire "**docker**".
```bash
sudo mkdir /docker/linkwarden
```
- Se rendre dans le dossier créer précédemment.
```bash
cd /docker/linkwarden
```
- Cloner le repository du projet **Linkwarden**.
```bash
sudo git clone https://github.com/linkwarden/linkwarden.git .
```
- Créer un fichier **.env**.
```bash
sudo cp .env.sample .env
```
- Editer le fichier créer précedemment.
```bash
sudo nano .env
```
- Modifier les champs suivants dans le fichier :
	- `NEXTAUTH_URL=http://IP:3000/api/v1/auth`
	- `NEXTAUTH_SECRET=VERY_SENSITIVE_SECRET`
	- `POSTGRES_PASSWORD=CUSTOM_POSTGRES_PASSWORD`
- Faire un "**Ctrl+S**" puis un "**Ctrl+X**" pous sauvegarder puis quitter le fichier.
- Démarrer le conteneur.
```bash
docker compose up -d
```
- Se connecter sur l'adresse suivante pour accéder à l'application : `http://IP:3000`

## Configuration


## Sauvegarde

## Restauration

## Mise à jour