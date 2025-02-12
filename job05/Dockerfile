# Utiliser l'image de base Nginx
FROM nginx:alpine

# Copier les fichiers nécessaires dans le conteneur
COPY index.html /usr/share/nginx/html/
COPY results.json /usr/share/nginx/html/
COPY save.php /usr/share/nginx/html/

# Exposer le port 80 pour Nginx
EXPOSE 80
