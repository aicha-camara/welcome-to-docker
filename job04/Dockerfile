# Utiliser une image de base contenant Apache et PHP
FROM php:7.4-apache

# Copier le fichier index.php dans le répertoire de l'Apache
COPY index.php /var/www/html/

# Exposer le port 8080
EXPOSE 8080

# Lancer Apache en mode premier plan pour garder le container actif
CMD ["apache2-foreground"]
