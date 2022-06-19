# Variables
Una variable es una referencia a un valor.
> Debes imaginar a las variables como tentáculos, en lugar de cajas. No _contienen_ valores, los referencian. Dos variables pueden referirse al mismo valor. Un programa puede acceder sólo a los valores a los que todavía tiene una referencia. Cuando necesita recordar algo, le crece un tentáculo para aferrarse a él o le vuelve a unir uno de sus tentáculos existentes. -Marijn Haverbeke (Eloquent JavaScript).
> 
## let
```javascript
let edad = 30;
```

## var
```javascript
var edad = 30;
````

## const
```javascript
let nombre = "Victor";
```

## Características
El valor de una variable, puede cambiar.

```javascript
let edad = 30; // "edad" es igual a 30
edad = 31; // "edad" es igual a 31
```

El valor de una constante, no puede cambiar
```javascript
const edad = 30; // "edad" es igual a 30
edad = 31; // error ("edad" sigue siendo 30)
```

Consideraciones para nombrar variables:
```javascript
// Usar camelCase
let miVariable = 123;

// El nombre puede llevar un número (pero no iniciar con un número)
let variable1 = 123; // Válido
let 1variable = 123; // ERROR
```

# let vs var
_let_ fue introducida en ES6 y es la forma preferente para crear variables.

| let      |      var      |
|----------|:-------------:|
| Es _blocked-scope_ |  Es _function-scoped_ |
| No permite re-declarar variables |    Sí permite re-declarar variables   |
| No permite _Hoisting_ | Sí permite _Hoisting_ |


## Scope
_let_ es _block scoped_
```javascript
function saludo() {
  
    let a = 'hola';
    // "b" NO puede usarse aquí
  
    if(a == 'hola'){
        // "a" SÍ puede usarse aquí
        // "b" SÍ puede usarse aquí
        let b = 'mundo';
        console.log(a + ' ' + b);
    }

    // "b" no puede usarse aquí
    console.log(a + ' ' + b); // error
  
}
// "a" NO puede usarse aquí

saludo();
```

_var_ es _function scoped_
```javascript
function saludo() {
    // la variable "a" SÍ puede usarse aquí
    var a = 'hola';
    console.log(a);
}
// "a" NO puede usarse aquí
saludo();
```

# Re-declarar variables
_let_ no lo permite
```javascript
  let a = 5; // 5
  let a = 3; // error
```
_var_ sí lo permite
```javascript
  let a = 5; // 5
  let a = 3; // 3
```
Re-declarar una variable con _let_ en un bloque diferente, trata a la variable como una diferente y NO cambia el valor de la variable afuera.
```javascript
let a = 5;
console.log(a); // 5

{
    let a = 3;
    console.log(a); // 3
}

console.log(a); // 5
```

Re-declarar una variable con _var_ en un bloque diferente, cambia el valor de la variable también afuera.
```javascript
var a = 5;
console.log(a); // 5

{
    var a = 3;
    console.log(a); // 3
}

console.log(a); // 3
```

## Hoisting
_let_ no permite _hoisting_
```javascript
console.log(a);
let a; // Uncaught ReferenceError: a is not defined
````
_var_ sí permite _hoisting_
```javascript
console.log(a);
var a; // undefined (no es un error)
```
