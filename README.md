# Welcome to Docker

This is a repo for new users getting started with Docker.

You can try it out using the following command.
```
docker run -d -p 8088:80 --name welcome-to-docker docker/welcome-to-docker
```
And open `http://localhost:8088` in your browser.

# Building

Maintainers should see [MAINTAINERS.md](MAINTAINERS.md).

Build and run:
```
docker build -t welcome-to-docker . 
docker run -d -p 8088:3000 --name welcome-to-docker welcome-to-docker
```
Open `http://localhost:8088` in your browser.

# Welcome to Docker
Ce repos a pour but de voir les commandes de docker 

# Liste des commandes :

### Pour vérifier la version d'installation de docker avec la commande :

```
wsl --update
```

![Resultat](image/1.png)

---------------------------------------------------------------------------------------------

### Pour afficher des informations détaillées sur l'installation Docker :

```
docker info
```
<p align="center">
  <img src="image/2.png" width="200"/>
  <img src="image/3.png" width="200"/>
  <img src="image/4.png" width="200"/>
</p>

---------------------------------------------------------------------------------------------

### Pour afficher la liste des conteneurs Docker en cours d'exécution :

```
docker ps
```
Resultat :
![Resultat](image/5.png)

---------------------------------------------------------------------------------------------

### Pour afficher la liste de toutes les images Docker présentes sur le système local :

```
docker images
```
Resultat :
![Resultat](image/6.png)

---------------------------------------------------------------------------------------------

### Pour lancer un conteneur Docker à partir d'une image:

```
docker run
```
Resultat :
![Resultat](image/7.png)

Pour corrigé l'erreur il faut rajouté le nom d'un container apres le run exemple : 

```
docker run [nom du container]
```
Resultat :
![Resultat](image/8.png)

### Bonus :

On peut mettre un nom personalisé pour nos container et ça rends plus simple de les gerés
![Resultat](image/bonus1.png)

---------------------------------------------------------------------------------------------

### Pour arreter un ou plusieurs conteneurs :

```
docker stop
```
Resultat :
![Resultat](image/9.png)

Pour corrigé l'erreur il faut rajouté le nom d'un container apres le stop exemple : 

```
docker stop [nom du container]
```
Resultat :
![Resultat](image/10.png)


    ---------------------------------------------------------------------------------------------

### Pour télécharger des images Docker depuis dockerhub :

```
docker pull
```
Resultat :
![Resultat](image/11.png)

Pour corrigé l'erreur il faut rajouté le nom d'un container apres le pull exemple : 

```
docker pull [nom de l'image]
```
Resultat :
![Resultat](image/12.png)

### Bonus :

On peut aussi choisir la version qu'on veut :
![Resultat](image/bonus2.png)


