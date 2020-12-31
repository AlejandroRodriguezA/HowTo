# JavaScript de [Soy Dalton](https://youtu.be/z95mZVUcJ-E)

Estas son mis anotaciones del curso de Dalton, y esta en fomato **Markdown**, <small>[aqui](https://markdown.es/)</small> puedes ver más información sobre que es markdown y las diferentes formas de visualizar el documento, quizas lo más facil es verlo desde **Github.** 

***Nota:***   
	* <small>[video](https://youtu.be/z95mZVUcJ-E)</small> son links al video del curso de Dalton al momento donde explica el tema.  
	* <small>[más info](https://developer.mozilla.org/en-US/)</small> son links a documentación, usualmente a  mozilla developer, que profundiza el tema explicado. Existe la documentacion en español, por si la prefieren.

# Indice:
1. [Capitulo 1:](#Capitulo1)
	* [Introducción.](#Introduccion)
	* [Editor de Texto.](#Editor)
	* [Usos de Java.](#Usos)
	* [Formas de incluir JS.](#Enlace)
	* [Variables.](#Variables)
	* [Pedir datos con prompt.](#Prompt)
	* [Operadores.](#Operadores)
	* [Concatenacion.](#Concatenacion)
	* [Camel Case.](#Camel)
	* [Condicionales](#Condicionales)
2. [Capitulo 2:](#Capitulo2)
	* [Arrays.](#Arrays)   
	* [Arrays Asociativos.](#Asociativos)
	* [Bucles: (While,For).](#Bucles)
	* [Funciones.](#Funciones)
	* [ForEach.](#ForEach)
	
3. [Capitulo 3:](#Capitulo3)
4. [Capitulo 4:](#Capitulo4)

	* [Método de Cadenas](#MetodosCadenas)  
		- [concat()](#concat)
		- [startWith()](#startWith)
		- [endWith()](#endWith)
		- [includes()](#includes)
		- [indexOf()](#indexOf)
		- [lastIndexOf()](#lastIndexOf)
		- [repeat()](#repeat)
		- [split()](#split)
		- [substring()](#substring)
		- [toLowerCase()](#toLowerCase)
		- [toUpperCase()](#toUpperCase)
		- [toString()](#toString)
		- [trim](#trim)
		- [valueOf](#valueOf)

	* [Método de Arrays](#MetodosArrays) 

		1. Transformadores: 
			- [pop().](#pop)
			- [push().](#push)
			- [shift().](#shift)
			- [reverse().](#reverse)
			- [unshift().](#unshift)
			- [sort().](#sort)
			- [splice().](#splice)  
			 
		2. Accesorios:
			- [join().](#join)
			- [slice().](#slice)
			
		3. De Repetición:
			- [filter().](#filter)
			- [forEach().](#forEach)
	* [Objeto Math](#ObjetoMath)
		1. [Metodos.](#MetodosMath)
		El objeto Math tiene muchos metodos, aqui algunos de utilidad.[ver mas metodos](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)
			- [sqrt().](#sqrt)
			- [cbrt().](#cbrt)
			- [max().](#max)
			- [min()](#min)
			- [random().](#random)
			- [round().](#round)
			- [fround().](#fround)
			- [floor().](#floor)
			- [trunc().](#trunc)
		2. [Propiedades.](#PropiedadesMath)
		Hay muchas constantes que se pueden usar, [ver mas informacion](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math). Por ejemplo:
			- [PI.](#PI)


5. [Capitulo 5:](Capitulo5)

	- [Consola de JavaScript (console).](#Consola)
	- [Metodos de registro en la consola.](#MRegistro)
	- [Metodos de conteo en la consola.](#MConteo)
	- [Metodos de agrupacion en la consola.](#MAgrupacion)
	- [Metodos de temporizacion en la consola.](#MTemporizacion)

	
6. [Capitulo 6:](#Capitulo6)

	- [El DOM (Document Object Model).](#DOM)
	- [Metodos de seleccion de elementos.](#MSeleccionElementos)
	- [Metodos de atributos de un elemento.](#MAtributos)
	- [Atributos globales.](#AtributosGlobales)
	- [Atributos de inputs.](#AStyle)
	- [Propriedad Style.](#PropiedadStyle)
	- [Clases, classList y sus metodos.](#ClassList)
	- [Creacion de Elementos.](#CreacionElementos)
	- [Obtencion y modificadores de childs.](#ModificarChilds)
	- [Metodos de childs (hijos).](#MChilds)
	- [Propiedades de parents (Padres).](#PropiedadesPadres)
	- [Propiedades de siblings (Hermanos).](#PropiedadesHermanos)
	- [Nodos, una propiedad extra.](#PropiedadExtra)     
	

- - - 

	
<a name="Capitulo1"></a>  
##Capitulo 1: 
* <a name="Introduccion"></a>Introduccion: <small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=445s)</small>
	- JS es un leguaje de programacion Interpretado que se difiere a un leguaje compilado, es decir, se ejecuta en el navegador en el inteprete.  
	- Es Orientado a objetos.  
	- Es Imperativo. Se va ejecutando linea a linea.
	- Es Case sensite.
	- Basado en prototipos / instancias / clases.
	- Tipado debil. Significa que el valor de los datos y variables puede ir variando durante el tiempo.Se define como string al comienzo y luego se redefine como interger.
	- Lenguaje dinnamico. El dato se ajusta a la variable.
	- Esta construido sobre ECMASCRIPT (5, 6, 7, 8, Next).

* <a name="Editor"></a>Editor de Texto:Esta usando Sublime Text 3, su configuracion (plugins) son:	<small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=940s)</small>
	- shift+command+P --> install control Package. Esta opcion es para Mac. 
	- BlackBird-ColorScheme
	- Brogrammer
	- Set UI
	- liveReload
	- ColorHelper
	- ColorPicker
	
* <a name="Usos"></a>Para que se usa:	<small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=1346s)</small>
	- Dinamismo de los sitios web
	- Servidor en NodeJS
	- Tecnologias Frontend como Angular, React o Vue.
	- Mobile Apps.
	- Desktop Apps.
	- Inteligencia Artificial. No es muy usual, pero se puede usar.
	
* <a name="Enlace"></a>Como enlazar JS:	<small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=1346s)</small>
	- En linea:   
	
		```html
		<h1 onclick="alert('hola')"> Saludo </h1>	 	```    
	
	- Dentro de la etiqueta:   
	 
		```html
		<script type="text/javascript">
			alert('Hola desde script');
		</script>   
		```
		    
	- Enlazado desde un archivo externo:  
	
		```html
		<script src="codigo.js" type="text/javascript"></script>
		```
		
	- Con un Require. Buscar inforamcion pues el no lo explica.
* <a name="Variables"></a>Variables:	<small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=1672s)</small>
	- Hay tres formas de declarar la variables (var, let, const)
		* var: alcance global.
		* let: alcance local.
		* const: es una constante.  
		***Nota***: Si no se especifica, la variable es definida de forma global (var).  
	- Casos especiales:
		- Undefined: Variable definida pero no inicializada.
		- Null: Variable definida e inicializada con valor vacio o null.
		- Nan: Variables no son numeros y no se pueden realizar operaciones de numeros, viene del ingles No A Number.
	- Multiples Variables.	<small>[video](https://youtu.be/z95mZVUcJ-E?t=2429)</small>
	- Hoisting: <small>[video](https://youtu.be/z95mZVUcJ-E?t=2513)</small>
	-  ***Nota***: Los errores se muestran en consola, no en la paguina. **option+command+j** para mostrar la consola de JS.
*  <a name="Prompt"></a>**prompt**("mensaje")	<small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=2774s)</small>-> Esta funcion permite ingresar informacion por el usuario.

```js
let nombre = prompt("Dime tu nombre");
alert ("hola " + nombre);
```   
* document.write(vatiable); --> Escribe la variable en la pag.web.

*  <a name="Operadores"></a>Operadores:	<small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=2991s)	</small>
	- De asignacion. <small>[más info](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Operadores/Assignment_Operators) </small> 
		* x = y
		* x += y
		* x -= y
		* x *= y
		* x /= y
		* x %= y  
		
	```js
	let numero = 10;
	numero += 5;
	document.write(numero);
	// Da como resultado 15
	// numero += 5 es igual que numero = numero +5
	numero -= 5;
	// Es igual que numero = numero - 5
	numero %= 6;
	// El resultado es 4.
	// Numero es 10, al dividirlo entre 6, el resto es 4, asi que, numero %= 6 es igual al resto de 10 % 4.
	numero **=3
	// El resultado es 1000 = 10^3.	
	```
	**Nota**: document.write(variable); --> Escribe la variable en la pag.web.
		
	- Aritmeticos.<small>[más info](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Math)</small>  
		* Suma.  
		
		```js
		numero1 = 10;
		numero2 = 5;
		resultado = numero1 + numero2;
		// resultado = 11;
		resultado = numero1++
		// Resultado = 16.
		```
		* Resta.
		
		```js
		numero1 = 10;
		numero2 = 5;
		resultado = numero1 - numero2;
		// resultado = 5;
		resultado = numero1--
		// Resultado = 9.
		```
		
		* Multiplicación.
		* División.
		* Resto.
		
* <a name="Concatenacion"></a>Concatenacion:	<small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=2991s)</small> 
	- **Para forzar** a que se concatene : frase = "" + numero + numero1 ***fuerza  a que sea string***
	
	```js
	let numero = 5;
	let numero2 = 5;
	resultado = "" + numero + numero2;
	document.write(resultado);
	// El resultado es 55.
	```
	- **Para concatenar dos string** se puede usar el **concat**: 
	
	```js
	// string.concat(string2)
	let string = "Hola ";
	let string2 = "Dalton";
	resultado = string.concat(string2);
	document.write(resultado);
	// El resultado es: Hola Dalton
	```   
	
	-  Con backtiks y la variable entre ${}. 
	
	```
	frase2= `<h2>
   Hola ${nombre}, Bienvenido a la paguina.
   </h2>`; 
	```
	- Escape de comillas simples('string') o de comillas dobles ("string"). 

* Operadores: <small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=4541s)</small>
	- **De Comparacion**:   
		* == Igualdad.  
		* !=	Desigualdad.  
		* === Exactamente iguales, y mismo tipo de datos. 
		* !== Estrictamente diferentes.   
		* < o > Mayor o menor a que.  
		* <= o => Mayor igual o menor igual a que.  
	- **Logicos**:   
		* Valor1 && Valor2. Valor1 And Valor2.  
		* Valor 1 || Valor2. Valor1 OR Valor2.  
		* !Valor.  NOT Valor1.  
		* a > b. A mayor que B.
		* a >= b. A mayoy o igual que B.
		* a < b. A menor que B.
		* a <= b. A menor o igual que B.  
		
* <a name="Camel"></a>**Camel Case**. El estandar para definir nombre en JS, se comienza con minusculas y la segunda palabra en mayusculas.
<small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=5697s)</small>  
Ejemplos:   
 	* nombreCliente.  
	* variableNombre
	* document.getElementById() -->Ejemplo de Camel Case.    

* <a name="Condicionales"></a>**Condicionales:**	<small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=5822s)</small>
	- IF.  
	 if (condicion){  
	...   
	...  
	} else if (condicion){   
	...   
	}   
	else {  
	}
	
	  
	
<a name="Capitulo2"></a>
## Capitulo 2: Arrays.  

 <a name="Arrays"></a> Son objetos que contienen variables que pueden ser de diferentes tipos. <small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=7406s)</small>
  
 ```js
 arrays = ["Alex",40,true];
 ```
 
 
 - <a name="Asociativos"></a>Arrays asociativo: (diccionarios) <small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=8109s) </small>
  
 	```js
	pc = {
	nombre: "AlexPC",
	procesador: "Intel i7:,
	ram: "16GB",
	espacio: "1TB"
	};
	document.write(`<strong>Nombre es: </strong> ${pc['nombre']} <br>`);  
	document.write(`
			    <strong>Procesador es: </strong> ${pc['procesador']} <br>`);  
	document.write(`<strong>La RAM es: </strong> ${pc['ram']} <br>`);
	document.write(`<strong>El espacio es:  </strong>${pc['espacio']} <br>`);

 	```
<a name="Bucles"></a> 	
### While y For:  Bucles. <small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=8608s)</small>

<small>[más info](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements#Iterations)</small> sobre lo bucles.

- **While**: Se ejecuta mientras se cumpla la condición.   

```js
// Sintaxis:
while (condition)
  statement
```
Ejemplo:

```js
let numero = 0;
while (numero <= 6){
	numero++;
	document.write(numero + "<br>")
}

```	
- **Do While**: Parecido al whie, pero ejecuta al menos una vez y luego verifica si se cumple la condición.  

```js
// Sintaxis:
do
   statement
while (condition);
``` 
Ejemplo:
 
```js
let numero = 0;
do{
	numero++;
	document.write(numero + "<br>")
}
while (numero <= 6)
```	
- **Break:** Interrumpe o finaliza el bucle.

```js
let numero = 0;
while (numero < 100){

    document.write(numero + "<br>")
    numero++;
    if ( numero == 10){
        break; //Interrumpe el while
    }
}
// El resultado son los numeros del 1 hasta el número 10.
```
- **For:** Crea un bucle de ejecución determinada. 

```js
// Sintaxis:
for ([initialization]; [condition]; [final-expression])
   statement  
```
Ejemplos:

```js
for (let i = 0; i<10;i++){
    document.write(i + "<br>");
}
document.write("----------" + "<br>");
for (let i = 9; i>=0;i--){
    document.write(i + "<br>");
}
```   
- **continue** Termina la ejecucion de las declaraciones y continua con la siguente interacion.   

```js
for (i=0;i<10;i++){
	if (i == 5){
		continue;
		}
    document.write(i+ " <br>");
// Escribe los números del 0 hasta el 9, saltando el 5.
```

- **for in:** Muestra la posición  

```js
let animales = ["gato","perro","conejo","tiburon"];

//For i, muestra las posiciones 
for (i in animales){
    document.write(i + "<br>");
}
/*Resultado
0
1
2
3 */
```

- **for of:** Muestra el valor de la posición.

```js

document.write("----------------" + "<br>");
//For i, muestra los valores en cada una de las posiciones
for (i of animales){
    document.write(i + "<br>");
}
/*Resultado
gato
perro
conejo
tiburon */
```

- Label: Sirve para cuando hacemos un break o continue nos lleve a la etiqueta que marcamos.

```js
let array1 = ["maria","josefa","roberta"];
let array2 = ["pedro","marcelo",array1,"josefina"];

etiqueta:
for (let array in array2){
    if (array == 2){
        for(let array of array1){
            document.write(array + "<br>");
            break etiqueta;
        }      
    } else {
        document.write(array2[array] + "<br>")
    }
}

```
**Nota** En este caso, el break interrumpe el segundo ciclo for, pero al colocarle la etiqueta tambien termina el primero, saliendo de los dos bucles, dando como resultado:  
pedro  
marcelo   
maria   


<a name="Funciones"></a>
### Funciones: <small>[video](https://www.youtube.com/watch?v=z95mZVUcJ-E&t=11149s)</small>

Tiene tres (3) formas de representarse:  
	- ***Declaración de funciones:*** <small>[más info](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions)</small>  
		function \[name\]([param1[, param2[, ..., paramN]]]) {  
   statements
  
}   
	- **Expresión de funciones**   
		const \[name\] = function ([param1[, param2[, ..., paramN]]]) {
   statements  
}   
	- ***Funciones flechas:***   
		const \[name\] = ([param1[, param2[, ..., paramN]]]) =>{   
		statements    
		}    
#### Paramétros: <small>[más info](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions#Function_parameters)</small> 
  
- Default parameters (Parámetros predeterminados): Permiten que los parámetros formales se inicialicen con valores predeterminados si no se pasa ningún valor o si no se define. Y pueden ser obsionales.   

```js
function multiply(a, b = 1) {
  return a * b;
}

console.log(multiply(5, 2));
// Resultado: 10

console.log(multiply(5));
// Resultado: 5
```
- Rest parameters (Parámetros de descanso): Permite representar un número indefinido de argumentos como una lista.   

```js
const variosParametros = function( ...arg){
    // los parametros los guarda en una lista, puedo acceder a ellos
    document.write(arg[0] + "<br>");
    //Puedo acceder a los metodos de listas.
    // como length,map,sort
    document.write(` Pasaste : ${arg.length} parametros <br>`);
}
variosParametros("maria","josefa","roberta");
```

	
<a name="ForEach"></a>
### ForEach: <small>[video]()</small>



<a name="Capitulo3"></a>
## Capitulo 3:Programacion Orientada a Objetos (POO) 

### Objetos y Clases:

- Atributos
- Metodos
- Constructor
- Instanciacion.
- Caracteristicas:  
	* Abstraccion
	* Modularidad
	* Encapsulamiento
	* Polimorfismo
- Otros conceptos de POO:   
	* Herencia.
	* Metodos Estaticos. Usamos static y es un metodo que se puede utilizar sin instaciar el objeto.
	* Metodos Accesores (Getters, Setters). Los toma como atributos y no como metodos.

<a name="Capitulo4"></a>
## Capitulo 4: Metodo cadenas y arrays

### <a name="MetodosCadenas"></a> Metodos de Cadenas <small>[más info](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Useful_string_methods)</small>

- <a name="length"></a>**length()**: Devuelve la longitud del string.  
	* Sintaxis: lentgth(str).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length)

- <a name="concat"></a>**concat()**: Junta dos o mas cadenas y retorna una nueva cadena.  
	* Sintaxis: str.concat(str2 [, ...strN]).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/concat)  
- <a name="startWith"></a>**startWith()**: Si una cadena comienza con los caracteres de otra cadena, devuelve true/false.  
	* Sintaxis: str.startsWith(searchString[, position])[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/startsWith)
- <a name="endWith"></a>**endsWith()**: Si una cadena termina con los caracteres de otra cadena, devuelve true/false.  
	* Sintaxis: str.endsWith(searchString[, length]).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/endsWith)
- <a name="includes"></a>**includes()**: Si una cadena puede encontrarse dentro de otra, devuelve true/false.  
	* Sintaxis: str.includes(searchString[, position]) [Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes)
- <a name="indexOf"></a>**indexOf()**: Fevuelve el indice del primer caracter de la cadena, si no existe devuelve -1.  
	* Sintaxis: str.indexOf(searchValue [, fromIndex]).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf)
- <a name="lastIndexOf"></a>**lastIndexOf()**: Devuelve el ultimo indice del primer caracter de la cadena, si no existe, devuelve -1.  
	* Sintaxis: str.indexOf(searchValue [, fromIndex]) [mas detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf)
- <a name="repeat"></a>**repeat()**: Devuelve la misma cadena pero repetida la cantidad que le indiquemos por parametro.  
	* Sintaxis: str.repeat(count).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/repeat)
- <a name="split"></a>**split()**: Divide la cadena con el separador.  
	* Sintaxis: str.split([separator[, limit]]).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)
- <a name="substring"></a>**substring()**: Devuelve un pedazo de la cadena.  
	* Sintaxis: str.substring(indexStart[, indexEnd]).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substring)
- <a name="toLowerCase"></a>**toLowerCase()**: Convierte una cadena a minúscula.  
	* Sintaxis: str.toLowerCase().[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase)
- <a name="toUpperCase"></a>**toUpperCase()**: Convierte una cadena a mayuscula.  
	* Sintaxis: str.toUpperCase().[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase)
- <a name="toString"></a>**toString()**: Convierte a string.  
	* Sintaxis: str.toString().[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toString)
- <a name="trim"></a>**trim()**: Elimina los espacios en blanco tanto al principio como al final.Tambien estan [trimEnd](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/trimEnd) y [trimStart.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/trimStart)  
	* Sintaxis: str.trim().[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/Trim)
- <a name="valueOf"></a>**valueOf()**: Devuelve el valor primitivo de un objeto string.  
	* Sintaxis: str.valueOf().[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/valueOf)


### <a name="MetodosArrays"></a> Metodos de Arrays
- <a name="pop"></a>**pop()**: Elimina el ultimo elemento de un array y lo devuelve.  
	* Sintaxis: arrName.pop().[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop)
- <a name="push"></a>**push()**: Agrega uno o mas elementos al final de un array y devuelve la longitud del nuevo array.
	* Sintaxis: arr.push([element1[, ...[, elementN]]]).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)
- <a name="shift"></a>** shift()**: Elimina el primer elemento de un array y lo devuelve.  
	* Sintaxis: arr.shift().[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift)
- <a name="reverse"></a>**reverse()**: Invierte el orden de los elementos de un array.  
	* Sintaxis: arr.reverse().[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse)
- <a name="unshift"></a>**unshift()**: Agrega uno o mas elementos al inicio del array, y devuelve la longitud del nuevo array.  
	* Sintaxis: arr.unshift(element1[, ...[, elementN]]).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift)
- <a name="sort"></a>**sort()**: Ordena los elementos de un array localmente y lo devuelve ordenado.  
	* Sintaxis: arr.sort([compareFunction]).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
- <a name="splice"></a>**splice()**: Cambia el contenido de un array eliminando elementos existentes y/o agregando nuevos elementos.  
	* Sintaxis: let arrDeletedItems = array.splice(start[, deleteCount[, item1[, item2[, ...]]]]).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)
- <a name="join"></a>**join()**: Crea un string con los elementos del array separados por el seperator.  
	* Sintaxis: arr.join([separator]).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)
- <a name="slice"></a>**slice()**: Devuelve un trozo del array original.  
	* Sintaxis: arr.slice([start[, end]]).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)
- <a name="filter"></a>**filter()**:Crea un nuevo array con los criterios deseados.  
	* Sintaxis: let newArray = arr.filter(callback(currentValue[, index[, array]]) {
  // return element for newArray, if true
}[, thisArg]);.[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
	* Ejemplo:

	```js
	const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];
	
	const result = words.filter(word => word.length > 6);
	console.log(result);
	// expected output: Array ["exuberant", "destruction", "present"]
	```
- <a name="forEach"></a>**forEach()**:Ejecuta por cada uno de los elementos del array la accion o funcion pasada por parametro.  
	* Sintaxis: arr.forEach(callback(currentValue[, index[, array]]) {
  // execute something
}[, thisArg]);.[Detalle](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/forEach)
	* Ejemplo:
	
	```js
	const array1 = ['a', 'b', 'c'];
	array1.forEach(element => console.log(element));
	```


### <a name="ObjetoMath"></a> Objeto Math

Math es un objeto integrado de JS que tiene propiedades y metodos para funciones y constantes matematicas. [Para mas informacion.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)

1. <a name="MetodosMath".</a> Metodos Math:
	- <a name="sqrt(x)"></a>**sqrt()**: La raiz cuadrada de un numero.  
	* Sintaxis: Math.sqrt.[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/sqrt)
	
	- <a name="cbrt"></a>**cbrt()**: Devuelve la raiz cubica de un numero.  
	* Sintaxis: Math.cbrt(x).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/cbrt)

	- <a name="max"></a>**max()**: Devuelve el mayor de varios numero.  
	* Sintaxis: Math.max(x,y,...,n).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/max)
	* Ejemplo:
	
	```js
	console.log(Math.max(1, 3, 2));
	// expected output: 3
	
	console.log(Math.max(-1, -3, -2));
	// expected output: -1
	
	const array1 = [1, 3, 2];
	
	console.log(Math.max(...array1));
	// expected output: 3
	```

	- <a name="min"></a>**min()**: Devuelve el numero mas pequeño.  
	* Sintaxis: Math.min(x,y,...,n).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/min)
	* Ejemplo:

	- <a name="random"></a>**random()**: Devuelve un numero pseudo-aleatorio entre 0 y 1.  
	* Sintaxis: Math.random.[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)

	- <a name="round"></a>**round()**: Devuelve el valorde un numero redondeado al numero entero mas cercano.  
	* Sintaxis: Math.round(x).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/round)
	* Ejemplo:

	- <a name="fround"></a>**fround()**: Devuelve el numero mas cercado con una precision de 32bits.  
	* Sintaxis: var singleFloat = Math.fround(doubleFloat);.[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/fround)
	* Ejemplo:
	
	```js
	console.log(Math.fround(5.05));
	// expected output: 5.050000190734863

	console.log(Math.fround(5));
	// expected output: 5
	```

	- <a name="floor"></a>**floor()**: Devuelve el mayor entero menor o igual al numero dado.  
	* Sintaxis: Math.floor(x).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/floor)
	* Ejemplo:
	
	```js
	console.log(Math.floor(5.95));
	// expected output: 5

	console.log(Math.floor(5.05));
	// expected output: 5

	console.log(Math.floor(5));
	// expected output: 5

	console.log(Math.floor(-5.05));
	// expected output: -6
	```

	- <a name="trunc"></a>**trunc()**: Devuelve la parte entera de un numero dado.  
	* Sintaxis: Math.trunc(x).[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/trunc)
	* Ejemplo:
	
	```js
	console.log(Math.trunc(42.84));
	// expected output: 42

	console.log(Math.trunc(0.123));
	// expected output: 0

	```
	
2. <a name="PropiedadesMath".</a> Pr5piedades Math:
	- <a name="PI"></a>**PI()**: Constante del valor PI.  
	* Sintaxis: Math.PI.[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/PI)
	

<a name="Capitulo5"></a>   
##Capitulo 5:


La consola se puede utilizar para variadas funciones como depurar errores, ubicar, asignar o modificar variables, asi como interactuar con la paguina.[Mas informacion](https://developer.mozilla.org/en-US/docs/Tools/Web_Console/The_command_line_interpreter)

1. <a name="Consola"></a> Consola de JavaScript (console).
2. <a name="MRegistro"></a>Metodos de registro en la consola.
	-	assert()
	- 	clear()
	-  error()
	-  info()
	-  log()
	-  table()
	
3. <a name="MConteo"></a>Metodos de conteo en la consola.
	- count(). Para contar las veces que se ejecuta algo.
	- countReset(). Reinicia el contador.
4. <a name="MAgrupacion"></a>Metodos de agrupacion en la consola.
	- group("nombre_grupo"). Crea un nuevo grupo en la linea de registro
	- groupEnd(). Remueve un grupu en linea de registro
	- groupCollapsed('nombre_grupo'). Igual que el group pero los muestra cerrado.
5. <a name="MTemporizacion"></a>Metodos de temporizacion en la consola.

	Se puede utilizar para saber cuanto tiempo tarda en ejecutarse algo, cuando tiempo tarda un usuario en hacer algo.

	- time()
	- timeLog()
	- timeEnd()

**Adicional:**  console.log("%cHola","color:red;background:black;padding:20px");


## <a name="Capitulo1"></a> Capitulo 6:

1. <a name="DOM"></a>El DOM (Document Object Model).
2. <a name="MSeleccionElementos"></a>Metodos de seleccion de elementos.
	* getElementById(). Selecciona un elemento por ID.
	
	```html
	<div class="idDiv1">
    	<p id="ID_Parrafo"></p>
	</div>
	```  
	
	```js
	parrafo = document.getElementById("ID_Parrafo");
	document.write(parrafo + "<br>");
	```
	
	* getElementByTagName(). Selecciona todos los elementos que coincidan con el nombre de la etiqueta especificada.

	```js
	parrafo1 = document.getElementsByTagName("p");
	document.write(parrafo1 + "<br>");
	```
	* querySelector(). Devuelve el primer elemento que coincida con el grupo especificado de selectores.

	```js
		// Selecionado por la clase
	parrafo2 = document.querySelector(".parrafo");
	document.write(parrafo2 + "<br>");
		// Selecionado por el ID
	parrafo3 = document.querySelector("#ID_Parrafo");
	document.write(parrafo3 + "<br>");
	```
	* querySelectorAll(). Devuelve todos los elementos que coincidan con el grupo especificado de selectores.

	
	```js
	parrafo4 = document.querySelectorAll(".parrafo");
	document.write(parrafo4 + "<br>");
	```
	
3. <a name="MAtributos"></a>Metodos de atributos de un elemento.
	* setAttribute(). Modifica el valor de un atriguto.
	* getAttribute(). Obtiene el valor de un atributo.
	* romeveAttribute(). Remueve el valor de un atributo.
	*
	
	```html
	<input type="range" class="rangoEtario">
    <label>Etiqueta del Input</label>
    ```
    
    ```js
    const rangoEtario = document.querySelector (".rangoEtario");

	//document.write(rangoEtario);
		
	//rangoEtario.setAttribute("type","text");
		
	valorDelAtributo = rangoEtario.getAttribute("type");
document.write(valorDelAtributo);
	```
4. <a name="AtributosGlobales"></a>Atributos globales. Para mas informacion [ver](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes) 	* class. Lista de clases del elemento separadas por espacios.
	* contenteditable. Indica si el elemento puede ser modificado por el usuario, booleano.
	
	```html
	<h1 class="titulo"> Titulo </h1>
	```
	
	```js
	// Selecciono por classe titulo
	const titulo = document.querySelector(".titulo");
	// Modifico el atributo
 	titulo.setAttribute("contentEditable","true");
 	```
	* dir. Indica la direccionalidad del texto.
	* hidden. Indica si el elemento es o no relevante. No lleva valor, al existir ya no se muestra el elemento.
	* id. Define un identificador unico.
	* style. Contiene declaracones de estilo CSS para el elemento.
	* tabindex. Indica si el elemento puede obtener un focus de input.
	* title. Contiene un texto con informacion del elemento.



5. <a name="AStyle"></a>Atributos de inputs. Para mas informacion [ver](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)
	* className. Devuelve el nombre de la clase
	
	```html
	<div><input type="text" class="input-normal" value="XYZ"><br></div>
	```
	
	```js
	const inputIntancia = document.querySelector(".input-normal");
	document.write(inputIntancia.className);
	// Imprime el nombr de la clase.
	```
	* value.
	
	```js
	const inputIntancia = document.querySelector(".input-normal");
	document.write(inputIntancia.value);
	// Imprime el nombr de la clase.
	```

	* type.
	
	```js
	inputIntancia.type="range";
		// Cambia el typo de elemento a range.
	inputIntancia.type="number";
		// Cambia el typo de elemeento a number.
	```
	
	* accept. Se utiliza para abrir archivo, las extenciones que acelta.
	
	
	```js
	inputIntancia.accept =  "image/png"
	```
	
	* form. Nos permite ejecutar un imput dentro de un form.

	  En este ejemplo, el Input-Fuera no afecta al form, pues esta fuera.
	
	```html
	<div>
        <form action="" id="formulario">
            <input type="text" id="Input-Dentro">
        </form>
        <input type="text" id="Input-Fuera" form="formulario">
    </div>
    ```
    En este ejemplo, incluimos el atributo form:   
	
	```js
	const inputIntancia2 = document.querySelector("#Input-Fuera");
	inputIntancia2.setAttribute("form","formulario");
		// Nota: no funciona de la siguiente forma:
	inputIntancia.form="formulario";
	```
	
	Entonces, el Input-Fuera va a ejecutar igual que el input-Dentro
	
	```html
	<div>
        <form action="" id="formulario">
            <input type="text" id="Input-Dentro">
        </form>
        <input type="text" id="Input-Fuera" form="formulario">
    </div>
    ```
	
	* minlength. Validador del input en un formulario.
	
	```html
	<form >
            <input type="text" id="Min-Len"><br>
            <input type="submit" value="Enter">
    </form>
	```
	
	```js
	const inputInance3 = document.querySelector("#Min-Len");
 	inputInance3.minLength = "5";
 	```
 	
	* placeholder.

	```js
	const inputInance3 = document.querySelector("#Min-Len");
 	inputInance3.placeholder = "Tu nombre:";
 	```
	* required. Validacion del input un form, para indicar que es requerido.

	```js
	const inputInance3 = document.querySelector("#Min-Len");
 	inputInance3.placeholder = "Tu nombre:";
 	inputInance3.required = false;
 	```
 	
 	Nota: Cuando se utiliza esta atributo po JS, funciona en la validacion, pero si vamos a ver el elemento en la paguina web no se muestra. Podria ser por seguridad?
 	
 	
6. <a name="PropiedadStyle"></a>Propriedad Style.

	* Nos permite modificar caracteristicas CSS del elemento.
	
	```js
	const titulo = documen.querySelector(".titulo");
	titulo.style.color = "red";
	```
7. <a name="ClassList"></a>Clases, [classList](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList) y sus [metodos](https://developer.mozilla.org/en-US/docs/Web/API/DOMTokenList).
	
	* classList.add().Añade una clase	
	```htnl
	<span class="a b c"></span>
	```
	
	```js
	let span = document.querySelector("span");
	let classes = span.classList;
	classes.add("d");
	span.textContent = classes;
	```
	
	* classList.remove()
	
	```
	<div id="a" class="a b c"></div>
	```
	
	```js
	let span2 = document.getElementById("a")
	let classes2 = span2.classList;
	
	classes2.remove("c", "b");
	span2.textContent = classes2;
	```
	
	El resultado es: a
	
	
	* classList.item().Devuelve la clase del indice indicado.
	
	```
	<span class="a b c"></span>
	```
	
	```js
	let span = document.querySelector("span");
	let classes = span.classList;
	let item = classes.item(classes.length-1);
	span.textContent = item;
	```
	El resultado es: C
	
	* classList.contains().
	
	```
	<span class="a b c"></span>
	```
	
	```js
	let span = document.querySelector("span");
	let classes = span.classList;
	let result = classes.contains("c");
	if (result) {
	  span.textContent = "The classList contains 'c'";
	} else {
	   span.textContent = "The classList does not contain 'c'";
	}
	```
	El resultado es: `The classList contains 'c'`
	
	* classList.replace()
	
	```
	<span class="a b c"></span>
	```
	
	```js
	let span = document.querySelector("span");
	let classes = span.classList;
	
	let result = classes.replace("c", "z");
	console.log(result);
	
	if (result) {
	  span.textContent = classes;
	} else {
	  span.textContent = 'token not replaced successfully';
}
	```
	El resultado es: `a b z`
	
	* classList.toggle(). Si no tiene la clase especificada, la agrega, si ya la tiene, la elimina.
	
	```
	<span class="a b">classList is 'a b'</span>
	```
	
	```
	let span = document.querySelector("span");
	let classes = span.classList;
	
	span.addEventListener('click', function() {
	  let result = classes.toggle("c");
	
	  if (result) {
	    span.textContent = `'c' added; classList is now "${classes}".`;
	  } else {
	    span.textContent = `'c' removed; classList is now "${classes}".`;
	  }
	})
	```
	El resultado es: ` classList is 'a b'`
	
	* node.textContent.[ver más](https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent). Devuelve o asigna el valor de texto interno del nodo.
	
	```html
	<div id="divA">This is <span>some</span> text!</div>
	```
	
	```js
	let text = document.getElementById('divA').textContent;
	// The text variable is now: 'This is some text!'
	```
	
	* Element.innerHTML.[ver más](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML). Devuelve o asigna, el valor interno del nodo, incluyendo el HTML interno.

	```html
	<div id="divA">This is <span>some</span> text!</div>
	```
	
	```js
	let  tHtml = document.getElementById("divA").innerHTML;
 	alert(tHtml);
	```
	El resultado es: `This is <span>some</span> text!`

	* Element.outerHTML.[ver más](https://developer.mozilla.org/en-US/docs/Web/API/Element/outerHTML).Devuelve o asigna, el valor interno del nodo, incluyendo el HTML que lo contine.

	```html
	<div id="divA">This is <span>some</span> text!
    <p id="pEjemplo">Ejemplo:</p>
	</div>
	```
	
	```js
		// Guarda en toHtml el HTML de todo el elemento.
	let toHtml = document.getElementById("divA").outerHTML;
		// Escribe el resultado en el parrafo id="pEjemplo
 	document.getElementById("pEjemplo").textContent = toHtml;
	```
	El resultado es:
	
	```
	<div id="divA">This is <span>some</span> text! <p id="pEjemplo">Ejemplo:</p> </div>
	```
	
8. <a name="CreacionElementos"></a>Creacion de Elementos.
	* createElement().Crea elemento en el DOM.[ver más](https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement)
	* createTextNode().
	* createDocumentFragment(). Esto es nuevo y se utiliza para optimizar recursos, cuando se inserta un nuevo elemento al DOM, el navegador borra el contenido y lo dibuja nuevamente con el nuevo elemento, entonces, se utiliza el **createDocumentFragment** para hacer una sola adicion al DOM.

	```html
	<div class="contenedor"></div>
	```
	
	```js
	// createDocumentFragment
		// Seleccionamos el elemento.
	const contenedor = document.querySelector(".contenedor");
		//Creamos el fragmento a utilizar.
	const fragmento = document.createDocumentFragment ();
	for (i=0;i<5; i++){
			// Creamos el elemento li:lista
	    const item = document.createElement("li");
	    	// Le asignamos valor a ese elemento.
	    item.textContent = "Este es un item de la lista";
	    	// Sumamos ese elemento con ese valor al fragmento.
	    fragmento.appendChild(item);
}
		// Sumamos o agregamos el fragmento completo al DOM, y aqui lo redibuja.
 	contenedor.appendChild(fragmento);
 	```
	
9. <a name="ModificarChilds"></a>Obtencion y modificadores de childs.[más información](https://developer.mozilla.org/en-US/docs/Web/API/ParentNode)
	* firstChild.
	* lastChild.
	* firstElementChild.
	* lastElementChild.
	
	```html
	<div class="contenedor">
    <h2>Un h2 comun</h2>
    <h4>Un h4 comun</h4>
    <p>Un parrafo</p>
	</div>
	```
	
	```js
	// Obtencion y modificadores de childs.
	const contenedor=document.querySelector(".contenedor");
	const primerHijo=contenedor.firstChild;
	console.log(primerHijo);
	 /* Aqui nos muestra, por consola, que el primer hijo es un texto, pues hay espacio antes de la
	 etiqueta del h2. Esto se resuelve utilizando   firstElementChild. */
	 const primerElementoHijo = contenedor.firstElementChild;
	 console.log(primerElementoHijo);
	```

	
	* childNotes. Nos devuelve todos los nodos hijos (incluyendo los espacios entre elementos) y es un objeto que se puede recorrer con forEach.
	
	```js
	const contenedor=document.querySelector(".contenedor");
	const hijo=contenedor.childNodes;
	console.log(hijo);
		// Para mostrar todos los hijos:
	hijo.forEach(hijo => console.log(hijo));
	```
	* children. Nos devuelve los elementos hijos del nodo.
	
	```js
	// Children.	
	const contenedor=document.querySelector(".contenedor");
	const hijo=contenedor.children;
	console.log(hijo);
	```
	
	```js
	// Para recorrerlo
	console.log(hijo);
	for (hijos of  hijo){
	    console.log(hijos);
	}
	```
	
9. <a name="MChilds"></a>Metodos de childs (hijos).
	* replaceChild().
	* removeChild().
	* hasChlidNodes().

	```html
	<div class="contenedor">
    <h2 class="h2">Un h2 comun</h2>
    <h4>Un h4 comun</h4>
    <div class="divParrafo">
         <p id="parrafo">Un parrafo</p>
    </div >
    <input type="submit" value="Renplace h2" id="replace" onClick="remplazar()"><br>
    <input type="submit" value="Remover  parrado" id="remover" onClick="remover()"><br>
    <input type="submit" value="Tiene Hijos?" id="remover" onClick="tieneHijos()"><br>
    <input type="submit" value="Remover Todos los hijos" id="removerTodosHijos" onClick="removerTextHtml()"><br>
	</div>
	```
	
	```js
	//  replaceChild + removeChild + hasChildNodes
	// Utilizando onClick eventos, para hacer practicas variadas.
	const contenedor=document.querySelector(".contenedor");
	const contenedorDivParrafo = document.querySelector(".divParrafo");
	const h2_nuevo = document.createElement("h2");
	h2_nuevo.textContent =  "Titulo";
	h2_angtiguo =  document.querySelector(".h2");
	//contenedor.replaceChild(h2_nuevo,h2_angtiguo);
	p_antiguo = document.querySelector("#parrafo");
	const remplazar = ()  => contenedor.replaceChild(h2_nuevo,h2_angtiguo);
	const removerTextHtml = () =>{
	    let cont = document.querySelector(".divParrafo");
	    let primerHijo2 = cont.firstChild;
	    while (cont.firstChild){
	        cont.removeChild(cont.firstChild);
	    }
	}
	const remover = () => {
	    contenedorDivParrafo.removeChild(p_antiguo);
	    removerTextHtml();
	    //let botton = document.getElementById("parrafo");
	    //botton.setAttribute("hidden","true");
	}
	const tieneHijos = () =>{
	    let contenedorDivParrafoNuevo = document.querySelector(".divParrafo");
	    let respuestaTieneHijos = contenedorDivParrafoNuevo.hasChildNodes();
	    if (respuestaTieneHijos) {
	        alert("Si tiene Hijos");
	        } else {
	            alert("No tiene Hijos");
	        }
	    }
	```
10. <a name="PropiedadesPadres"></a>Propiedades de parents (Padres).
	* parentElement.
	* parentNode. Se usa muy poco, pues en la mayoria de los casos los padres son elementos.

	```js
	const contenedor=document.querySelector("#parrafo");
	console.log(contenedor.parentElement);
	```
	Me va a devolver divParrafo, que es el padre de parrafo
	
	```js
	const contenedor=document.querySelector(".divParrafo");
	console.log(contenedor.parentElement);
	```
	Me va devolver el div contenedor.

	
11. <a name="PropiedadesHermanos"></a>Propiedades de siblingds (Hermanos).
	* nextSibling.
	* previousSibling.
	* nextElementSibling.
	* previousElementSibling. 

	```js
	const contenedor=document.querySelector(".divParrafo");
	    // Me devuelve el hermano siguiente, incluyendo los Text.
	    // En este caso un Text
	console.log(contenedor.nextSibling)
	    // Me devuelve el hermano anterior, solo los elementos.
	    // En este caso el h4
	console.log(contenedor.previousElementSibling);
	    // Me devuelve el hermano siguiente, solo elementos.
	    // En este caso el input "Remplace h2"
	console.log(contenedor.nextElementSibling);
	```
	## Practica:
	**Practica** para eliminar los nodos Text de un Elemento. Utilizo el metodo node.nodeType [ver más](https://developer.mozilla.org/es/docs/Web/API/Node/nodeType) y el forEach para recorrer la lista de objetos [ver más](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
	
	```js
	// Practica - Eliminar todos los Nodos tipo Text
	const removerTextHtml2 = (identificadorClase) =>{
	    const contenedor=document.querySelector(identificadorClase);
	    const hijo=contenedor.childNodes;
	    console.log(`Al comienso tiene: ${hijo.length} hijos`);
	    hijo.forEach(hijo => {
	        //console.log(hijo);
	        //console.log(hijo.nodeType);
	        if (hijo.nodeType != 3){
	            hijo.nextSibling
	        } else{
	            contenedor.removeChild(hijo);
	        }
	    });
	    console.log(`Al final tiene: ${hijo.length} hijo(s)`);
	}
removerTextHtml2(".divParrafo");
```
12. <a name="PropiedadExtra"></a>Nodos, una propiedad extra.






		
		

