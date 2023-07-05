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

#### length

El metodos length se utiliza para devolver el numero de caracteres de una cadena, incluyendo espacios.

```javascript
let texto = "hola mundo";
console.log(texto.length); //10
// la variable texto tiene un total de 10 caracteres
```

#### Acceder a lo caracteres de la cadena

podemos acceder a una cadea usando su indice, el conteo del indice de una cadean comienza en 0

![1688484200477](image/tipodedatos/1688484200477.png)

```javascript
let string = "Hola Juan";
let firstLeter = string[0];

console.log(firstLeter); // H
```

#### toUpperCase()

Este metodo cambia la cadena a letras mayúsculas.

```javascript
let string = "hola mundo";
console.log(string.toUpperCase()); // HOLA MUNDO
```

#### toLowerCase()

Este metodo cambia la cadena a letras minusculas.

```javascript
let string = "HOLA MUNDO";
console.log(string.toLowerCase()); // hola mundo
```

#### substr()

Este metodo devuelve una parte de la cadena original, para esto necesitamos dos argumentos, el indice incial y la longitud de la cadena.

```javascript
let string = "hola mundo";
console.log(string.substr(4,8));
```

#### slice()

El metodo slice tambien extrae un subcadena, pero a diferencia del metodo substr, este nesecita el indice inicial y final.

```javascript
let miString = "Hola mundo";
console.log(miString.slice(1,4)); // ola
```

#### split()

El metodo split divide la cadena en partes segun un carecter indicado.

```javascript
let string = "30 dias con javascript";
console.log(string.split(" ")); // Se van a separar la cadena segun el caracter " ", el resultado se guadara en un array;
// ["30","dias","con","javascript"]
```

#### trim()

Elimina los espacio del final y del comiezo de una cadena.

```javascript
let string = "  hola mundo  ";
console.log(string); //   hola mundo  
console.log(string.trim()); // hola mundo
```

#### includes()

Toma el argumento ingresado y verifica que la cadena ingresada exista como subcadena en la cadena principal.

```javascript
let string = "hola mundo";

console.log(string.includes("ho")); // True
console.log(string.includes("halo")); // False
```

#### replace()

El metodo replace remplanza una subcadena por otra subcadena que esta en la cadena principal

```javascript
let string = "hola mundo";

console.log(string.replace("hola","chao"));
// chao mundo
```

#### indexOf()

Este metodo toma una cadena o caracter y busca si esta existe en la cadena principal, y devuelve la primera posicion de donde esta ubicada.

```javascript
let string = "Hola mundo";

console.log(string.index.Of("ola")); /1
```

Recordar que este metodo se usa solo para datos tipo String.

#### lastIndexOf()

Toma una subcadena y la busca en una cadena, devuelve la ultima posicion de ka subcadena buscada, y si no existe devuelve -1.

```javascript
let string = "I love javascript. If tou do not love javascript what else can you love.";

console.log(string.length);
console.log(string.lastIndexOf("love"));
```

#### concat()

El metodo concat() concatena varias subcadenas y las une en una sola cadena.

```javascript
let string = "30";
console.log(string.concat("dias","con","javascript"));
```

#### startsWith() , endsWith()

toma una cadena y verifica si comienza o termina con la subcadena ingresada.

```javascript
let string = "Hola amigos de git";

console.log(string.starstWith("Hola")); //True
console.log(string.starstWith("hola")); //False

console.log(string.endsWith("git")); //True
console.log(string.endsWith("Git")); //False
```

#### search()

Este metodo tomo el valor de una subcadena como argumento y devuelve el indice de la primera concidencia.
Recordar que el valor de la busqueda puede ser una cadena o una patron de exprecion regular(**RegExp**),una expresión regular es una secuencia de caracteres que define un patrón de búsqueda

```javascript
let string = "Hola este es mi primer texto en javascript";
console.log(string.search("primer")); 
console.log(string.search("/hola/gi"))
```

La ultima exprecion /gi, son modificadores que afectan el comportaminieto de la expresion al realizar la busqueda.

* `g` (global): Realiza una búsqueda global en toda la cadena de texto y encuentra todas las coincidencias en lugar de detenerse después de la primera coincidencia.
* `i` (ignore case): Realiza una búsqueda insensible a mayúsculas y minúsculas, lo que significa que ignora las diferencias entre letras mayúsculas y minúsculas al realizar una coincidencia.
* `m` (multiline): Cambia el comportamiento del inicio y fin de línea (`^` y `$`) para que coincidan con los límites de línea en lugar de los límites de toda la cadena. Esto es útil cuando se trabaja con cadenas de texto que contienen múltiples líneas.
* `s` (dotAll): Cambia el comportamiento del metacarácter `.` para que coincida con cualquier carácter, incluidos los caracteres de nueva línea (`\n`). Por defecto, el metacarácter `.` no coincide con los caracteres de nueva línea.
* `u` (unicode): Habilita el modo unicode para tratar correctamente los caracteres unicode en una cadena de texto.
* `y` (sticky): Realiza una búsqueda "sticky" que coincide solo con la posición siguiente a la última coincidencia exitosa.
* `d` (Unicode property escapes): Habilita el uso de escapes de propiedades Unicode en una expresión regular.

#### repeat()

Toma un numero como argumento y devuelve una cadena repetida por el numero ingresado.

```javascript
let string = "hola"
console.log(string.repeat(3)); //holaholahola
```

### Comprobar el tipo de dato

Para saber que tipo de dato que estamos utilizando, usaremo el metodo typeof.

```javascript
let string = "Hola mundo";
console.log(typeof string);

let numero = 12;
console.log(typeof numero);

```

### Cambio del tipo de datos

- Casting: el lenjuage de js nos proporciana varios metodo para ponder convertir un tipo de dato a otro.
  - Cadena a Int
    Podemos convertir una cadena en un numero, con los metodo parseInt(), Number o con el operador (+).

    ```javascript
    let numer = "10";
    let numInt1 = parseInt(num);
    console.log(numInt1); // 10

    let numInt2 = Number(num);
    console.log(numInt2); // 10
    ```
  - Cadena a Flotante
    Podemos convertir valores tipo flotante en cadenas de texto, mediante los metodos parseFloat(), Number o con el signo (+).

    ```javascript
    let num = 9.32;

    let numFloat1 = parseFloat(num);
    console.log(numFloat1);

    let numFloat2 = Number(num);
    console.log(numberFloat2);
    ```
  - Flotante a Int

    Para convertir un numero de float a int, solo hay existe el metodo parseInt.
  - ```javascript
    let num = 9.4;
    let numInt = parseInt(num);

    console.log(numInt);
    ```

### Numerico

Los datos de tipo numerico son todos lo numero que nos podamos imaginar, tanto enteros como valores decimales, este tipo de dato acepta opraciones matematicas.

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

Los datos no primitivos no almacenan un valor directamente, sino que contienen referencias a otros valores o variables; algunos ejemplos de datos no primitivos son :

- Objetos (Object)
- Arreglos (Array)
- Funciones (Funtions)
- Fechas (Dates)

Los tipos de datos no primitivos son modificables o mutables, como por ejemplo creamos una matriz de numeros y depues podemos modificar alguno de sus valores; recordar que una matriz en js no solo puede contener un solo tipo de dato sino tambien puede contener diferente tipos de datos, y para acceder a cualquier dato de una matriz se realizara mediante su indice de ubicacion que comeinza desde el cero.

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
