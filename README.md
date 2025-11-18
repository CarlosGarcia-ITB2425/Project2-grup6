[Linux.md](Projecte2-grup6/Hardware%20de%20serveis/Desplegament%20d'equips/Linux.md)
[Linux.md](Projecte2-grup6/Hardware%20de%20serveis/Desplegament%20d'equips/Linux.md)
# Resumen del proyecto

El proyecto Project2-grup6 es una iniciativa académica cuyo propósito es diseñar, desplegar y gestionar una infraestructura de red multicapa realista (router + varias subredes) junto con una aplicación de visualización de datos. Se trata de simular un entorno profesional donde confluyen aspectos de redes, servidores y bases de datos, además de una capa de aplicación que consume datos reales.

## Infraestructura de red

- Se plantea un router que segmenta la red en al menos tres zonas (como DMZ, Intranet y NAT), lo cual es común en redes seguras:

- DMZ (zona desmilitarizada): para servicios accesibles desde el exterior.

- Intranet interna: para comunicaciones seguras y privadas.

- Zona NAT: para gestión de direcciones y control de tráfico saliente.

- Sobre esta topología de red se despliegan múltiples servidores, cada uno con su rol específico:

- Servidor web: para alojar la aplicación de visualización.

- Servidor MySQL: base de datos donde se importa un CSV con datos reales.

- Servidor SSH: para acceso seguro y administración remota.

- Servidor DNS: gestionando nombres de dominio internos.

- Servidor DHCP: asignación automática de IPs en la red.

- Servidor FTP: para transferencia de ficheros, posiblemente para subir datos o backups.

Además, se configuran dos clientes finales: uno con Windows y otro con Linux, que permiten probar la conectividad, el acceso a los servicios y la aplicación desde extremos distintos.

## Datos y aplicación

- El proyecto utiliza un archivo CSV con el listado de equipamientos educativos de Barcelona, que proviene de datos abiertos. Este tipo de datos reflejan centros educativos, equipamientos asociados, y su distribución territorial. 
Datos.gob.es

- Dicho CSV se importa en la base de datos MySQL, creando una o varias tablas con los distintos campos del fichero (nombre del equipamiento, tipo, ubicación, etc.).

- Sobre esos datos, se desarrolla una aplicación web ligera que permite visualizar el contenido de la base de datos, mostrando los equipamientos educativos cargados y ofreciendo, posiblemente, filtros o consultas por diferentes criterios.

- De este modo, el sistema no solo demuestra la infraestructura de red, sino también el ciclo completo de datos: adquisición (CSV), almacenamiento (MySQL) y presentación (aplicación web).

## Organización y metodología

- El proyecto está organizado por sprints, lo que indica un enfoque ágil: se divide el trabajo en varias fases (posiblemente tres sprints), cada uno con tareas específicas para desplegar la red, montar los servidores y desarrollar la aplicación.

- El control de versiones se realiza mediante Git, manteniendo todo el despliegue, los scripts y la documentación en un repositorio (el que has compartido). Esto permite trazabilidad, colaboración y respaldo coherente.

- También se menciona el uso de autenticación por clave pública/privada (SSH), lo cual mejora la seguridad en el acceso a los servidores.

- Se usa un usuario predefinido (bchecker) con contraseña (bchecker121) en todos los sistemas, lo que facilita la configuración y pruebas en entorno controlado.

## Valor formativo y beneficios

- Desde el punto de vista educativo, este proyecto es muy completo: obliga a los participantes a trabajar con aspectos de red (segmentación, zonas seguras), servicios de infraestructura (DHCP, DNS, FTP, SSH) y persistencia de datos (MySQL), además de una capa de aplicación que consume datos reales.

- Permite ver cómo los datos abiertos (como los del Ayuntamiento de Barcelona) pueden usarse en proyectos técnicos reales, dando sentido práctico al uso de CSV públicos.

- Al desplegar clientes Windows y Linux, el equipo aprende a manejar interoperabilidad y a probar servicios en distintos entornos.

- El hecho de documentar todo y trabajar con Git promueve buenas prácticas de ingeniería de software, versionado y colaboración.

## Resultado esperado

1. Cuando el proyecto esté completado, se debe tener un entorno funcional donde:

2. La red está correctamente segmentada, y los servicios se comunican según lo previsto entre distintas zonas.

3. El CSV con equipamientos educativos de Barcelona está importado en la base de datos.

4. La aplicación web permite consultar y visualizar esos equipamientos de forma clara y usable.

5. Los clientes (Windows y Linux) pueden acceder a los servicios (web, FTP, SSH, etc.).

6. La infraestructura es reproducible (documentada) y segura (uso de SSH, control de acceso), aunque el usuario bchecker y su contraseña se usen solo para desarrollo.


