## Instalar MySQL

`sudo apt install mysql-server`

Instala el servidor de bases de datos MySQL usando permisos de administrador. Si el paquete ya está instalado, el sistema lo notificará y mantendrá la versión más reciente.

![Install](Install%20mysql.png)

## Habilitar MySQL

`sudo systemctl enable mysql`

Configura MySQL para que se inicie automáticamente al encender el sistema.

<img width="1002" height="136" alt="image" src="https://github.com/user-attachments/assets/2d341050-186b-42dc-973d-e13f3bcf38f3" />


## Arrancar el servicio inmediatamente y comprobar el estado MySQL.

`sudo systemctl start mysql`

La imagen muestra cómo habilitar y arrancar el servicio MySQL desde la terminal usando los comandos anteriores. El sistema confirma que MySQL se añadirá al arranque automático tras reiniciar y que el servicio se ha iniciado correctamente.

`sudo systemctl status mysql`

Revisa el estado del servicio para verificar si está activo y corriendo sin errores.

<img width="1007" height="471" alt="image" src="https://github.com/user-attachments/assets/4b2c0261-b48c-401f-927b-cd08cfdfd38a" />




