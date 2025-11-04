## Instalación de MySQL Server
sudo apt install -y mysql-server

## Habilitar y arrancar servicio MySQL
sudo systemctl enable --now mysql

## Verificar estado de MySQL
sudo systemctl status mysql --no-pager

## Acceso a MySQL con usuario bchecker
mysql -u bchecker -p
