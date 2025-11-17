## Crear usuario FTP

`sudo adduser ftpuser`

Crea el usuario ftpuser que utilizarás para el acceso FTP, asegurándote de usar una contraseña segura y rellenar los campos que necesites.​

![Crear usuario FTP](/Projecte2-grup6/Imagenes/user%20ftp.png)

- - -

## Crear directorios y asignar permisos

`sudo mkdir -p /home/ftpuser/ftp/upload`

`sudo chown -R ftpuser:ftpuser /home/ftpuser/ftp`

Estos comandos crean la estructura de carpetas para el usuario FTP y le asignan la propiedad.​

![Crear directorios y asignar permisos](/Projecte2-grup6/Imagenes/ftp%20mkdir.png)

---
​
## Configurar la lista de usuarios permitidos

`echo "ftpuser" | sudo tee -a /etc/vsftpd.userlist`

Asegúrate de añadir tu usuario a la lista de permitidos en el archivo de configuración.​

![Añadir usuario permitido](/Projecte2-grup6/Imagenes/usuario%20ftp.png)

---​

## Realizar copia de seguridad del archivo de configuración

`sudo cp /etc/vsftpd.conf /etc/vsftpd.conf.orig`

Antes de modificar la configuración, crea una copia de respaldo del archivo original.​

![Backup configuración](/Projecte2-grup6/Imagenes/sudoi%20cp.png)

---​

## Configurar el cortafuegos para FTP

`sudo ufw allow 21/tcp`

`sudo ufw allow 20100:20200/tcp`

Abre el puerto estándar 21 y el rango de puertos pasivos para FTP en el firewall UFW.​

![Firewall FTP](/Projecte2-grup6/Imagenes/ftp%20allow.png)

---​

## Reiniciar el servicio y comprobar estado

`sudo systemctl restart vsftpd && sudo systemctl status vsftpd`

Reinicia el servicio FTP y verifica que esté corriendo correctamente.​

![Estado servicio vsftpd](/Projecte2-grup6/Imagenes/status.png)​
