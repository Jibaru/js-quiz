# Problemas básicos

1. Crear una función que encuentre el menor número de un arreglo de elementos cualquiera.
2. Crear una función que encuentre la menor fecha de un arreglo de strings que representan una fecha. El formato de los strings es el siguiente:

```js
'mm-dd-YYYY'
```

3. Se tiene el siguiente texto:

```js
const texto = 'A1 100 B3 102 B2 203 C1 900 C8 100 C89 10.31 D11 202';
```
Convierta el texto a un arreglo de objetos, donde cada objeto tendrá el formato:
```js
{ A1: 100 }
```

4. Se tiene una lista de strings que representa un correo electrónico. Valide que correos electrónicos son validos y cuales no. Utilizar funciones de alto nivel (o high order functions).

```js
const lista = [
    'ignacio@gmail.com',
    'pedro@pedro',
    'juana_marticorena@@',
    'maria_luiza@yahoo.es',
    'AntonellaPerez@hotmailcom',
    'UrielFernandez2002@empresa.es',
    'Martin_1990@gmail.com@'
    'Irma_Fernandez@hotmail.@com',
    'ignacio@hotmail.com',
]
```

5. Ordene ascendentemente los siguientes elementos del arreglo por la propiedad `id`. Utilizar funciones de alto nivel (o high order functions).

```js
const lista [
    { id: 100, name: 'Manzana' },
    { id: 56, name: 'Pera' },
    { id: 11, name: 'Piña' },
    { id: 190, name: 'Naranja' },
    { id: 4, name: 'Mandarina' },
]
```

6. A partir de la lista anterior, genere un arreglo de strings que posea solamente los `name` de cada objeto. Además ordénelo descendentemente.

7. Se tiene la siguiente función:

```js
function showLowercase(str) {
   const str2 = str.toLowerCase();
    console.log(str2);
}
```
Transforme esta función a una nueva (`nuevaFuncion`) que reciba un callback de la siguiente manera, que deberá ser invocado de la siguiente manera:
```js
nuevaFuncion('mistr', function(strChanged) {
    console.log(strChanged);
});
```

8. Cree una función que devuelva otra función que incremente un contador interno al ser llamada. Utilizar el concepto de closures.

9. Crear la siguiente estructura de funciones constructoras (`classes`).

```
Clase Elemento (contenido: string)
+obtenerContenido() -> contenido

Clase SubElemento (padre: Elemento, nodo: string)
+obtenerNodoPadre() -> padre.contenido()

Clase Contenedor (contenido: string, tag: string) hereda de Elemento
+obtenerContenido() -> contenido
+agregarA(domElement: HTMLElement) -> vacio
```
El método agregarA debe recibir un HTMLElement y a partir del `tag` y el contenido agregar un elemento en el nodo seleccionado. Por ejemplo si el tag es `p` y el contenido `hola mundo`, al llamar a `agregarA` de la siguiente manera:
```js
obj.agregarA(body); // body es un HTMLElement que está vinculado a la etiqueta body del DOM
```
El DOM quedaría:
```html
...
<body>
<p>hola mundo</p>
</body>
...
``` 
10. Cree una promesa que devuelva el siguiente arreglo al ser resuelta.
```js
const arreglo = [1,2,3,4,5,6];
```

# Problemas intermedios

1. Se tiene el siguiente objeto `objL`:
```js
const objL = [
    { 
        a: 10, // suma de 1+2+3+4
        b(num) {
            return num > 20;
        }
    },
    5, // Promedio de 1,2,3,4
    [
        [1,2,3,4], // Arreglo de 4 números consecutivos que no se repite en ninguno de los objetos que se creará más adelante
        {
            date: '12-04-1997' // Fecha de creación del objeto en este formato
        },
        false // es el valor de invocar a b con num = a.
    ],
    {
        status: 200, // 200 solamente si b() es true, sino es 400
        info: {
            messages: [
                "Ok", // Ok solo si status es 200, sino es Error
                "Successfull" // Successfull solo si es OK, sino es Bad
            ]
        }
    }
];
const listas = [];
```
Crear 4 objetos con el mismo formato, respetando el orden y las condiciones. Cada objeto debe ser único y no debe existir ninguna referencia entre ellos.


