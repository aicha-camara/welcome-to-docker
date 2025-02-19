# Welcome-to-docker - Symphony  

## ETAPE A :

### Étape 1 : Préparer l'environnement

- Je verifie si docker et docker compose sont installer avec `docker --version` et `docker-compose version`. Comme il y'a pas de message d'erreur ça veut dire qu'ils sont bien installer.
![resultat](image/2.png)
![resultat](image/3.png)

- Je verifie si composer et symphony sont installer avec `composer --version` et ` symfony --version`. J'ai bien composer installer mais pas symphony du coup je vais installé `scoop` pour utilisé une commande qui installe symphony:

    1. J'installe scoop depuis le terminal de powershell :
    ![resultat](image/4.png)

    2. J'installe symphony avec la commande scoop: 
    ![resultat](image/5.png)

    3. Je verifie que symphony est bien installer
    ![resultat](image/6.png)

---

### Étape 2 : Créer un dossier de projet

- Je vais creer un répertoire pour le projet Symfony et je le nomme
“UNIT_SYMFONY” qui hébergera le readme et les autres dossiers du projet,normalement on peut le faire directement avec composer mais comme sur mon ordinateur jai pas php a jour je vais devoir creer une image puis un container
 
![resultat](image/7.png)

---

### Étape 3 : Préparer le fichier Docker Compose

Voici notre fichier Docker compose :
![resultat](image/8.png)


Notre fichier `docker-compose.yml` liste tous les services dont on a besoin et les répertorie dans une variable appelée services. À l'intérieur, on a :

1. Le service `app` qui utilise l'image `php:8.2-fpm`, puis crée un conteneur nommé `symfony_app`. Il définit le répertoire de travail du conteneur à `/var/www/html`, et crée un volume à ce chemin `./app:/var/www/html`. Enfin, le service sera connecté à un réseau Docker nommé `symfony_network`."

2. Le service `webserver` utilise l'image `nginx:stable`, puis crée un conteneur nommé `symfony_webserver`. Il expose le port `8080` sur l'hôte pour le rediriger vers le port `80` du conteneur. Ensuite, il crée deux volumes : l'un pour lier le répertoire `./app de l'hôte` à `/var/www/html` dans le conteneur, et l'autre pour lier le répertoire `./nginx` de l'hôte à `/etc/nginx/conf.d` dans le conteneur. Le service dépend du service `app`, ce qui signifie qu'il sera lancé uniquement après que le service `app` soit démarré. Enfin, le service sera connecté à un réseau Docker nommé `symfony_network`.





2. Expliquez dans le readme du dossier projet ce qu’il fait ligne par ligne
2. Créer un fichier de configuration Nginx
Créez un dossier nginx et un fichier default.conf avec le contenu
approprié fournis en annexe.
3. Expliquez dans le readme du dossier projet ce qu’il fait ligne par ligne
4. Créer un fichier dockerfile avec le contenu approprié fournis en
annexe.
5. Expliquez dans le readme du dossier projet ce qu’il fait ligne par ligne