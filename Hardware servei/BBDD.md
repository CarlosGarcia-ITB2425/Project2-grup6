## Descargar un archivo CSV desde portal OpenData

`wget "https://opendata-ajuntament.barcelona.cat/data/dataset/[...]/download" -O educacio_bcn.csv`

Este comando descarga el archivo y lo guarda como educacio_bcn.csv en el directorio actual.



2. Visualizar las primeras líneas del archivo CSV
Para ver rápidamente si el archivo se descargó correctamente y cómo es su contenido, utiliza el comando:

bash
head -5 educacio_bcn.csv
Esto muestra las primeras 5 líneas del archivo, permitiéndote inspeccionar el formato y visualización de los datos.

La captura enseña el uso de head -5 para revisar los primeros registros del fichero CSV descargado. Se observan algunos errores en los caracteres, típicos de un problema de codificación.

3. Convertir el archivo CSV a UTF-8
Si el archivo original está en otra codificación (por ejemplo, UTF-16), debes convertirlo para evitar problemas de lectura. Para ello, usa el comando:

bash
iconv -f UTF-16 -t UTF-8 ~/Baixades/educacio_bcn.csv -o ~/Baixades/educacio_bcn_utf8.csv
Esto genera un nuevo archivo en UTF-8, listo para trabajar en la mayoría de aplicaciones y bases de datos.



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

## Acceder a MySQL y mostrar tablas de la base de datos

`mysql -u bchecker -p`

![Acceder](bchecker%20-p.png)

Después de acceder, selecciona la base de datos y muestra las tablas disponibles:

`USE barcelona_educacio;
SHOW TABLES;`

La imagen muestra el acceso a MySQL, el cambio a la base de datos barcelona_educacio y la lista de tablas existentes, donde aparece equipaments.

## Visualizar la estructura de la tabla equipaments

`DESCRIBE equipaments;`

![Visualizar](describe.png)

La captura enseña la estructura de la tabla equipaments, mostrando cada campo, su tipo de datos, si permite NULL, si es clave primaria o secundaria, valores predeterminados y atributos extra.

## Consultar registros de la tabla equipaments

`SELECT * FROM equipaments LIMIT 10;`

![Consultar](select.png)

Esta imagen muestra el resultado del comando SQL que extrae un máximo de 10 registros de la tabla equipaments, mostrando todas sus columnas y algunos datos de ejemplo.




