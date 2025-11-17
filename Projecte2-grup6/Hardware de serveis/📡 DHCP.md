
## Instalación del paquete ISC DHCP Server

Para instalar el servidor DHCP en tu sistema, ejecuta el siguiente comando en la terminal:

`sudo apt install isc-dhcp-server -y`

Este comando descargará y configurará automáticamente el paquete junto a sus dependencias.

![Instalación isc-dhcp-server](/Projecte2-grup6/Imagenes/luka%20dhcp.png)

---

## Edición del archivo de configuración por defecto

Abre y edita el archivo principal de configuración para definir sobre qué interfaz trabajará el servidor DHCP. Usa el siguiente comando:

`sudo nano /etc/default/isc-dhcp-server`

Solamente tendrás que especificar el nombre de la interfaz en la que quieres que el servicio escuche, por ejemplo:

INTERFACESv4="enp3s0"
INTERFACESv6=""

![Configuración interfaz isc-dhcp-server](/Projecte2-grup6/Imagenes/luka%20dhcp%202.png)

