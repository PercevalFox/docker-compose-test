#  docker-compose-test
# version: '3'
# services:
#  db:
#    image: mysql:5.7                       # Image source du container
#    volumes:                               # Point de Montage entre le container et l'hôte
#      - db_data:/var/lib/mysql
#    restart: always                        # Comportement en cas d'arrêt du processus
#    environment:                           # Variables d'environnement
#      MYSQL_ROOT_PASSWORD: somewordpress
#      MYSQL_DATABASE: wordpress
#      MYSQL_USER: wordpress
#      MYSQL_PASSWORD: wordpress
    
#  wordpress:
#    depends_on:                            # Depend de "db"
#      - db
#    image: wordpress:latest                # Image source du container
#   ports:
#      - "8000:80"
#    restart: always                        # Comportement en cas d'arrêt du processus
#    environment:                           # Variables d'environnement
#      WORDPRESS_DB_HOST: db:3306
#      WORDPRESS_DB_USER: wordpress
#      WORDPRESS_DB_PASSWORD: wordpress
#      WORDPRESS_DB_NAME: wordpress

# volumes:                                  # Point de Montage entre le container et l'hôte
#  db_data: {}
