# Welcome to Docker - Part 2

Je vais depuis le terminal aller dans mon dossier ou se trouve le projet puis je lance cette commande :
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

![Resultat](image/21.png)