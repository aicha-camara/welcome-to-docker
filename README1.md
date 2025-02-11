# Welcome to Docker - Part 2

## Le fonctionne d'une image deja créer
GIT
Je vais depuis le terminal aller dans mon dossier où se trouve le projet puis je lance cette commande :
```
docker run -d -p 8088:80 --name welcome-to-docker docker/welcome-to-docker
```
![Resultat](image/20.png)

Je verifie que le container est bien installer et allumer avec :
```
docker ps
```
![Resultat](image/22.png)

On remarque qu'il s'affiche dans le menu et que son statue est up, Maintenant depuis l'url je vais rentrer ceci  `http://localhost:8088` et ça fonctionne

![Resultat](image/23.png)

 ## Creation d'une image

 Pour qu'on puisse faire des modfication de cette page il faudra la suprimé et la recreer pour cela :
 
1. Il faut supprimer le container avec :
     ```
    docker rm welcome-to-docker
    ```
![Resultat](image/24.png)

2. Ensuite on va re-crer l'image :
    ```
    docker build -t welcome-to-docker .
    ```
![Resultat](image/25.png)

3. Puis relancer le container: 
    ```
    docker run -d -p 8088:3000 --name welcome-to-docker welcome-to-docker
    ```
![Resultat](image/26.png)

Et on remarque lorsqu'on retourne dans le site le titre a bien changer
![Resultat](image/27.png)

 ## Publication de notre image

 Pour partagez notre projet il fraudra :

1. Se connecter depuis le terminal
    ```
    docker login
    ```
    ![Resultat](image/28.png)

2. Rajouter un tag à notre image en rajoutant notre pseudo
    ```
    docker tag welcome-to-docker aichaaa/welcome-to-docker:latest
    ```
    ![Resultat](image/29.png)

3. Ensuite envoie tout avec un push
    ```
    docker push aichaaa/welcome-to-docker:latest
    ```
    ![Resultat](image/30.png)
