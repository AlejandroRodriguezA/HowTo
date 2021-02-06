TypeScrip [handbook](https://www.typescriptlang.org/docs/handbook/intro.html)

[ Angular:](https://angular.io/)

[Angular Glosario:](https://angular.io/guide/glossary)
[Stack Blitz](https://stackblitz.com/).  Es un repositorio donde  puedes guardar tus proyectos para compartir. La diferenciacon github es que se pueden ejecutar en la web y no hace falta descargarlo o clonarlo a la computadora o en local.

[Angular Tutorial}(https://angular.io/tutorial): Tutorial de la paguina oficial:   

* [CLI](https://angular.io/cli). Es una herramienta que se usa para inicializar, mantener, entre otras cosas, las apliaciones de Angular desde la consola/terminal.   
* Creo una carpeta en el directorio, projects,  raiz de mi computadora ya que son los estanderes actuales para la ubicacion de los proyectos.  En mi caso queda en:

       /Users/alejandroRodriguez/projects/angular/tutorial

* Para instalar [CLI](https://angular.io/cli) se usa npm package manager:  

    ```bash
    npm install -g @angular/cli
    ```

    nota: -g es para global
* Si ya tienes instalado el npm, salta este paso, sino:

	```bash
	brew install npm
	```
	Nota: Existen varias formas, esta fue la que escogi.

	Verificamos la instalacion:

	```bash
	$ npm --version
	7.3.0
	```   

* Para crear el proyecto Angular basico, en el terminal, ir al directorio donde van a guardar el proyecto (En mi caso ../projects/angular/tutorial).
	```bash
		$ ng new <proyecto_nombre>
	```

	```bash
	$ ng new my-first-project
	? Do you want to enforce stricter type checking and stricter bundle budgets in the workspace?
	  This setting helps improve maintainability and catch bugs ahead of time.
	  For more information, see https://angular.io/strict Yes
	? Would you like to add Angular routing? Yes
	? Which stylesheet format would you like to use?
	❯ CSS
	  SCSS   [ https://sass-lang.com/documentation/syntax#scss                ]
	  Sass   [ https://sass-lang.com/documentation/syntax#the-indented-syntax ]
	  Less   [ http://lesscss.org                                             ]
	  Stylus [ https://stylus-lang.com

	  ✔ Packages installed successfully.
    Successfully initialized git.
	```

* **Para ejecutar el servidor**:
	```bash
	cd my-app
	ng serve --open
	```

	Nota: Por defecto lo ejecuta en http://127.0.0.1:4200/   

     
## **Para generar un nuevo componente** 
### De forma manual.   

#### 1. Creamos los archivos necesarios.Cada "componente" contiene 4 archivos:   
	1. \<nombre-componente\>.component.ts.  
	2. \<nombre-componente\>.component.html.  
	3. \<nombre-componente\>.component.CSS.  
	4. \<nombre-componente\>.component.spec.ts.  
<br>

Los dos primeros son indispensables y son los que vamos a utilizar de momento. **Nota:** Cuando creamos el module con CLI crea los cuatro archivos.   

Para organizarnos, es mejor contener todos los archivos de un component dentro de una carpeta, que estara ubicada dentro de /app:   

```bash
 nombre_proyecto. git:(master) ✗ cd src
➜  src git:(master) ✗ mkdir nombre-componente
➜  src git:(master) ✗ cd nombre-componente
➜  nombre-componente git:(master) ✗ touch nombre-componente.component.ts
➜  nombre-componente git:(master) ✗ touch nombre-componente.component.html
➜  nombre-componente git:(master) ✗ touch nombre-componente.component.css
➜  nombre-mcomponente git:(master) ✗ touch nombre-componente.component.spec.ts
➜  nombre-componente git:(master) ✗ ls
nombre-componente.component.css     nombre-componente.component.spec.ts
nombre-componente.component.html    nombre-module.component.ts
```   

**NOTA:* por standar el nombre del componente, de tener varias palabras, van separadas por "-" y en minusculas.   

#### 2. En el \<nombre-componente\>.component.ts:   

```TS
import { Component } from '@angular/core';

@Component({
  selector: 'app-<nombre-modulo>',
  templateUrl: '.\<nombre-componente\>.component.html'
})
export class <NombreComponente>Component {
  
}
```   

**Notas:**   
1. El nombre del selector es : app+\<nombre-componente\>.  
2. En el templateUrl: la direccion del archivo \<nombre-componente\>.component.html   
3. En el nombre de la clase se utiliza Pastal estandar, que es NombreModulo.   <br>

#### 3. En el archivo app.module.ts, agregamos la clase del nuevo component creado:   

```ts
// Importamos la clase del componente creado
import { NombreComponenteComponent } from './nombre-componente/nombre-conponente.component';

// agregamos la clase a la declaracion:
@NgModule({
  declarations: [
    AppComponent, // No olvidar colocar la ","
    NombreComponenteComponent // <-- Aqui se agrega
  ],
  imports: [
    BrowserModule,
    AppRoutingModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
```   

***Nota: El archivo (app.module.ts) que asi:***   

```ts
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';

import { AppRoutingModule } from './app-routing.module';
import { AppComponent } from './app.component';
// Importamos la clase del componente creado
import { PostCreateComponent } from './post/post-create/post-create.component';

@NgModule({
  declarations: [
    AppComponent,
    PostCreateComponent // <-- Aqui se agrega
  ],
  imports: [
    BrowserModule,
    AppRoutingModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```  

#### 4. En el \<nombre-componente\>.component.html:   
Creamos una etiqueta html.   

```html
<h2>Componente Funciona!</h2>
```   

#### 5. En el archivo app.component.html:   
Agregamos el componente que creamos, utilizando una etiqueta Html pero con selector ingresado en \<nombre-componente\>.component.ts, quedando asi:   

```html
<NombreComponenteComponent></NombreComponenteComponent>
```   

Ejecutando el servidor deberiamos estar observando el html creado en el archivo \<nombre-componente\>.component.html.    

	

### Utilizando CLI:   

([mas info](https://www.angularjswiki.com/angular/how-to-delete-a-component-in-angu)).     

```bash
ng generate component <address>/<component_name>
```   

Tambien se pueden utilizar:   

```bash
ng g c <address>/<component_name>
```   

* Para borrar un componente no hay un comando en CLI, sigue las instrucciones de [aqui.](https://www.angularjswiki.com/angular/how-to-delete-a-component-in-angu)

* Transformando la data usando [PIPES.](https://angular.io/guide/pipes)   


* Testacular (now [Karma](https://karma-runner.github.io/latest/index.html)) es una herramienta de test en javascript.
*  [Protractortes](https://www.protractortest.org/#/)

- Video donde explican Angular, y TypeScript
    + https://www.youtube.com/watch?v=k5E2AVpwsko



   
   
## Listening to Events.   

En el \<nombre-component\>.component.html agregamos un boton y colocamos el "escucha de eventos" (listening to events) onClick. Quedando asi el archivo:    

```html
<button (click)="onAddPost()">Save Post</button>
```   

Y en \<nombre-component\>.component.ts, creamos el método "onAddPost", quedando asi:   

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-post-create',
  templateUrl: './post-create.component.html'
})
export class PostCreateComponent {
    onAddPost(){
        alert('Post Added');
    }
  
}
```   

Para [más info](https://angular.io/guide/event-binding) sobre los "Event binding" asi como crear eventos propios.    


## Outputting Content o Salida de contenido.   

Necesitamos dos cosas:   
1.Donde guardar el contenido.   
Creamos una propiedad en la clase del componente y la agregamos a la funcion "onAddPost".   

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-post-create',
  templateUrl: './post-create.component.html'
})
export class PostCreateComponent {
    newPost = 'No Content';

    onAddPost(){
        this.newPost = 'The user\'s post';
    }
  
}  
```   

2.Colocar o mostrar la nueva variable:   

Esto se hace con el "string extrapolation". En el archivo post-create.component.html creamos un <p></p> y agregamos la variable entre doble cochetes {{ variable }}. **Nota: Esta variable puede ser la propiedad o el metodo/funcion de la clase.   

```ts
<textarea rows="6" [value]="newPost" >  </textarea>
<hr>
<button (click)="onAddPost()">Save Post</button>
<p> {{ newPost }}</p>
```   

El valor de la propiedad "value" se puede modificar utilizando los [], y el valor es un typeScript, si queremos ingresar un string, tenemos que agregar '' internas.   

```ts
<textarea rows="6" [value] =" 'Texto' " >  </textarea>
```    

En el caso del parrafo se utiliza la variable, en el textarea podriamos usar lo mismo quedando:   

```ts
<textarea rows="6"> {{ newPost }}  </textarea>
```   

y funciona tambien, pero utilizando los [] podemos modificar las propiedades de las etiquetas de los html, como en este caso la propiedad value de la etiqueta \<textarea\>.   

## Getting User Input. 

Hay dos formas de hacerlo:  

1. <u>Local reference (Referencia local):</u><br>   
	Con una referencia local en el modelo se crean variables en el modelo ( [Template Variables](https://angular.io/guide/template-reference-variables#template-variables) ) para ser usadas y pueden ser usadas para elementos del DOM, directivas (directive) un elemento, entre otros.<br>    
	
	En el modelo usamos el simbolo hash (#) para declarar la variable. Por ejemplo, en el archivo html y el elemento textarea:<br>   
	
	```html
	<textarea rows="6" [value]="newPost" #postInput>  </textarea>
	```   
	
	Agregamos la variable #posInput para ser usada en el archivo nombre.component.ts en un metodo que agregue la variable a otro elemento.    
	
	```ts
	onAddPost(postInput:HTMLTextAreaElement){
        //this.newPost = 'The user\'s post';
        //console.log(postInput);
        //console.dir(postInput);
        this.newPost = postInput.value;  
    }
    ```   
    
    Es este ejemplo, la variable contine un elemento Textarea que es un objeto que tiene la propiedad value y podemos acceder a ella, pero primero hay que hacer el llamdo al metodo que defimos antes, para esto usamos un botton (boton), quedando asi:   
    
    ```html
    <button (click)="onAddPost(postInput)">Save Post</button>
<p> {{ newPost }}</p>
	```   
	
	Entonces, al hacer click en el boton, este llama al metodo "onAddPost" que recibe como parametro un objeto elemento y mostramos el valor en un parrafo usando la propiedad "newPost".   
	
	**NOTA:** En el metodo "onAddPost" hay varias lineas de codigo comentadas, esto su usa para ir verificando que va funcionando, aqui vemos el uso de [console.dir](https://developer.mozilla.org/es/docs/Web/API/Console/dir) que despliega una lista de las propiedades del objeto por la consola.

2. <u>Two way biding.</u>


## Installing Angular Material.   

Información en: <https://material.angular.io/>   


```bash
#Para versiones viejas
npm install --save @angular/material
# Para versiones actuales, usar:
ng add @angular/material

```    

En el archivo package.json agrega:  

```ts
Dependencies: {<br>
	.   
	.   
	.   
"@angular/material": "^11.0.4",   
	.   
	.   
	.    
}<br>
```   

   
Y en el archivo angular.json, agrega:

```
"styles": [
              "./node_modules/@angular/material/prebuilt-themes/indigo-pink.css",
              "src/styles.css"
            ],    
```    
       
            
**NOTA:** Se pueden ver mas themes en la carpeta: node_modules>angular>material>prebuilt-themes    


En el archivo app.module.ts, agrego:   


```ts
import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
```   

En el archivo src/index.html, agrego:    
   
```html
<link href="https://fonts.googleapis.com/css?family=Roboto:300,400,500&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
  ```   
  
  
  
  ```bash
  npm install --save @angular/material@8 --save-exact
  ```
  
  
  




