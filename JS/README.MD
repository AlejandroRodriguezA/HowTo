# JS a Junior de [Soy Dalton](https://youtu.be/z95mZVUcJ-E)

# Indice:
- [Capitulo 1:](#Capitulo1)
- [Capitulo 2:](#Capitulo2) 

	* [Metodo de Cadenas](#MetodosCadenas)  
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

	* [Metodo de Arrays](#MetodosArrays) 

		1. Transformadores: 
			- [pop().](#pop)
			- [push().](#push)
			- [shift().](#shift)
			- [reverse().](#reverse)
			- [unshift().](#unshift)
			- [sort().](#sort)
			- [splice().](#splice)  
			 
		2. Accesores:
			- [join().](#join)
			- [slice().](#slice)
			
		3. De Repeticion:
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
			
## <a name="Capitulo1"></a> Capitulo 1:
* Introduccion.
	- JS es un leguaje de programacion Interpretado que se difiere a un leguaje compilado, es decir, se ejecuta en el navegador en el inteprete.  
	- Es Orientado a objetos.  
	- Es Imperativo. Se va ejecutando linea a linea.
	- Es Case sensite.
	- Basado en prototipos / instancias / clases.
	- Tipado debil. Significa que el valor de los datos y variables puede ir variando durante el tiempo.Se define como string al comienzo y luego se redefine como interger.
	- Lenguaje dinnamico. El dato se ajusta a la variable.
	- Esta construido sobre ECMASCRIPT (5, 6, 7, 8, Next).
* Esta usando Sublime Text 3, su configuracion (plugins) son:   
	- shift+command+P --> install control Package
	- BlackBird-ColorScheme
	- Brogrammer
	- Set UI
	- liveReload
	- ColorHelper
	- ColorPicker
	
* Para que se usa:  
	- Dinamismo de los sitios web
	- Servidor en NodeJS
	- Tecnologias Frontend como Angular, React o Vue.JS
	- Mobile Apps
	- Desktop Apps
	- Inteligencia Artificial. No es muy usual, pero se puede usar.
	
* Como enlazar JS:   
	- En linea:   
	```<h1 onclick="alert('hola')"> Saludo </h1>	 ```
	- Dentro de la etiqueta:   
	``` <script></script>:  
			<script type="text/javascript">
		        alert('Hola desde script');
		    </script> ```
	- Enlazado desde un archivo externo:  
			<script src="codigo.js" type="text/javascript"></script>
	- Con un Require. Buscar inforamcion pues el no lo explica.
* Variables:
	- Hay tres formas de declarar la variables (var, let, const)
		* var: alcance global.
		* let: alcance local.
		* const: es una constante.
		Nota: Si no se coloca nada, la variable es definida de forma global.  
	- Hoisting. 
*  Nota: Los errores se muestran en consola, no en la paguina. option+command+j para mostrar la consola de JS.
*  **prompt**("mensaje") -> Esta funcion permite ingresar informacion por el usuario.
*  document.write(vatiable); --> Escribe la variable en la pag.web.
*  Operadores:   	
	- De asignacion. [mas info](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Operadores/Assignment_Operators)  
		* x = y
		* x += y
		* x -= y
		* x *= y
		* x /= y
		* x %= y
		
	- Aritmeticos.
* Concatenacion:  
	- **Para forzar** a que se concatene : frase = "" + numero + numero1 /* fuerza  a que sea string*/
	- **Para concatenar dos string** se puede usar el **concat**: 
	```string.concat(string2)```   
	-  Con backtiks y la variable entre ${}. 
			```
			frase2= `<h2>
        Hola ${nombre}, Bienvenido a la paguina.
        </h2>`; 
			```
	- **De Comparacion**:   
		== Igualdad.  
		!=	Desigualdad.  
		=== Exactamente iguales.  
		<,> Mayor o menor a que.  
		<=, => Mayor igual o menor igual a que.  
	- **Logicos**:   
		Valor1 && Valor2. Valor1 And Valor2.  
		Valor 1 || Valor2. Valor1 OR Valor2.  
		!Valor.  NOT Valor1.    
		
* **Camel Case**. El estandar para definir nombre en JS, se comienza con minusculas y la segunda palabra en mayusculas.Ejemplo:   
nombreCliente
variableNombre
document.getElementById() -->Ejemplo de Camel Case.    

* **Condicionales:**   
	- IF.  
	 if (condicion){  
	...   
	...  
	} else if (condicion){   
	...   
	}   
	else {  
	}
	
	- While.
	- For.  
	
## <a name="Capitulo2"></a>Capitulo 2: Arrays
 Son objetos que contienen variables que pueden ser de diferentes tipos. 
  
 ```js
 arrays = ["Alex",40,];
 ```
 
 
 - Arrays asociativo: (diccionarios)  
 - 
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
 	
### While y For:  Bucles.

- While:

```js
let numero = 0;
while (numero <= 6){
	numero++;
	document.write(numero + "<br>")
}
```	
- Do While:   
 
```js
let numero = 0;
do{
	numero++;
	document.write(numero + "<br>")
}
while (numero <= 6)
```	
- Break: Interrumpe o finaliza el bucle.

```js
let numero = 0;
while (numero < 100){

    document.write(numero + "<br>")
    numero++;
    if ( numero == 10){
        break; //Interrumpe el while
    }
}
```
- For:

```js
for (let i = 0; i<10;i++){
    document.write(i + "<br>");
}
document.write("----------" + "<br>");
for (let i = 9; i>=0;i--){
    document.write(i + "<br>");
}
```

```js
let animales = ["gato","perro","conejo","tiburon"];

//For i, muestra las posiciones 
for (i in animales){
    document.write(i + "<br>");
}

document.write("----------------" + "<br>");
//For i, muestra los valores en cada una de las posiciones
for (i of animales){
    document.write(i + "<br>");
}
```

- Label: Sirve para cuando hacemos un break o continue nos lleve a la etiqueta que marcamos.

### Funciones:

Tiene tres (3) formas de representarse:  
	- function nombreFuncion (variable,variable2){  
		Sentencias  
		return  
	}  
	- const nombreFuncion = function (variable){
		sentencias  
		return  
		}  
	- const nombreFuncion = (variables) =>{   
		sentencias   
		return  
		}   

## Programacion Orientada a Objetos (POO) 
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


## <a name="MetodosCadenas"></a> Metodos de Cadenas
#####[Para más informacion ver](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Useful_string_methods)

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


## <a name="MetodosArrays"></a> Metodos de Arrays
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


## <a name="ObjetoMath"></a> Objeto Math

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
	
2. <a name="PropiedadesMath".</a> Propiedades Math:
	- <a name="PI"></a>**PI()**: Constante del valor PI.  
	* Sintaxis: Math.PI.[Detalle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/PI)
	




		
		

