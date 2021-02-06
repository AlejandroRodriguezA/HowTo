# Angular

Es un framework que permite construir paguinas webs de una sola pagina (simplePaguine), la documentacion oficial se encuentra en <https://angular.io/start>.

## CLI Deep Dive

Command Line Interface (CLI) permite crear, manejar, conostruir y probar proyecto en angular. Para mas informacion <https://github.com/angular/angular-cli>

Updating npm:   

```
sudo npm install -g npm
```   

Updating the CLI    
 
```
$ [sudo] npm uninstall -g angular-cli @angular/cli 

$ npm cache verify 

$ [sudo] npm install -g @angular/cli 
```   

Verificando correcta instalacion:    

```
$ ng help
$ ng generate --help
```   

Crear un nuevo proyecto   

```
$ ng new my-first-project
? Do you want to enforce stricter type checking and stricter bundle budgets in the workspace?
  This setting helps improve maintainability and catch bugs ahead of time.
  For more information, see https://angular.io/strict (y/N)
? Would you like to add Angular routing? (y/N)
❯ CSS
  SCSS   [ https://sass-lang.com/documentation/syntax#scss                ]
  Sass   [ https://sass-lang.com/documentation/syntax#the-indented-syntax ]
  Less   [ http://lesscss.org                                             ]
  Stylus [ https://stylus-lang.com                                        ]
  
$ cd my-first-project
$ ng serve
```   

Para installar Bootstrap 3 en la carpeta del proyecto:   

```
$ npm install --save bootstrap@3
```   

En el archivo angular.json incluir la instalacion:   

```
"styles": [
              "src/styles.css"
            ],
```   

```
"styles": [
              "node_modules/bootstrap/dist/css/bootstrap.min.css",
              "src/styles.css"
            ],
```   

## The Basics.  

### Como una aplicacion Angular se carga y comienza.   



### Los componentes son importantes.    

### Creando nuevos componentes.  

### Databinding.   

Databinding = Comunicacion (entre TypeScrip Code y Templates)

1. Output Data:  
	* String Interpolation ( {{ data }} ).   
	* Property binding ( [property] ='data ).   
2. React to (user) Events:   
	* Event Binding ( (event)='expression" )   
3. Combinacion de los dos anteriores:
	* Two-Way-Binding ( [(NgModel)]="data" ).   


#### String Interpolation: [documentacion](https://angular.io/guide/interpolation)      

String Interpolation or text interpolation permite la incorparacion de data a los HTML templates.

La forma de usarla es usando los doble llaves {{ }} y el objetivo puede ser un elemento HTML, un componente o una directiva.   

y pueden ser:   

* Propiedades o Metodos del componente al que pertenecen.
* Evaluar y convierte a string el resultado. Por ejemplo {{ 1+ 1 }} mostrara 2.   
* Variable referencia en el template.
* Variables input en el template.


[Mejores practicas](https://angular.io/guide/interpolation#expression-best-practices)    


#### Property Binding.    


 




	  



