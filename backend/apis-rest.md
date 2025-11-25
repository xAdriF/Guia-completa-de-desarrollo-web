# APIs: El Lenguaje de Comunicación entre Sistemas

## ¿Qué es una API?

Una **API (Application Programming Interface)** es un conjunto de reglas, protocolos y herramientas que permite que diferentes aplicaciones de software se comuniquen entre sí. En el desarrollo web, la API es el **contrato** que define exactamente cómo el **frontend** (el cliente, como un navegador o una app) puede solicitar información o enviar datos al **backend** (el servidor). Esencialmente, es el **mesero** que toma el pedido y lleva la respuesta, sin que el cliente tenga que ir a la cocina. 

[Image of a diagram showing frontend client communicating with a backend server through an API]


---

## Tipos de Peticiones API (Métodos HTTP)

Las APIs más comunes, conocidas como **APIs RESTful**, utilizan los métodos estándar del protocolo HTTP para realizar acciones sobre los datos en el servidor. Esto se conoce como operaciones **CRUD** (Crear, Leer, Actualizar, Borrar).

| Método HTTP | Propósito (Acción) | Operación CRUD | Ejemplo |
| :--- | :--- | :--- | :--- |
| **GET** | Obtener o solicitar datos. | **R**ead (Leer) | `GET /productos` (Lista de productos) |
| **POST** | Crear un nuevo recurso o enviar datos. | **C**reate (Crear) | `POST /usuarios` (Crear un nuevo usuario) |
| **PUT/PATCH** | Modificar o actualizar un recurso existente. | **U**pdate (Actualizar) | `PUT /usuarios/5` (Cambiar datos del usuario 5) |
| **DELETE** | Eliminar un recurso específico. | **D**elete (Borrar) | `DELETE /productos/10` (Eliminar producto 10) |

---

## Estructura y Formato

Para que la comunicación sea eficiente, la información que se intercambia a través de la API debe seguir un formato estandarizado.

* **Endpoint:** Es la dirección URL específica donde el cliente envía la petición (ej. `/api/v1/productos`).
* **Formato de Datos:** El formato más utilizado para enviar y recibir datos en las APIs modernas es **JSON (JavaScript Object Notation)**, debido a que es ligero, fácil de leer para humanos y fácil de interpretar para las máquinas.
* **Códigos de Estado (Status Codes):** La respuesta del servidor siempre incluye un código que indica el resultado de la petición.
    * **200 OK:** La petición fue exitosa.
    * **404 Not Found:** El recurso solicitado no existe.
    * **401 Unauthorized:** El usuario no está autenticado.
    * **500 Internal Server Error:** Ocurrió un fallo en el servidor.