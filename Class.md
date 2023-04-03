# Content 
* ✍🏻 Week 1
    * [Class 1: Markdown](#class-1-markdown)
    * [Class 2: Git](#class-2-git)
    * [Class 3: HTML](#class-3-html)
    * [Class 4: CSS](#class-4-css)
* 👓 Week 2
    * [Class 1: Introducción JS](#class-1-js-introduction)
    * [Class 2: JS POO](#class-2-js-poo)
    * [Class 3: HTML Semantic](#class-3-html-semantic)
    * [Class 4: Forms HTML](#class-4-forms-html)
* 🐛 Week 3


# ✍🏻 WEEK 1
Class 1 Markdown
=================
This is a lith language for create content, this language is easy to read from source.

* https://daringfireball.net/projects/markdown/syntax
* https://es.markdown.net.br/sintaxis-extendida/
* https://readme.so/

![#00d700](https://via.placeholder.com/15/00d700/000000?text=+) Image by color.
## Task
- [ ] Different between terminal emulator and terminal application.
- [x] Update my profile in Github. [here](https://github.com/yrguativa)
- [x] Table with commands learning today.
- [x] Alias commons and util by me.

### Tabla
| Command   | Description                   |
| -------   | -----------:                  |
| date      | Print to date now             |
| calc      | Print calendar                |
| ctrl + u  | Clear line terminal now       |
| ctrl + a  | Mover to start terminal       |
| ctrl + b  | Mover to next word terminal   |

### Alias
- alias rrp='npm run dev' : run project (React Run Project)
- alias mds='npx @11ty/eleventy --serve': Create web page from file .md  (Markdown Server)

### 11ty
This plugin create web page from file markdown.

1. Create content with plugin
```console
npx @11ty/eleventy --serve
```

2. Open browser with {host:port}/{filename}/

Class 2 Git
============

## Task
- [x] Different between distributed and centralized repository

For centralized repositories, changes synced to only one place (remote repository) and  when the repository is distributed, changes are synced to other repositories (clients) that are on the network (not just one place).

Class 3 HTML
============
Run vite by html file
```console
npx vite dev
```

## Void Elements
in html the are voids elements as < br/> or < hr/>

## Links
1. Absolute 

https://en.wikipedia.org/wiki/sweden 

<details>
<summary>URL Parts</summary>
<table>
<table>
<tr>
    <td>Schema</td>
    <td>https://</td> 
</tr>
<tr>
    <td>Domain</td>
    <td>en.wikipedia.org</td> 
</tr>
<tr>
    <td>Path</td>
    <td>/wiki/sweden</td> 

</tr>
</table>
</table>
</details>

2. Relative

about.html

3. Root Relative 

/about.html

Class 4 CSS
===========
Hojas de estilos, propiedasdes y unidades en CSS

- **Selector**: body
- **Propiedasd**: background, font-size
- **Valores**: tomato, 16px 
- **Unidad**: px

## Modelo de Caja

Tipos de **display**:
- Bloque: Uno elemento debajo del otro. El ancho del contenedor, la altura segun el content. **Collapso de los margenes de dos elementos en bloque** (cuando hay dos elementos en bloque seguido no se suma su margenes (20 px margen del elemento superior y 20px del elemento inferion para dar un margen 40px, pero por el collapso solo se coloca 2o0px))
- Linea: Un elemento al lado el otro.  El ancho segun el contenido, no afectan el espacio vertial. **El margen vertical no se ve afectado**

### box:
funciona de la siguiente manera: -> Margin -> border -> padding -> content

> **Box-sizing property** asegura que el tamaño sea el correcto entre el ancho, padding, y el borde.

## Selectores
- **Adyacente:** .primero + .segundo
- **Hijo:** .padre > .hijo
- **Descendiente:** .abuelo .bisnieto
- **Hermano:** .hermano ~.hermana

## Reference
* [Web Design in 4 minutes](https://jgthms.com/web-design-in-4-minutes/) 

# 👓 WEEK 2

Class 1 JS Introduction
=======================

* Una **Expresión** es una combinación de valores, variables, operadores y funciones que se evalúa para producir un resultado.

* Una **Sentencia** es una instrucción que realiza una acción en el programa. Las sentencias pueden cambiar el estado de las variables, realizar operaciones de entrada/salida, controlar el fuljo de ejecución del programa, entre otras acciones.

* Los **Operadores** son símbolos o palabras reservada q    ue se utilizan para realizar operaciones o comparaciones entre valores o variables.

## Valores Primitivos (7)
* **Booleans** ( true y false ) 
* **Numbers** ( -100 , 3.14 )
* **Strings** ( "hola" , 'abracadabra' )
* **Symbols** ( Symbol() )
* **BigInts2** ( 10n )
* **Undefined** ( undefined )
* **Null** ( null )

## Los valores "falsy":
* **false**: el valor booleano falso. 
* **0**: el número cero.
* **-0**: el número cero negativo. 
* **0n**: elBigIntcero. 
* **"":** la cadenade texto vacía.
* **null**: un valor nulo.
* **undefined**: un valor no definido.
* **NaN**: un valor que representa "Not a Number".

>  Cualquier otra cosa que no sea "falsy" es "truthy":
* **true**: el valor booleano verdadero.
* **1**: cualquier número diferente de cero se considera verdadero.
* **"false"**: cualquier cadena de texto no vacía se considera verdadera.
* **[]**: un arreglo vacío se considera verdadera.
* **{}**: cual quier objeto vacío se considera verdadero.
* **function (){}**: cualquier función definida se considera verdadera.
* **new Date()**: cualquier objeto de fecha se considera verdadero.
* **42n**: cualquier BigInt diferente de cero se considera verdadero.

> Los valores "Nullish" son *null* y *undefined*
## Exercise
Hugo, Paco y Luis tienen una cantidad desconocida de monedas cada uno.

Sabemos que Paco tiene el doble de monedas que Hugo y que Luis tiene 10 monedas más que Paco.

Si los tres juntos tienen un total de 85 monedas.

### ¿Cuántas monedas tiene cada uno?

```javascript
// Asignamos la cantidad de monedas de Hugo, este valor es el que tienes que resolver. 
let hugo = 0; // solution: 15

// Calculamos la cantidad de monedas de Paco y Luis en función de Hugo.
let paco = 2 * hugo;
let luis = paco + 10;

// Sumamos las cantidades de monedas de los tres amigos 
let total = hugo + paco + luis;

if (total === 85) {
    console.log("Hugo: " + hugo)
    console.log("Paco: " + paco)
    onsole.log("Luis: " + luis)
}
```

## Exercise 2
¿Cómo puedo implementar una expresión para verificar si un valor es un objeto?
```javascript
typeof obj === "object" && obj != null
```

Class 2 JS POO
==============
Creation of objects in JavaScript

```javascript
let human = {
    name: 'Yilmer',
    last_name: 'Guativa',
    age: 29
} 

console.log(human);

// add property and read property as array
human.id = Symbol('yrguativa');
console.log(human['id']);

// delete properties of object
delete human.last_name;
```
## Types of functions
The functions en JS are first class  (that is the function are stored in the variables).

* Function Statement
```javascript
function walk(who) // *who* parameter of function
{ 
    console.log(´I am {who} and I am walking´);
}

walk('Yilmer'); // 'yilmer' is argument of function
```

* Function Expression
```javascript
const walk = function () {
    console.log("I'm walking");
}

walk();
```

## Puras y Impuras
**PURAS**
* No tiene efectos secundarios: No modifica ningún estado fuera de su alcance, como variables globales o referencias.
* Es determinista: Esto significa que dada la misma entrada, siempre producirá la misma salida.

## Los operadores lógicos
- **OR: a || b || c** => retorna el primer valor verdadero
- **AND: a && b && c** => retorna el primer valor falso
- **NOT: !a** => retorna el valor contrario booleano

## Operador Ternario ?
```javascript
let msg = age >= 18 ? "Adult" : "Young";
```
## Book
<img src="https://github.com/getify/You-Dont-Know-JS/raw/2nd-ed/get-started/images/cover.png" width="200">

This books is in [github](https://github.com/getify/You-Dont-Know-JS)
## Ejercicio
¿Cómo puedo implementar una expresión para verificar si un valor es un array?
```javascript
// option 1
typeof x === 'object' && x != null && x.__proto__  == [].__proto__

// option 1
Array.isArray(x)
```
Class 3 Html Semantic
=====================
Validated html semantic util: https://validator.w3.org/nu/ 

## Qué es el HTML Semántico

Es la práctica de utilizar etiquetas HTML que dan significado y estructura a los contenidos de una página web.

Un `<article>` es un "contenido" que tiene relación con otras 1 "contenidos" a su alrededor.

```html
<section>
    <h1>Articulos de frutas:</h1>
    <article>
        <header>
            <h2>Manazana</h2>
        </header>
        <p>La manzana es el fruto pomáceo del manzano...</p>
    </article>
    <article>
        <h2>Naranja</h2>
        <p>La naranja es un híbrido de origen ancestral cultivado...</p>
    </article>
    <article>
        <header>
            <h2>Banano</h2>
        </header>
        <p>Los plátanos vienen en una variedad de tamaños y colores....</p>
        <footer>
            31/03/2023
        </footer>
    </article>
</section>
```

## time y address en HTML

```html
<p>
    Por Guillermo Rodas. Publicado
    <time datetime='2023-03-13 15:00-0800'>Marzo 13th</time>
</p>

<footer>
    <p>Este articulo falso fue escrito por alguien.</p>
    <address>
        Por favor contacte a
        <a href='mailto:me@guillermorodas.com'>Guillermo</a>
        para preguntas sobre el articulo.
    </address>
</footer>
```

## Los tags figure , figcaption e img
> If image have relationship to article should be into ```<figure>```.

```javascript
<section>
        <h2>El esquema del documento</h2>
        <p>
            HTML5 incluye varios elementos de "contenido de sección" que afectan el contorno del documento
        </p>
        <figure>
            <img src='semantic-elements.png'
                alt='Diagrama del uso de elementos semanticos '/>
            <figcaption>Elementos semánticos en HTML</figcaption>
        </figure>
</section>
```
Sobre la etiqueta picture Respecto al tag ```<picture>``` este se suele usar cuando necesitamos cargar múltiples fuentes de imágenes basado en temas de diseño responsivo, pero no agregar valor semántico en si, es un remplazo a img cuando es necesario.

Class 4 Forms HTML
==================

## Los forms clásicos en HTML
```javascript
<form action='/server' method='get' class='form'>
</form>
```
## Inputs en los formularios de HTML
- Input text, Email. 
- Radio buttons
- Select elements
- Textareas
- Checkboxes:
### Examples:
```html
<fieldset>
    <legend>Presupuesto</legend>
    <input id="10000" name="budget" type="radio" value="10000"><label for="10000">$10.000</label>
    <input id="5000" name="budget" type="radio" value="5000"><label for="5000">$5.000</label>
    <input id="1000" name="budget" type="radio" value="100"><label for="1000">$1.000</label>
</fieldset>

<label for="terms">
    <input id="terms" name="terms" type="checkbox" required>
    <span>Acepto los terminos y condiciones</span>
</label>
```
## Controles moderlos para formularios
1. **email**: Acepta una dirección de correo electrónico. Ejemplo: `<input type="email" name="email">`

2. **url**: Acepta una URL. Ejemplo: `<input type="url" name="website">`

3. **number**: Acepta números enteros o decimales. Puedes especificar atributos adicionales como min,
max y step para restringir y controlar el rango de valores permitidos. Ejemplo: `<input type="number" name="age" min="1" max="100">`

4. **range**: Acepta un rango de números y presenta un control deslizante en la interfaz de usuario.
También puedes usar atributos como min, max y step. Ejemplo: `<input type="range" name="volume" min="0" max="100">`

5. **date**: Acepta una fecha y muestra un selector de fecha en la interfaz de usuario. Ejemplo: `<input type="date" name="birthdate">`

6. **time**: Acepta una hora y muestra un selector de hora en la interfaz de usuario. Ejemplo: `<input type="time" name"appt_time">`

7. **datetime-local**: Acepta una fecha y hora y muestra un selector de fecha y hora en la interfaz de
usuario. Ejemplo: `<input type="datetime-local" name="meeting">`

8. **color**: Acepta un valor de color y muestra un selector de color en la interfaz de usuario. Ejemplo:
`<input type="color" name="favorite_color">`

9. **search**: Acepta una cadena de búsqueda y puede mostrar sugerencias de búsqueda en algunos navegadores. Ejemplo: `<input type="search" name="query">`

10. **tel**: Acepta un número de teléfono, aunque no realiza una validación específica del número de teléfono. Se utiliza principalmente para mejorar la experiencia del usuario en dispositivos móviles, mostrando un teclado numérico adecuado. Ejemplo: `<input type="tel" name="phone">`

## El formato JSON
JSON (JavaScript Object Notation) es un formato de intercambio de datos ligero y fácil de leer tanto para humanos como para máquinas.

Se utiliza ampliamente para transmitir datos en aplicaciones web entre el cliente y el servidor, así como:

```json
{
    "nombre": "Juan Pérez",
    "edad": 30,
    "ocupacion": "Ingeniero de software",
    "direccion": {
        "calle": "Avenida de la Tecnología",
        "numero": "123",
        "ciudad": "Ciudad Futuro",
        "codigoPostal": "54321"
    },
    "hobbies": [ 
        "Leer", 
        "Programar",
        "Ciclismo"
    ]
}
```
## ¿Qué es el DOM?
El DOM (Document Object Model) es una representación en forma de árbol de los elementos y la estructura de una página web.

El DOM es una interfaz de programación que permite a los desarrolladores interactuar y manipular el contenido, la estructura y el estilo de una página web utilizando JavaScript.

## ¿Qué es el CSSOM?
El CSSOM (CSS Object Model) es una representación en forma de árbol de todos los estilos CSS asociados con una página web.

Al igual que el DOM representa la estructura y el contenido de una página web, el CSSOM representa la información de estilo de la página.
