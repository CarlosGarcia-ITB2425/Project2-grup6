
## Instalar BIND9 y utilidades

`sudo apt install bind9 bind9utils -y`

Instala el servicio DNS BIND9 y las utilidades necesarias para la gestión del servidor de nombres.

![Instalación de BIND9](/Projecte2-grup6/Imagenes/instalacion%20de%20dns.png)
​
## Copiar archivos de configuración base

`sudo cp /etc/bind/db.local /etc/bind/db.midominio.local`

Se copia el archivo de zona de ejemplo para crear la zona de tu dominio.

![Copiar archivo db.local](/Projecte2-grup6/Imagenes/sudo%20cp%20db.png)

---

## Crear y editar archivo de zona inversa

`sudo cp /etc/bind/db.127 /etc/bind/db.192.168.6`

`sudo nano /etc/bind/db.192.168.6`

Se crea y edita el archivo de zona inversa para la red interna.

![Copiar y editar archivo de zona inversa](/Projecte2-grup6/Imagenes/sudo%20cp2.png)


Aquí se definen los registros PTR para la resolución inversa:

![Editar archivo de zona inversa](/Projecte2-grup6/Imagenes/bind%20db.png)

---
​
