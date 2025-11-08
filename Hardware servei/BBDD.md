## Instalar MySQL

`sudo apt install mysql-server`

Instala el servidor de bases de datos MySQL usando permisos de administrador. Si el paquete ya está instalado, el sistema lo notificará y mantendrá la versión más reciente.

## Habilitar y arrancar MySQL

`sudo systemctl enable mysql`

Configura MySQL para que se inicie automáticamente al encender el sistema.

## Arranca el servicio MySQL inmediatamente.

`sudo systemctl start mysql`

La imagen muestra cómo habilitar y arrancar el servicio MySQL desde la terminal usando los comandos anteriores. El sistema confirma que MySQL se añadirá al arranque automático tras reiniciar y que el servicio se ha iniciado correctamente.

## Comprobar el estado de MySQL

`sudo systemctl status mysql`

Revisa el estado del servicio para verificar si está activo y corriendo sin errores.
