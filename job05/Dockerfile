# Utiliser l'image officielle PHP avec Apache
FROM php:7.4-apache

# Copier les fichiers du jeu dans le répertoire de l'Apache
COPY index.html /var/www/html/
COPY result.json /var/www/html/
COPY save.php /var/www/html/

# Exposer le port 8080 pour accéder au jeu
EXPOSE 8080

# Démarrer Apache en mode premier plan
CMD ["apache2-foreground"]
