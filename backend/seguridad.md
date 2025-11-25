# Seguridad en el Backend: Protegiendo tu Aplicación

## ¿Por qué es Crítica la Seguridad?

La **seguridad en el backend** se refiere a las prácticas y defensas implementadas en el servidor para proteger la información sensible, evitar el acceso no autorizado y garantizar que el servicio sea robusto y esté disponible. Dado que el servidor gestiona las bases de datos, las cuentas de usuario y la lógica de negocio, es el **objetivo principal** de los ataques. Una brecha de seguridad puede resultar en pérdida de confianza, multas regulatorias y daño financiero.

---

## Mecanismos de Protección Clave

Existen varios pilares esenciales para proteger un servidor y sus datos:

* **Autenticación:**
    * **Propósito:** Verificar que el usuario es quien dice ser.
    * **Práctica:** Uso de **contraseñas robustas** almacenadas con *hashing* (ej. bcrypt) y técnicas como la **autenticación multifactor (MFA)**.
    * **Tokenización:** El servidor usa *tokens* (ej. **JWT**) después del inicio de sesión para verificar la identidad en peticiones futuras, sin tener que enviar la contraseña cada vez.

* **Autorización:**
    * **Propósito:** Determinar a qué **recursos** tiene derecho a acceder un usuario ya autenticado.
    * **Práctica:** Implementación de **roles y permisos** (ej. un "administrador" puede borrar datos, un "usuario normal" solo puede leer su propio perfil).

* **Validación de Entradas:**
    * **Propósito:** Nunca confiar en los datos que llegan del cliente (frontend).
    * **Práctica:** El servidor debe **limpiar y validar** todos los datos recibidos (formularios, APIs) para prevenir ataques como la **Inyección SQL** o **XSS (Cross-Site Scripting)**.

---

## Amenazas Comunes

Los desarrolladores deben estar conscientes de los riesgos más frecuentes para aplicar las defensas adecuadas.

* **Inyección SQL (SQL Injection):**
    * Ocurre cuando un atacante inserta código SQL malicioso en un campo de entrada para manipular o robar información de la base de datos.

* **Fallo de Autenticación (Broken Authentication):**
    * Fallos en la gestión de sesiones o contraseñas que permiten a un atacante suplantar la identidad de un usuario.

* **Cross-Site Scripting (XSS):**
    * Permite a un atacante inyectar scripts maliciosos del lado del cliente en un sitio web, que luego se ejecutan en el navegador de otros usuarios.

* **Exposición de Datos Sensibles:**
    * No cifrar datos sensibles, especialmente contraseñas y datos personales, o usar cifrado débil. La comunicación entre cliente y servidor siempre debe usar **HTTPS** (cifrado SSL/TLS).