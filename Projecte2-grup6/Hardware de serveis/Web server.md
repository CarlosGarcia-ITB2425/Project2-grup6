## Actualizar y actualizar el sistema

`sudo apt upgrade && sudo apt update`

Actualiza la lista de paquetes e instala las versiones más recientes para evitar posibles problemas de compatibilidad.

![sudo apt upgrade and update](/Projecte2-grup6/Imagenes/sudo%20apt%20upgrade%20and%20update.png)

2. Instalar Apache2
text
sudo apt install apache2
Instala el servidor web Apache2 necesario para alojar páginas web en tu máquina.

![install apache2](/Projecte2-grup6/Imagenes/install apache2.png)

3. Iniciar y habilitar Apache2
text
sudo systemctl start apache2
sudo systemctl enable apache2
Inicia y configura Apache2 para que se ejecute automáticamente al arrancar el sistema.

![start and enable apache](/Projecte2-grup6/Imagenes/start and enable apache.png)

4. Verificar el estado de Apache2
text
sudo systemctl status apache2
Comprueba si el servicio de Apache2 está activo y corriendo correctamente.

![status apache2](/Projecte2-grup6/Imagenes/status apache2.png)

5. Editar/crear el archivo principal de la web
text
sudo nano index.html
Crea o edita el archivo principal de la página web dentro del directorio adecuado (habitualmente /var/www/html/).

![sudo nano index html](/Projecte2-grup6/Imagenes/sudo nano index html.png)

6. Añadir contenido HTML a la página
Escribe el contenido que se mostrará en tu página principal.

![contenido html](/Projecte2-grup6/Imagenes/contenido html.png)

7. Visualizar la página HTML en el navegador
Abre tu navegador y accede a la dirección IP o localhost del servidor.

![pagina html](/Projecte2-grup6/Imagenes/pagina html.png)

8. Crear archivo de configuración de VirtualHost
Configura los sitios que alojará Apache, editando o creando un archivo en los sitios disponibles.

![apache sites avaible](/Projecte2-grup6/Imagenes/apache sites avaible.png)

9. Habilitar el sitio con a2ensite
text
sudo a2ensite tu_config.conf
Activa la configuración de tu sitio virtual (reemplaza tu_config.conf por el nombre real del archivo de configuración).

10. Reiniciar Apache2
text
sudo systemctl restart apache2
Reinicia Apache2 para aplicar la nueva configuración de los sitios.

![restart apache2](/Projecte2-grup6/Imagenes/restart apache2.png)

11. Recargar configuración de Apache2
text
sudo systemctl reload apache2
Recarga la configuración de Apache2 para que los cambios en configuraciones menores surtan efecto sin un reinicio completo.

![reload apache2](/Projecte2-grup6/Imagenes/reload apache2.png)

12. Instalar módulo PHP para Apache2
text
sudo apt install libapache2-mod-php
Instala el módulo para que Apache2 procese páginas PHP.

![install libapache](/Projecte2-grup6/Imagenes/install libapache.png)

13. Crear archivo PHP de prueba
text
sudo nano info.php
Crea el archivo PHP dentro del directorio del sitio para comprobar que PHP funciona.

![info php](/Projecte2-grup6/Imagenes/info php.png)

14. Añadir código PHP a info.php
Incluye funciones básicas de PHP para comprobar que el módulo está correctamente instalado.

![contenido php](/Projecte2-grup6/Imagenes/contenido php.png)

15. Visualizar la página PHP en el navegador
Abre tu navegador y accede a la ruta /info.php en tu servidor para comprobar la salida de PHP.

![pagina php](/Projecte2-grup6/Imagenes/pagina php.png)


