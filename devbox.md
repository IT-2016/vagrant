# Information supplémentaire sur la DEVBOX

## Configuration serveur Apache

Le serveur Apache est configuré pour capter un site web avec l'adresse `www.project.dev`
Le DocumentRoot du serveur Apache est configuré pour aller dans un dossier src/public dans votre projet

Commande pour créer les dossiers :

`mkdir -p /var/www/project/src/public`

## Configuration interpréteur PHP

PHP n'est pas configuré pour afficher les messages d'erreurs.

`sudo nano -c /etc/php5/apache2/php.ini`

Ligne 480 > `display_errors = On`

Ligne 491 > `display_startup_errors = On`

Redémarrer le serveur

`sudo service apache2 restart`
