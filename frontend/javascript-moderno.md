# Resumen de JavaScript Moderno (ES6+)

## Introducción
**JavaScript moderno** hace referencia al conjunto de características introducidas desde ES6 (ECMAScript 2015) hasta la actualidad. Estas mejoras permiten escribir código más limpio, organizado y eficiente, además de facilitar la creación de aplicaciones web interactivas, dinámicas y escalables.

---

## Conceptos Fundamentales

### Declaración de Variables
- **`let`**: permite crear variables modificables con alcance de bloque.  
- **`const`**: define constantes cuyo valor no debe cambiar.  
- Se evita usar `var` por su comportamiento confuso con el *hoisting*.

```js
let contador = 1;
const PI = 3.1416;
