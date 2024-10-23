# SXE_Tarea04
## Angel Jose Piñeiro Andion
### Enunciado:
#### Crear un  fichero (nombre "Readme.md") con formato markdown en un repositorio en github para subir este fichero y hacer commits que indiquen lo realizado.

#### En la respuesta pon el enlace a tu repositorio en github

#### 1. Utiliza la imagen de Ubuntu , tag 22 y apoyandote en esta guía sigue sus instrucciones para instalar LAMP en dicho contenedor.

En primer lugar vamos a descargar la imagen de Ubuntu 22.04 utilizando el siguiente comando:

    docker pull ubuntu:22.04

Una vez descargada la imagen, vamos a crear un contenedor con la misma utilizando el siguiente comando:

    docker container create -i -t --name ubuntu22.04 ubuntu:22.04

Una vez creado el contenedor lo arrancamos con el siguiente comando:

    docker start --attach -i  ubuntu22.04 

Una vez dentro vamos a instalar la pila LAMP siguiendo los siguientes pasos:
1. Actualizamos los paquetes del sistema:

        apt update

2. Instalamos Apache:

        apt install -y apache2 apache2-utils

3. Instalamos mariadb:

        apt install -y mariadb-server mariadb-client

4. Iniciamos maria db, y configuramos la contraseña de root:

        service mariadb start
        mysql_secure_installation

5. Instalamos PHP:
    
         apt install -y php php-mysql libapache2-mod-php

6. Probamos que funciona:

    echo "<?php phpinfo(); ?>" | tee /var/www/html/info.php


#### 2. Utiliza esta guía para instalar wordpress en el contenedor.

#### 3. Comprueba que puedes acceder a wordpress.


#### OPCIONAL: Instala phpmyadmin en el contenedor siguiendo esta guía. Comprueba que puedes acceder.