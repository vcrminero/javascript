# Datos primitivos
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
