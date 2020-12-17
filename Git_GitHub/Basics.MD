![git logo](../assets/git/git_logo2.png)

* Paguina Oficial [Git](https://git-scm.com/) o `https://git-scm.com/`
* Paguina del libro:[GIT Book](https://git-scm.com/book/en/v2) `https://git-scm.com/book/en/v2`



## **Comandos:**

- **Git init**.Inicia el repositorio. Por defecto crea la rama o branch "master".  


	``` 
	$ git init
	```


- **git status**.Muestra el estatus de los archivos.  

	```
	$ git status
	```


- **Git add**.Agrega los archivos. Si los archivos no estan agregados los agrega al stage. 
 
	```
    $ git add .  -> Agrega todos los archivos
    $ git add archivo.ext  -> Agrega el archivo espeficifo

    ```
- **Git rm** --cached <file>]: Remueve el archivo y lo deja fuera del proyecto a guardar.  

	```
    $ git rm --cached <file>
    Nota: 	Si quieren borrarlo de la carpeta usando -f 
    		fuerzan su borrado

    ```
- **Git commit**. Guarda en repositorio los archivos. Pasa al repositorio todos los archivos que esten en "stage".  

	```
	$ git commit		-> Abre un editador de texto para ingresar
						nombre del commit
   $ git commit -m "Nombre o variable de ese commit"
   $ git commit -a	-> Hace el commit sin pasar por el stage

    ```
- **Git restore** .Descarta los cambios en los archivos que estan en el "stage".  

	```
	$ git restore <file>
	```
## **Git Braching:**    

	- **Mostrar** todas las ramas o branches que existen: 
	
	~~~
	$ git branch			
		main				
		* master			-> y selecciona con * la que esta activa.
	~~~
	- Para **crear** una nueva:   

	~~~
	$ git branch <branch_name>
	Ej:
	$ git branch main
	~~~
	- Para **cambiar** de una branch a otra:   
	
	~~~
	$ git checkout <name_branch>
	Ej:
	$ git checkout main
	...
	Switched to branch 'main'
	~~~
	- Para **borrar** o eliminar una branch.  
	
	~~~
	$ git branch -d <name_branch>
	Ej:
	$ git branch -d master
	Deleted branch main (was e264106).
	~~~
	- Para "juntar" o merge dos branch:  
		1. Me ubico en la branch principal.  
		
				$ git checkout <name_branch_principal>  
		
		2. Uno las dos branch's. 
		 
				$ git merge <name_branch_secundaria>   
				
		3. Elimino la branch secundaria.  

				$ git branch -d <name_branch_secundaria>   
				
		Ejemplo:
		![git logo](../assets/git/git-merge.png)   
		
				$ git checkout master
				Switched to branch 'master'
				$ git merge hotfix
				.
				.
				.
				$ git branch -d hotfix
				Deleted branch hotfix (...)   
				
		Mas informacion en: 
		[git-merge]
		(https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)   
		
		![git logo](../assets/git/git-merge2.png)
		
			
	
	