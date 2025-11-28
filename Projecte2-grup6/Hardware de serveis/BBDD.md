Actualizar y actualizar el sistema
bash
sudo apt upgrade && sudo apt update
Actualiza la lista de paquetes e instala las versiones más recientes desde los repositorios de Ubuntu para evitar problemas de compatibilidad del sistema.

Instalar el servidor MySQL
bash
sudo apt install mysql-server
Instala el paquete del servidor MySQL desde los repositorios de Ubuntu para poder crear y gestionar bases de datos en el sistema.

Habilitar y arrancar el servicio MySQL
bash
sudo systemctl enable mysql
sudo systemctl start mysql
sudo systemctl status mysql
Configura MySQL para iniciarse automáticamente con el sistema, lo arranca manualmente y comprueba que el servicio esté activo y en ejecución.

Crear usuario y base de datos bchecker
sql
CREATE USER 'bchecker'@'%' IDENTIFIED BY 'bchecker121';
CREATE DATABASE equipaments_educacio CHARACTER SET utf8mb4;
Crea un usuario dedicado llamado bchecker accesible desde cualquier host y genera la base de datos equipaments_educacio con codificación adecuada para caracteres especiales.

Conceder privilegios al usuario bchecker
sql
GRANT ALL PRIVILEGES ON equipaments_educacio.* TO 'bchecker'@'%';
FLUSH PRIVILEGES;
Otorga al usuario bchecker todos los permisos sobre la base de datos equipaments_educacio y recarga la tabla de privilegios para que los cambios tengan efecto inmediato.

Descargar el CSV de equipaments
bash
wget https://opendata-ajuntament.barcelona.cat/data/.../download -O equipaments.csv
Descarga desde el portal de datos abiertos del Ayuntamiento de Barcelona el fichero equipaments.csv con la información de los equipamientos educativos.

Comprobar el contenido del CSV
bash
head -5 equipaments.csv
Muestra las primeras líneas del archivo CSV para revisar que el separador de campos, encabezados y datos sean correctos antes de importarlos a MySQL.

Crear la tabla equipaments
sql
CREATE TABLE equipaments (
  register_id INT,
  name VARCHAR(200),
  institution_id INT,
  institution_name VARCHAR(200),
  created DATETIME,
  modified DATETIME,
  addresses_roadtype_id INT,
  addresses_roadtype_name VARCHAR(100),
  addresses_road_id INT,
  addresses_road_name VARCHAR(100),
  addresses_start_street_number VARCHAR(20),
  addresses_end_street_number VARCHAR(20),
  addresses_neighborhood_id INT,
  addresses_neighborhood_name VARCHAR(100),
  addresses_district_id INT,
  addresses_district_name VARCHAR(100),
  addresses_zip_code VARCHAR(10),
  addresses_town VARCHAR(100),
  addresses_main_address VARCHAR(200),
  addresses_type VARCHAR(100),
  values_id INT,
  values_attribute_id INT,
  values_category VARCHAR(100),
  values_attribute_name VARCHAR(100),
  values_value INT,
  values_outstanding VARCHAR(100),
  values_description VARCHAR(100),
  secondary_filters_id INT,
  secondary_filters_fullpah VARCHAR(200),
  secondary_filters_tree VARCHAR(200),
  secondary_filters_asia_id INT,
  geo_epsg_25831_x DOUBLE,
  geo_epsg_25831_y DOUBLE,
  geo_epsg_4326_lat DOUBLE,
  geo_epsg_4326_lon DOUBLE
);
Define la estructura de la tabla equipaments con todos los campos necesarios para almacenar direcciones, categorías, atributos y coordenadas geográficas de cada registro.

Ver estructura de la tabla equipaments
sql
DESCRIBE equipaments;
Muestra las columnas de la tabla equipaments con su tipo de dato, si permiten valores nulos y otros detalles útiles para comprobar que la definición es correcta.

Activar la opción local_infile en MySQL
sql
SHOW GLOBAL VARIABLES LIKE 'local_infile';
bash
mysql -u bchecker -p equipaments_educacio --local-infile=1
Comprueba si la variable local_infile está activa y se conecta a MySQL habilitando la carga de archivos locales, requisito para usar LOAD DATA LOCAL INFILE.

Importar datos del CSV a la tabla
sql
LOAD DATA LOCAL INFILE '/home/isard/equipaments_utf8.csv'
INTO TABLE equipaments
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 LINES;
Carga masivamente los registros del fichero CSV convertido a UTF‑8 en la tabla equipaments, ignorando la primera línea de encabezados y usando la coma como separador de campos.

Comprobar contenido de la tabla
sql
SELECT * FROM equipaments LIMIT 5;
Visualiza los primeros cinco registros insertados en la tabla para verificar que las columnas se han importado correctamente y los datos son coherentes.

Conexión remota a MySQL desde otra máquina
bash
mysql -h 192.168.6.20 -u bchecker -p
Abre una sesión MySQL desde un cliente remoto usando la IP del servidor, el usuario bchecker y una contraseña, comprobando que el acceso remoto está correctamente configurado.

Listar bases de datos y tablas
sql
SHOW DATABASES;
USE equipaments_educacio;
SHOW TABLES;
Muestra todas las bases de datos disponibles, selecciona equipaments_educacio como base de datos activa y lista sus tablas para confirmar que equipaments existe y es accesible.