2. Realizar una copia por valor del siguiente objeto:
```js
const obj = {
    name: 'Jos',
    age: 23,
    products: [
        {
            id: 3,
            name: 'Plate',
            price: 50,
            tags: [
                'small', 'circle', 'cook'
            ],
            amount: 0
        },
        {
            id: 5,
            name: 'PC',
            price: 2500,
            tags: [
                'info', 'giant', 'computer'
            ],
            amount: 5
        },
    ],
}
```

3. Eliminar todos los `null` y `undefined` del siguiente objeto. Considerar que si una propiedad posee estos valores o es un objeto vacio, no debe existir en el objeto.

```js
const obj = {
    a: 1,
    b: false,
    c: '',
    d: {
        a: null,
        b: 'undefined',
        c: undefined,
        d: [
            1,
            false,
            0,
            undefined,
            {
                a: [1,undefined,8],
                b: true,
                c: function(){
                    return undefined;
                },
                d: 'ok'
            }
        ],
        e: {
            a: null,
            b: null,
        }
    },
    e: {
        a: {
            b: {}
        },
        b: null,
    },
}
```

4. Se tiene la siguiente lista de números:

```js
const list = [1721, 979, 366, 299, 675, 1456];
```
En esta lista, existen dos números que suman 2020, y son 1721 y 299. Ahora, busque en la siguiente lista dos números que sumen 2020 e imprímalos.

```js
const list2 = [
429,
1368, 1661, 1687, 1593, 1495, 1565, 1500, 1635, 1845, 1645, 1999, 1415, 1054, 1930, 1774, 1405, 1993, 1757, 1623, 1675, 1665, 631, 1950, 1702, 1311, 1509, 1790, 1643, 1884, 226, 1455, 1679, 1746, 1284, 1342, 1684, 1543, 1396, 1806, 1523, 1363, 1011, 1577, 1767, 1287, 1885, 1517, 1556, 1722, 1260, 1624, 1466, 1263, 1162, 1688, 1202, 1913, 1964, 1385, 1970, 1976, 1431, 858, 1748, 1544, 1438, 1300, 1926, 1587, 1376, 1939, 1039, 1639, 1539, 1491, 1631, 1521, 1564, 1507, 1637, 1534, 1713, 1533, 1118, 1356, 2003, 282, 1079, 1837, 1259, 1941, 1836, 1903, 1433, 1467, 1027, 1441, 1048, 1742, 1087, 1872, 1476, 1657, 1361, 1182, 1494, 1529, 1822, 1444, 1330, 1514, 1723, 1432, 1683, 1997, 1443, 1474, 1932, 1504, 1313, 1765, 19, 1784, 1619, 992, 1560, 1680, 1626, 1558, 1899, 1293, 1676, 1161, 1140, 1341, 1597, 1628, 1611, 1302, 1269, 1241, 1952, 1591, 1726, 428, 1703, 1289, 1109, 1478, 1002, 1817, 1849, 1838, 1319, 1641, 583, 1920, 1453, 1411, 1870, 1763, 1469, 1646, 1719, 1213, 1462, 1545, 1682, 1711, 18, 2004, 1252, 1620, 1559, 1315, 781, 1656, 1987, 1436, 1630, 1985, 1897, 1551, 1296, 1282, 1735, 1320, 1659, 1271, 1380, 1274, 1876, 1492, 1298, 1399, 1692, 1265, 1555, 1337 ];
```

5. Se necesita un crear un string con el siguiente formato de fecha:

```js
'dd de MES de YYYY Son las HH horas con mm minutos. En 10 minutos la fecha será' +
'dd de MES de YYYY y serán las HH horas con mm minutos'
```
Crear una función que reciba un objeto `Date` y que devuelva dicho string de acuerdo a la fecha y hora del objeto.

Omitir `la fecha será dd de MES de YYYY y` si la fecha no cambia. 

# Avanzado (mas o menos :v)

1. Utilice el siguiente servicio [TODOS](https://jsonplaceholder.typicode.com/todos/)
Utilice la información para renderizar el listado en pantalla. Mostrar solo el title. Si la tarea está completada, dar información al usuario de que es así.

2. De lo anterior, permita completar tareas a través de un botón. También eliminar tareas y agregar nuevas tareas. Las tareas se almacenarán en memoria.

3. De lo anterior, ahora almacene las tareas en el localstorage para que cuando se refresque la página no se pierda la información. La lista de del servicio solo se cargará cuando se ingrese por primera vez a la página.


