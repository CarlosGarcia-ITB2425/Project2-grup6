## Configuración Netplan

`sudo nano /etc/netplan/00-installer-config.yaml`

Este archivo permite definir la configuración de red en Ubuntu a través de Netplan. Aquí se asignan interfaces, se habilita DHCP o direcciones fijas y se distinguen segmentos como NAT, intranet y DMZ.

![netplan2](/Projecte2-grup6/Imagenes/netplan2.png)

## Comprobar iptables

`sudo iptables -L -v -n`

Se muestran las reglas activas del firewall iptables y se puede analizar el tráfico permitido o bloqueado en el sistema.

![comprobarIPtables5](/Projecte2-grup6/Imagenes/comprobarIPtables5.jpg)

## Conexión por SSH

`ssh usuario@ip_del_servidor`

Ejemplo de conexión SSH a un servidor remoto con autenticación y mensajes de bienvenida en Ubuntu.

![connexioSSH8](connexioSSH8.jpg)

## Instalación de SSH
bash
sudo apt install ssh-server
sudo apt-get install openssh-server
Muestra comandos para instalar el servicio SSH y luego cómo comprobar su estado.

text
![instalarSSH6](instalarSSH6.jpg)
Estado del servicio SSH
bash
sudo systemctl status ssh
Verifica el estado y funcionamiento del servicio OpenSSH para acceso remoto seguro.

text
![serveiSSH7](serveiSSH7.jpg)
Comprobación de interfaces de red y direcciones IP
bash
ip a
Se listan las interfaces de red disponibles y sus direcciones IP, para verificar la configuración de red activa.

text
![IPa3](IPa3.jpg)
Reglas avanzadas de iptables
bash
sudo iptables -A FORWARD ...
sudo iptables -A POSTROUTING ...
sudo apt install iptables-persistent -y
Ejemplo de reglas para controlar el encaminamiento, NAT y persistencia en iptables.

text
![iptables4](iptables4.jpg)
Información de tarjeta de red (Virtualización)
Sin comando directo, visualización web/GUI.
Muestra detalles de las tarjetas de red y configuraciones de virtualización (WireGuard, MAC, etc) útiles en entornos virtualizados o laboratorio.

text
![tarjetared1](tarjetared1.jpg)
