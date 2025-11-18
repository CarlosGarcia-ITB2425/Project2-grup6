# 🏠[Pàgina principal.md](Projecte2-grup6)

## 1.🖥️ [Hardware de serveis](Projecte2-grup6/Hardware%20de%20serveis)

Esta sección agrupa la documentación sobre el despliegue y configuración de todos los servicios esenciales del proyecto.

   - [BBDD 💾](Projecte2-grup6/Hardware%20de%20serveis/BBDD.md)
   - [DHCP 📍](Projecte2-grup6/Hardware%20de%20serveis/DHCP.md)
   - [DNS 🌐](Projecte2-grup6/Hardware%20de%20serveis/DNS.md)
   - [FTP 📤](Projecte2-grup6/Hardware%20de%20serveis/FTP.md)
   - [SSH 🛡️](Projecte2-grup6/Hardware%20de%20serveis/SSH.md)
   - [Web server 🌍](Projecte2-grup6/Hardware%20de%20serveis/Web%20server.md)

   ### 1.1 [Desplegament d'equips](Projecte2-grup6/Hardware%20de%20serveis/Desplegament%20d'equips)

   Documentación sobre los sistemas operativos cliente utilizados para las pruebas.

   - [Linux 🐧](Projecte2-grup6/Hardware%20de%20serveis/Desplegament%20d'equips/Linux.md)

   - [Windows 🪟](Projecte2-grup6/Hardware%20de%20serveis/Desplegament%20d'equips/Windows.md)

## 2.📡 [Hardware de xarxes](Projecte2-grup6/Hardware%20de%20xarxes)
   
 - [DMZ-Intranet-NAT 🚦](Projecte2-grup6/Hardware%20de%20xarxes/Xarxes.md)



---

# 🏠 Projecte2-grup6: Infraestructura de Red y Datos

> El proyecto simula un entorno profesional, diseñando, desplegando y gestionando una **infraestructura de red multicapa** junto con una **aplicación de visualización de datos** que consume un dataset real de equipamientos educativos de Barcelona.

---

## 🎯 Resumen y Objetivos Clave

* **Propósito:** Diseñar, desplegar y gestionar una infraestructura de red, servidores y una aplicación de visualización de datos.
* **Datos:** Uso de un **CSV de equipamientos educativos de Barcelona** (Datos Abiertos).
* **Ciclo de Datos:** Adquisición $\rightarrow$ Almacenamiento (**MySQL**) $\rightarrow$ Presentación (**Aplicación Web**).
* **Metodología:** **Sprints** (enfoque ágil) y **Git** para control de versiones y documentación.
* **Seguridad:** Uso de autenticación por **clave pública/privada (SSH)**.
* **Credenciales de Prueba:** Usuario `bchecker` con contraseña `bchecker121` en todos los sistemas.

---

## 🌐 Infraestructura de Red Segmentada

Se plantea un **router** que segmenta la red en tres zonas principales (topología segura y común en entornos profesionales).

| Zona | Descripción | Propósito |
| :--- | :--- | :--- |
| **DMZ** (Zona Desmilitarizada) | Servicios públicos | **Acceso desde el exterior** (Ej: Servidor Web). |
| **Intranet** | Red interna privada | **Comunicaciones seguras** y privadas. |
| **Zona NAT** | Traducción de direcciones | Gestión de **direcciones** y control de **tráfico saliente**. |

### 🗺️ Visión General del Diagrama

Este diagrama ilustra la **topología de red** propuesta, segmentada en tres zonas principales para optimizar la seguridad y la gestión del tráfico: **NAT**, **DMZ** e **Intranet**. La estructura se centra alrededor de un router principal que distribuye el acceso a los diferentes servicios y clientes.

![Diagrama](/Projecte2-grup6/Imagenes/diagrama1.png)

---

## 💻 Despliegue de Servicios (Servers)

Múltiples servidores se despliegan sobre esta topología, cada uno con un rol esencial.

### 1. Servidores de Infraestructura Básica
| Servicio | Rol Principal | SO (Ejemplos) |
| :--- | :--- | :--- |
| **MySQL / BBDD** 💾 | **Almacenamiento** de datos (CSV importado). | Linux |
| **Web server** 🌍 | Alojar la **aplicación web** de visualización. | Linux |
| **SSH** 🛡️ | **Acceso seguro** y administración remota. | Linux |
| **FTP** 📤 | **Transferencia de ficheros** (datos, backups). | Linux |

### 2. Servicios de Red
* **DNS:** Gestiona los **nombres de dominio** internos.
* **DHCP:** **Asignación automática de IPs** en la red.

---

## 🖥️ Despliegue de Equipos Cliente

Para pruebas y verificación de la conectividad y acceso a servicios.

### 1.1 Desplegament d'equips
* **Linux** 🐧
* **Windows** 🪟

---

## 📈 Datos y Aplicación Web

El proyecto pone en valor la conexión entre la infraestructura y el dato real.

1.  **Datos:** Utiliza un **CSV de equipamientos educativos** de Barcelona (datos.gob.es).
2.  **Base de Datos:** El CSV se **importa a MySQL**, creando tablas con campos (nombre, tipo, ubicación, etc.).
3.  **Aplicación Web:** Desarrollo de una aplicación ligera que permite:
    * **Visualizar** el contenido de la BBDD.
    * Ofrecer **filtros** o consultas por distintos criterios.

---

## ✨ Valor Formativo y Beneficios

* **Integración Completa:** Conecta redes, servicios de infraestructura, bases de datos y desarrollo de aplicaciones.
* **Buenas Prácticas:** Promueve el uso de **Git** (versionado y colaboración) y **seguridad (SSH)**.
* **Interoperabilidad:** Manejo de entornos **Windows y Linux** para pruebas.
* **Práctico:** Da sentido al uso de **Datos Abiertos** públicos en proyectos técnicos reales.

