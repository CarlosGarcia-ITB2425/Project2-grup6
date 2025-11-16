## Crear usuario bchecker

`sudo adduser bchecker`

Crea el usuario "bchecker" y define sus datos básicos.

![adduserbchecker(Linux)](adduserbchecker-Linux.jpg) 

## Asignar permisos sudo a bchecker

`sudo usermod -aG sudo bchecker`

Añade el usuario al grupo "sudo" para permitirle ejecutar comandos administrativos.

![Permisosuser(Linux)](Permisosuser-linux.jpg)

## Instalar Apache2

`sudo apt install apache2`

Instala el servidor web Apache2 para alojar páginas web.

![ApacheFuncionando(Linux)](ApacheFuncionando-Linux.jpg)

## Acceso a Apache desde navegador

Prueba que Apache funciona accediendo a la IP del servidor desde el navegador.

![ConectandoApache(Linux)](ConectandoApache-Linux.jpg)

## Pruebas de conectividad con ping

`ping <IPDestino>`

Verifica la conectividad entre distintos hosts de la red local.

![Conectividad(Linux)](Conectividad-Linux.jpg)

## Ver la IP y configuración de red

`ip a`

Muestra la conf. de red y IP actual de la máquina.

![Ip(Linux)](Ip-Linux.jpg)

## Instalación y activación del servicio SSH

`sudo apt install -y openssh-server`

`sudo systemctl enable --now ssh`

Instala y activa el servicio SSH.

![SSHacitvo(Linux)](SSHacitvo-Linux.jpg)

## Generar clave SSH

`ssh-keygen -t ed25519 -N "" -f ~/.ssh/id_ed25519`

Genera pares de claves ED25519 para autenticación segura por SSH.

![SSHkey(Linux)](SSHkey-Linux.jpg)

## Actualizar e instalar OpenSSH Server

`sudo apt update`

`sudo apt install -y openssh-server`

Actualiza el sistema y luego instala OpenSSH Server.

![UpdateyInstallSSH(Linux)](UpdateyInstallSSH-Linux.jpg)
