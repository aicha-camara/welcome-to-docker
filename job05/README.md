# Welcome-to-docker - JOB 05

On va apprendre a faire des volumes.

# Creation des premier fichiers
 
Apres avoir copier les fichier : index.html , result.json et save.php. Nous allons configuré notre dockerfile

![resultat](image/1.png)

Maintenant on peut creer notre image et notre container et lancer notre page:
![resultat](image/2.png)
![resultat](image/3.png)
![resultat](image/4.png)

# Creation du volume

On va maintenant creer notre volume “game-results” pour stocker les
résultats dans un fichier resuslts.json et le fichier save.php pour cela on va supprimé l'ancien container avec `docker rm tictactoe` en veillant d'avoir eteint le container pui on utilise cette commande qui creer le volume pour un container precis : 
 ```
docker run -d -p 8080:80 -v game-results:/var/www/html --name tictactoe php:7.4-apache 
 ```
 ![resultat](image/5.png)

 Je peux regardé s'il est bien creer avec : 
 ```
 docker volume ls

 ```
![resultat](image/6.png)






