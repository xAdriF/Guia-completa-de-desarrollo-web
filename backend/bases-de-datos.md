# Bases de Datos: El Almacén de la Información Web

## ¿Qué es una Base de Datos (DB)?

Una **Base de Datos** es un conjunto organizado de datos que se almacena y se accede de manera electrónica desde un sistema informático. En el contexto de desarrollo web, la DB es donde el **servidor backend** guarda de forma **persistente** toda la información crucial de la aplicación, como cuentas de usuario, artículos, historial de pedidos o configuraciones. 

[Image of a database server with tables and structured data]


---

## Funciones de la Base de Datos en el Backend

La base de datos es esencial para la funcionalidad de cualquier aplicación moderna, ya que maneja el ciclo de vida de los datos, conocido como **CRUD** (Create, Read, Update, Delete).

* **Almacenamiento (Create/Update):**
    * Recibe datos del servidor (ej. un nuevo registro de usuario, la actualización de un precio) y los almacena de forma segura.

* **Recuperación (Read):**
    * Permite que el servidor consulte y obtenga datos específicos para responder a las peticiones del usuario (ej. mostrar el *feed* de noticias o el detalle de un producto).

* **Consistencia e Integridad:**
    * Garantiza que los datos sean **precisos** y sigan las reglas definidas (ej. asegurar que dos usuarios no tengan el mismo nombre de usuario).

---

## Tipos de Bases de Datos Populares

Las bases de datos se dividen principalmente en dos grandes categorías, dependiendo de cómo estructuran y almacenan la información.

* **Bases de Datos Relacionales (SQL):**
    * **Características:** Almacenan datos en **tablas** con filas y columnas predefinidas. Utilizan el lenguaje **SQL (Structured Query Language)**. Son ideales cuando la estructura de los datos es clara y se necesita una alta **integridad** (ej. sistemas bancarios, inventarios).
    * **Ejemplos:** MySQL, PostgreSQL, Oracle, SQL Server.

* **Bases de Datos No Relacionales (NoSQL):**
    * **Características:** Almacenan datos en formatos flexibles (ej. documentos JSON, pares clave-valor). Son ideales para manejar grandes volúmenes de datos que cambian rápidamente y no requieren un esquema rígido.
    * **Ejemplos:** MongoDB (Documentos), Redis (Clave-Valor), Cassandra (Columnas anchas).

---