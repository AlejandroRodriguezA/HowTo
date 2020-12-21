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
- <a name="XXX"></a>**XXXX()**: XXXX.  
	* Sintaxis: XXXX.[Detalle](XXXX)



		
		

