# Tipos de Datos

```javascript
mi_recipiente = "papel"
console.log(mi_recipiente)
mi_recimiente = 0"hola"
console.log(mi_recipiente)
```

## Datos Primitivos

Los datos de tipo primitivos en JS incluyen:

1. Numeros
2. Cadenas
3. Booleanos
4. Datos Especiales

Los datos primitivos  son tipos de datos inmutables, una vez declarados no se pueden modificar.

Ejemplo:

```javascript
let word = "hola amigo";
```

si intentamos modificar algun caracter de este mismo, no devolvera un error; aclara que es muy diferente reacsignar el valor de la variable a modificarse este.

```
word[0] = "y";
```

---

### String

Un String son cadenas de texto, que estan englobadas por comillas simples, dobles o triples

```javascript
mi_string = "mi cadena de texto"
mi_numero = "19"
```

#### Concatenación de Cadenas

La palabra contatenación hace referencia en programacion de unir o conectar, dos o mas datos tipo string para formar uno mas grande.

```javascript
let nombreCompleto = primerNommbre + " " + Apellido; // para contatenar se usa el operado + unir los strigs
console.log(nombreCompleto);
```

##### Concatenar usando el operador suma

Esta forma es la mas clasica de concatenar varias cadenas de codigo, pero es de las mas tediosa y propensa de errores.

```javascript
let primerNombre = "Miguel";
let espacio = " ";
let apellido = "Dominguez";

let nombreCompleto = primerNombre + espacio + apellido;

console.log(nombreCompleto);
```

##### Cadenas literales largas

Podemos unir una cadena de varias lineas, señalando con '\\' que el texto sigue en la siguiente linea.

```javascript
const parrafo =
"Mi nombre es Asabeneh Yetayeh. Vivo en Finlandia, Helsinki.\
Soy profesora y me encanta enseñar. Enseño HTML, CSS, JavaScript, React, Redux, \
Node.js, Python, Data Analysis y D3.js para cualquier persona interesada en aprender. \
A fines de 2019, estaba pensando en expandir mi enseñanza y llegar a \
a la audiencia global y comencé un desafío de Python del 20 de noviembre al 19 de diciembre.\
Fue una de las experiencias más gratificantes e inspiradoras.\
Ahora, estamos en 2020. Disfruto preparando el desafío 30DaysOfJavaScript y \
Espero que tú también estés disfrutando.";

console.log(parrafo);
```

##### Literales de Plantilla

Son cadenas de texto donde podemos inyectar datos como expresiones dentro de cadena, gracias a `${dato_1}`.

```javascript
let a = 2 ;
let b = 3;

cosole.log('la suam de ${a} y ${b} es ${a+b}')
```

### Secuencia de Escape de Cadenas

Son `\ mas algunos caractere` que se usan para salir del flujo normal de una cadena de texto y hacer ciertas cosas.

* \n salto de linea
* \\\Barra inertida
* \\' una comilla
* \\" comillas doble+

### Métodos de Cadena

---

### Numerico

Los datos de tipo numerico son todos lo numero que nos podamos imaginar, tanto enteros como valores decimales, este tipo de dato acepta opraciones matematicas.2.

```javascript
mi_numero = 133
otro_numero = 12.4
```

#### El Objeto Math

En JS existe el objeto matematico que proporcina mcuhos metodos para trabajar con valores numericos.

```javascript
const PI = Math.PI;

console.log(PI) //3.1415926
// Math.round - redondea el valor al más cercano
console.log(Math.round(PI)); // 3
console.log(Math.round(9.81)); // 10

//Math.floor -  redondea hacia abajo
console.log(Math.floor(PI)); // 3
//Math.ceil - redondea hacia arriba
console.log(Math.ceil(PI)); // 4

// Devuelve el minimo valor
console.log(Math.min(-5,3,20,4,5,10)); // -5
// Devuelve el maximo valor
console.log(Math.max(-5,3,20,4,5,10)); // 20

//Math.random() crea un numero aleatorio entre 0 y 0.9999
const randNum = Math.random();
console.log(randNum);

// Math.abs nos da le valor absoluto
console.log(Math.abs(-10)); // 10

//Raíz cuadrada
console.log(Math.sqrt(100)); // 10

// Elevar un numero a un exponente
console.log(Math.pow(3,2));

//Logaritmo
// Logaritmo Natural, con base E en x
console.log(Math.log(2)) //0.693147

// otra manera que Devuelva el logaritmo natura
console.log(Math.LN2); //0.693147

// Trigonometria
Math.sin(60);
Math.cos(3)

```

### Boolean

Los datos de tipo boolean, solo abarcan dos posibles valores:

- true
- false

```javascript
mi_boolean_1 = true
mi_boolean_2 = false
```

### Tipos de Datos Especiales

Estos tipos de datos aparecen cuando no se difinio la variable o no existe.

Cuando declaramos una variable tenemos 3 formas de hacerlo `var - let - const`,

los casos de tipos de especiales son:

- Undefined .- son variables que nunca le direron un valor, no definido.
- Null .-
- Nan

## Tipos de Datos no Primitivos

Los Datos no Primitivos son:

- Objetos
- Funciones
- Matrices

Los tipos de datos primitivos son modificables o mutables, como por ejemplo creamos una matriz de numeros y depues podemos modificar alguno de sus valores; recordar que una matriz en js no solo puede contener un solo tipo de dato sino tambien puede contener diferente tipos de datos, y para acceder a cualquier dato de una matriz se realizara mediante su indice de ubicacion que comeinza desde el cero.

```javascript
let numeros = [1, 2, 3, "cuatro"];
numeros[0] = 5; // se modifica el indice 0 que tenia coimo valor 1.
console.log(numeros) // [5, 2, 3, "cuatro"];
```

Ahora un cosa mas sobre los datos primitivos es que estos no pueden ser comprados por el operador de igualdad, asi sus propiedades y valores sean iguales.

```javascript
let usuarioUno = {
	name : "Miguel",
	role : "admin",
	activate : true,
};

let usuarioDos = {
	name : "Miguel",
	role : "admin",
	activate : true,
};

console.log(usarioUno == usuarioUno) // false
```

Como dato, los valores no primitivos se conocen como tipos de referencia, porque se comparan por referencia en lugar de por valor. Dos objetos son estrictamente iguales si refiere al mismo objeto subyacente.

```javascript
let nums = [1,2,3];
let numeros = nums;

console.log(nums == numeros); //falks

let usuarioUno = {
	name : "Miguel",
	role : "admin",
	activate : true,
};

lef usuarioDos = usuarioUno;

console.log(usuarioDos == usuarioUno) // true
```
