# Preguntas básicas

1. ¿Qué tipos de datos existen en JS?
2. ¿Qué diferencia hay entre un valor y una referencia? ¿Qué tipos de datos se pasan por valor y por referencia?
3. ¿Qué es un literal?
4. ¿Se puede asignar una función a una variable? ¿Por qué sucede esto?
5. ¿Qué son los valores trusy y falsy?
6. ¿Qué es una función de primer orden? ¿Por qué en JS las funciones son de primer orden?
7. ¿Qué es el scope (o entorno léxico)?
8. ¿Qué es un closure? ¿En que casos usarlo?
9. ¿Qué diferencias existen entre let y var?
10. ¿Cómo se define un objeto en JS? ¿Pueden crearse objetos con atributos privados?
12. ¿Qué es el prototype? ¿Para qué sirve?
13. ¿Qué es una fat arrow function? ¿Qué diferencias hay con una función normal?
14. ¿Qué es una función constructora de objetos?
15. ¿Qué diferencia existe entre `==` y `===`?
16. ¿Qué diferencia existe entre `undefined` y `null`?
17. ¿Qué valor tiene la variable a: `let a;`?
18. ¿Qué son las promesas? ¿Para qué usarlas?
19. ¿Qué es una función asíncrona?
20. ¿Cómo obtienes el valor de una Promesa?
21. ¿Cómo o en que casos usar `async`, `await` y `class`?
22. ¿Qué valor devuelve una función sin `return`? ¿Qué valor devuelve una asignación?
23. ¿Qué es una expresión? ¿Qué es una sentencia?
24. ¿Qué es un generador? ¿En qué casos usarlo?

# Preguntas intermedio

1. ¿Qué es el DOM?
2. ¿Si se declara un objeto con `const`, se puede modificar alguna propiedad?
3. ¿Si se daclara un arreglo con `const`, se puede modificar algún elemento o agregar/quitar uno?
4. ¿Qué es la pila de ejecución (o contexto de ejecución)? ¿Cómo se ejecuta un programa en JS?
5. ¿Qué es `Àrray.map`, `Array.reduce`, `Array.filter`?
6. ¿Cómo se vincula JS con los elementos del DOM?
5. ¿Se pueden crear módulos en JS?
6. ¿Qué es this y su contexto? ¿Qué significa this binding (o enlazamiento)? ¿Qué tipos de binding hay?
7. ¿Qué es`arguments`?
8. ¿Qué es la asignación por destructuración?
9. ¿Para que sirve el operador spread `...`?
10. ¿Qué es el prototype `Object`? ¿Qué utilidad se le puede dar?
7. ¿Qué valor se imprime?:
```js
let a = 10;
function b() {
  let a = 11;
  console.log(a);
}
b();
```
7. ¿Qué valor se imprime?
```js
let a = 10;
function print() {
  console.log(a);
}
function start() {
  let a = 20;
  print();
}
```
8. Al ejecutar el siguiente fragmento de código, ¿ocurre algún error? ¿si es así, porque? ¿qué significan los `{}` en JS?
```js
{ let a = 10; }
{ let b = 11; }
console.log(a, b);
```
9. ¿Qué es la destructuración de objetos? ¿y de arreglos?
10. ¿Qué valor se imprime?
```js
function Dog(name) {
  this.name = name;
  console.log(this);
}

const a = Dog('Doggy');
```
11. ¿Para que sirve la palabra `new`?
12. ¿Ocurre algún error al ejecutar lo siguiente? ¿si es así, porqué?
```js
const a = document.createElement('ul');
a.appendChild('li');
document.querySelector('body').appedChild(a);
```
13. ¿Qué es objeto `document`?
14. ¿Qué son los callback?

# Avanzadas

1. ¿Como compararías los siguientes objetos para ver si son iguales en cuanto a valores? ¿y en cuanto a referencia?
```js
const a = { a: 10, b: [1,2,3], c: { m: true, n: [{a: 'a'}, 1]}};
const b = a;
const c = { a: 10, b: b.b, c: a.c };
```
2. ¿Que se imprime en pantalla? ¿Se modificó algún valor del objeto a? ¿si es así, porque?
```js
const a = { a: 10, b: [1,2,3] };
const b = a;
const c = { a: 10, b: a.b };

a.a = 20;
b.b[2] = 4;
c.a = 30;
c[2] = 5;

console.log(a);
```
3. ¿ Qué se imprime en pantalla?
```js
const a = { m: 10, c: null };
const b = { ...a.c && { a: m } };
console.log(b);
```
4. ¿Qué valor obtiene c?
```js
const a = undefined;
const b = null;
const c = a || b;
```
5. ¿Es posible hacer lo siguiente? ¿Qué valor se imprime? ¿Qué valor obtienen las constantes c y d?
```js
function a() {
  function b() {
    function c() {
      console.log(a);
    }

    const d = c();
  }

  const c = b;
  return c;
}

console.log(a()());
```
6. ¿Qué valor se imprime?
```js
const a =  () => {
  console.log(this);
}
a();
```
7. ¿Qué es el event bubbling?
8. ¿Qué es el local storage?
9. ¿Como exportar e importar datos de un módulo con ES6?
10. ¿Es buena idea usar ES6 para una aplicación web?
11. ¿Qué es `use strict`?
