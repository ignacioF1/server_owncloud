BIENVENIDO

ownCloud es un software de sincronización e intercambio de archivos de manera segura, en servidores que controlamos, en nuestro caso de forma local.
Se pueden compartir archivos y carpetas y sincronizarlas con el servidor de ownCloud y disponer de ellas/os en el cliente de sincronización para escritorio o aplicaciones para Android o iOS.

Con este archivo de docker-compose, preparamos de cero un ambiente con containers que contienen todos los servicios para que ownCloud funcione y preste servicio web local.


1. Clonar el directorio server_owncloud del repositorio GitHub

git clone https://github.com/echiseall/server_owncloud.git

2. Editar el archivo de configuracion .env con los datos de usuario y contraseña deseados

vim .env

"

OWNCLOUD_VERSION=10.8

OWNCLOUD_DOMAIN=localhost:80

ADMIN_USERNAME=usuario

ADMIN_PASSWORD=contrasena

HTTP_PORT=80


"

3. Poner en marcha el container

docker-compose up -d

4. Comprobar que todos los contenedores se han iniciado correctamente

docker-compose ps

5. Deberá ver una salida similar a la siguiente:

 ![image](https://user-images.githubusercontent.com/90971034/142946481-00009eb4-db62-4d49-bcc3-d2c1d00c45d1.png)


6. Iniciar sesión abriendo en el navegador el puerto 80 y completando los datos ingresados en el .env 
 
http://localhost:80


