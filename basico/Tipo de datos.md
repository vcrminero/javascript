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

|Tipo||
|---|---|
|Undefined|typeof instance === "undefined"|
|Boolean|typeof instance === "boolean"|
|Number|typeof instance === "number"|
|String|typeof instance === "string"|
|BigInt|typeof instance === "bigint"|
|Symbol|typeof instance === "symbol"|

Y por otro lado están:

_null_<br>
typeof instance === "object"

_object_<br>
typeof instance === "object"

_function_<br>
typeof instance === "function"

## Datos primitivos
Son datos que no son un objeto y no tienen métodos.

Todos los primitivos son inmutables, es decir, no se pueden modificar.

Sí se puede reasignar un nuevo valor a la variable, pero el valor existente no se puede cambiar de la misma forma en que se pueden modificar los objetos, los arreglos y las funciones.

Ejemplo:

```javascript
// El uso de un método string no modifica el string
var saludo = "hola";
console.log(saludo);               // hola
saludo.toUpperCase();
console.log(saludo);               // hola

// El uso de un método de array sí cambia el array
var arreglo = [];
console.log(arreglo);               // []
arreglo.push("uno");
console.log(arreglo);               // ["uno"]

// La asignación le da al primitivo un nuevo valor (no lo muta)
saludo = saludo.toUpperCase();       // HOLA

```

## undefined vs null
_undefined_ indica que una variable ha sido declarada, pero no se le asignó valor.
```javascript
let a;

console.log(a); //undefined
```

_null_ es un objeto y puede ser asignado a una variable como representación de "sin valor"

Por ejemplo, cuando no sabes el valor le puede asignar _null_ a una variable:

```javascript
var a = null;

// Después en el programa
a = 123;
```
