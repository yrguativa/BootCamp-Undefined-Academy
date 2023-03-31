# Content 
* Semana 1
    * [Class 1: Markdown](#class-1-markdown)
    * [Class 2: Git](#class-2-git)
    * [Class 3: HTML](#class-3-html)
    * [Class 4: CSS](#class-4-css)
* Semana 2
    * [Class 1: Introducción JS](#class-1-js-introduction)
    * [Class 2: JS POO](#class-2-js-poo)

# SEMANA 1
Class 1 Markdown
=================
This is a lith language for create content, this language is easy to read from source.

* https://daringfireball.net/projects/markdown/syntax
* https://es.markdown.net.br/sintaxis-extendida/

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

## Selectores
- **Adyacente:** .primero + .segundo
- **Hijo:** .padre > .hijo
- **Descendiente:** .abuelo .bisnieto
- **Hermano:** .hermano ~.hermana

## Reference
* [Web Design in 4 minutes](https://jgthms.com/web-design-in-4-minutes/) 

# SEMANA 2

Class 1 JS Introduction
=======================

* Una **Expresión** es una combinación de valores, variables, operadores y funciones que se evalúa para producir un resultado.

* Una **Sentencia** es una instrucción que realiza una acción en el programa. Las sentencias pueden cambiar el estado de las variables, realizar operaciones de entrada/salida, controlar el fuljo de ejecución del programa, entre otras acciones.

* Los **Operadores** son símbolos o palabras reservada q    ue se utilizan para realizar operaciones o comparaciones entre valores o variables.


## Exercise
Hugo, Paco y Luis tienen una cantidad desconocida de monedas cada uno.

Sabemos que Paco tiene el doble de monedas que Hugo y que Luis tiene 10 monedas más que Paco.

Si los tres juntos tienen un total de 85 monedas.

### ¿Cuántas monedas tiene cada uno?

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


