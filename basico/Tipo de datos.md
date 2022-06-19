# Tipo de datos

## JS es un lenguaje débilmente tipado y dinámico
- Debilmente tipado: Las variables no están asociadas directamente con ningún tipo de valor en particular
- Dinámico: A cualquier variable se le puede asignar (y reasignar) valores de todos los tipos

```javascript
let variable = 1; // variable es un número
variable = "uno"; // ahora un string
variable = true;  // ahora un boolean
```

## En JS hay 9 tipos de datos
6 tipos primitivos

|Tipo|| |
|---|---|---|
|String|typeof instance === "string"| "Hola mundo" |
|Number|typeof instance === "number"| 1, 2, 3.14 |
|BigInt|typeof instance === "bigint"| 10n |
|Boolean|typeof instance === "boolean"| true / false |
|Undefined|typeof instance === "undefined"| Explícitamente declarar una variable sin valor |
|Symbol|typeof instance === "symbol"| Usado con objetos |

Y por otro lado están:

_null_<br>
typeof instance === "object"

_object_<br>
typeof instance === "object"
(Como Arrays, Dates, Literals, etc)

_function_<br>
typeof instance === "function"
