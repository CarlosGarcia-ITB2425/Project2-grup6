## Configuración Netplan

`sudo nano /etc/netplan/00-installer-config.yaml`

Este archivo permite definir la configuración de red en Ubuntu a través de Netplan. Aquí se asignan interfaces, se habilita DHCP o direcciones fijas y se distinguen segmentos como NAT, intranet y DMZ.

![netplan2](/Projecte2-grup6/Imagenes/netplan2.png)

## Comprobar iptables

`sudo iptables -L -v -n`

Se muestran las reglas activas del firewall iptables y se puede analizar el tráfico permitido o bloqueado en el sistema.

![comprobarIPtables5](/Projecte2-grup6/Imagenes/comprobarIPtables5.png)

## Conexión por SSH

`ssh usuario@ip_del_servidor`

Ejemplo de conexión SSH a un servidor remoto con autenticación y mensajes de bienvenida en Ubuntu.

![connexioSSH8](/Projecte2-grup6/Imagenes/connexioSSH8.png)

## Instalación de SSH

`sudo apt install ssh-server`

`sudo apt-get install openssh-server`

Muestra comandos para instalar el servicio SSH y luego cómo comprobar su estado.

![instalarSSH6](/Projecte2-grup6/Imagenes/instalarSSH6.png)

## Estado del servicio SSH

`sudo systemctl status ssh`

Verifica el estado y funcionamiento del servicio OpenSSH para acceso remoto seguro.

![serveiSSH7](/Projecte2-grup6/Imagenes/serveiSSH7.png)

## Comprobación de interfaces de red y direcciones IP

`ip a`

Se listan las interfaces de red disponibles y sus direcciones IP, para verificar la configuración de red activa.

![IPa3](/Projecte2-grup6/Imagenes/IPa3.png)

## Reglas avanzadas de iptables

`sudo iptables -A FORWARD ...`
`sudo iptables -A POSTROUTING ...`
`sudo apt install iptables-persistent -y`

Ejemplo de reglas para controlar el encaminamiento, NAT y persistencia en iptables.

![iptables4](/Projecte2-grup6/Imagenes/iptables4.png)

## Información de tarjeta de red (Virtualización)

Muestra detalles de las tarjetas de red y configuraciones de virtualización (WireGuard, MAC, etc) útiles en entornos virtualizados o laboratorio.

![tarjetared1](/Projecte2-grup6/Imagenes/tarjetared1.png)
