## Actualizar y actualizar el sistema

`sudo apt upgrade && sudo apt update`

Actualiza la lista de paquetes e instala las versiones más recientes para evitar posibles problemas de compatibilidad.

![sudo apt upgrade and update](/Projecte2-grup6/Imagenes/sudo%20apt%20upgrade%20and%20update.png)

## Instalar Apache2

`sudo apt install apache2`

Instala el servidor web Apache2 necesario para alojar páginas web en la máquina.

![install apache2](/Projecte2-grup6/Imagenes/install%20apache2.png)

## Iniciar y habilitar Apache2

`sudo systemctl start apache2`

`sudo systemctl enable apache2`

Inicia y configura Apache2 para que se ejecute automáticamente al arrancar el sistema.

![start and enable apache](/Projecte2-grup6/Imagenes/start%20and%20enable%20apache.png)

## Verificar el estado de Apache2

`sudo systemctl status apache2`

Comprueba si el servicio de Apache2 está activo y corriendo correctamente.

![status apache2](/Projecte2-grup6/Imagenes/status%20apache2.png)

## Editar/crear el archivo principal de la web

`sudo nano index.html`

Crea o edita el archivo principal de la página web dentro del directorio adecuado (habitualmente /var/www/html/).

![sudo nano index html](/Projecte2-grup6/Imagenes/sudo%20nano%20index%20html.png)

## Añadir contenido HTML a la página

Aqui se escribe el contenido que se mostrará en tu página principal.

![contenido html](/Projecte2-grup6/Imagenes/contenido%20html.png)

## Visualizar la página HTML en el navegador

Imagen de la página web en el navegador accediendo con la dirección IP del servidor.

![pagina html](/Projecte2-grup6/Imagenes/pagina%20html.png)

## Crear archivo de configuración de VirtualHost

Configura los sitios que alojará Apache, editando o creando un archivo en los sitios disponibles.

![apache sites avaible](/Projecte2-grup6/Imagenes/apache%20sites%20avaible.png)

## Habilitar el sitio con a2ensite

`sudo a2ensite tu_config.conf`

Activa la configuración de tu sitio virtual (reemplaza tu_config.conf por el nombre real del archivo de configuración).

![install a2nsite](/Projecte2-grup6/Imagenes/a2nsite.png)

## Reiniciar Apache2

`sudo systemctl restart apache2`

Reinicia Apache2 para aplicar la nueva configuración de los sitios.

![restart apache2](/Projecte2-grup6/Imagenes/restart%20apache2.png)

## Recargar configuración de Apache2

`sudo systemctl reload apache2`

Recarga la configuración de Apache2 para que los cambios en configuraciones menores surtan efecto sin un reinicio completo.

![reload apache2](/Projecte2-grup6/Imagenes/reload%20apach2.png)

## Instalar módulo PHP para Apache2

`sudo apt install libapache2-mod-php`

Instala el módulo para que Apache2 procese páginas PHP.

![install libapache](/Projecte2-grup6/Imagenes/install%20libapache.png)

## Crear archivo PHP de prueba
    
`sudo nano info.php`

Crea el archivo PHP dentro del directorio del sitio para comprobar que PHP funciona.

![info php](/Projecte2-grup6/Imagenes/info%20php.png)

## Añadir código PHP a info.php

Incluye funciones básicas de PHP para comprobar que el módulo está correctamente instalado.

![contenido php](/Projecte2-grup6/Imagenes/contenido%20php.png)

## Visualizar la página PHP en el navegador

Desde el navegador accede a la ruta /info.php en el servidor para comprobar la salida de PHP.

![pagina php](/Projecte2-grup6/Imagenes/pagina%20php.png)


