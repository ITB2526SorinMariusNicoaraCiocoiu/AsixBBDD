# AsixBBDD
# Comprobamos que tenemos docker
docker

# Instalamos una base de datos llamada "sorin2"
docker run --name sorin2 -p3307:3306 -e MYSQL_ROOT_PASSWORD=1234 -d mysql:latest

docker ps

# Instalamos el phpmyadmin en el puerto 8080:80
docker run --name my-phpmyadmin -d --link sorin2:db -p 8080:80 phpmyadmin/phpmyadmin

docker ps
