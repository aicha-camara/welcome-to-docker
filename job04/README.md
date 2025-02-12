# Welcome-to-docker - JOB 04

On va créer notre premier Dockerfile pour générer un environnement Apache :

Pour cela, nous avons besoin d'un fichier index.php qui affichera les informations du serveur :
![resultat](image/1.png)

Ensuite, je vais créer mon fichier Dockerfile avec les configurations nécessaires.
![resultat](image/2.png)

## Creation de l'image et du container

Après, on doit construire l'image et lancer le container avec :

### l'image :
```
docker build -t apache . 
```
![resultat](image/3.png)
### le container:
```
docker run -d -p 8080:80 apache . 
```

![resultat](image/4.png)

Après son lancement, je peux accéder au site et voici ce que j'obtiens :
![resultat](image/5.png)

Du coup, pour l'arrêter, j'utilise cette commande :

![resultat](image/6.png)