# Welcome-to-docker - JOB 04

On va créer notre premier dockerfile pour générer un environement apache:

Pour cela on a un besoind d' un fichier index.php qui nous affichera les infos du serveur :
![resultat](image/1.png)

Ensuite je vais créer mon fichier dockerfile avec les configurations
![resultat](image/2.png)

## Creation de l'image et du container

Apres on doit build l'image et le container avec :

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

