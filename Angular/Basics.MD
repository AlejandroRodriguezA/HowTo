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

     
* Para generar un nuevo componente ([mas info](https://www.angularjswiki.com/angular/how-to-delete-a-component-in-angu)).   
    ```bash
    ng generate component <address>/<component_name>
    ```
	Tambien se pueden utilizar:  

    ```bash
    ng g c <address>/<component_name>
    ```

* Para borrar un componento no hay un comando en CLI, sigue las instrucciones de [aqui.](https://www.angularjswiki.com/angular/how-to-delete-a-component-in-angu)

* Transformando la data usando [PIPES.](https://angular.io/guide/pipes)   


* Testacular (now [Karma](https://karma-runner.github.io/latest/index.html)) es una herramienta de test en javascript.
*  [Protractortes](https://www.protractortest.org/#/)

- Video donde explican Angular, y TypeScript
    + https://www.youtube.com/watch?v=k5E2AVpwsko
