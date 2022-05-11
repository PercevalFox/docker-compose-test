# Wordpress_Perceval

## Informations concernant les commandes : 

### image = Image source du container  

Pour cet exemple : mysql:5.7 et wordpress:latest

### volumes = Point de Montage entre le container et l'hôte  

Pour cet exemple :  db_data:/var/lib/mysql

### restart = Comportement en cas d'arrêt du processus  

Pour cet exemple : always (signifie qu'il redémarre automatiquement en cas d'arrêt)

### environment = Variables d'environnement 

Pour cet exemple :  
> MYSQL_ROOT_PASSWORD: secret  
> MYSQL_DATABASE: wp1  
> MYSQL_USER: user_wp1  
> MYSQL_PASSWORD: secret2  

et 

> WORDPRESS_DB_HOST: db:3306  
> WORDPRESS_DB_USER: fox  
> WORDPRESS_DB_PASSWORD: secret3  
> WORDPRESS_DB_NAME: wp1  

### depends_on = Depend d'un service 

Pour cet exemple : "db"  
Signifie qu'il dépend du service "db" qui contient l'image mysql:5.7 qui redémarre auto en cas d'exctinction  
que son volume se situe ici : /var/lib/mysql et fonctionne avec l'environnement qui contient "MYSQL_#"

## Accès : 

http://127.0.0.1:8000 
