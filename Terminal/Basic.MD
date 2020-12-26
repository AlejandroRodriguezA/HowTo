# Terminal

- **touch** - Crear un archivo:
    * touch \<name_file.ext\>
    
    ```bash
    touch test.txt
    touch Documents/.../test.txt

    ```
- **rm** - Borrar un archivo:
	
	```bash
	rm test.html
	```
	    
- **mkdir** - Crear un directorio:
    * mkdir \<name_foulder\>    
    
    ```bash
    mkdir text
    mkdir Documents/.../text
    ```
- **cat** - Ver el contenido de un archivo por pantalla:
    * cat \<name_file.ext\>   
    
    ```bash
    cat text.txt
    ```
- **cd** - Navegacion por los archivos: 

    ```bash
    cd ~ (me dirige al directorio raiz /Users/tu_usuario)
	cd .. (sube al directorio anterior)
	cd Documents/ (entra en el directorio "Documents")
	cd ~/folder (Sin importar donde estes va a la carpeta indicada. Tienes que saber la ruta exacta de la carpeta)
	cd ~/**/Programacion (te dirige a la carpeta Programacion buscando en todo el ordenador, si no sabes donde esta)
	Nota: Si existe mas de un archivo con ese nonbre da un error.
	```
- **mv** - Renombra el archivo:
    * mv \<source\> \<target\> 	
    
    ```bash
    mv test.txt test.MD (Cambia el nombre del archivo o carpeta)
    ```
- **ls** Muestra el contenido de la carpet:

	```bash
	ls -la  // Muestra la lista de archivos incluyendo los ocultos.
	ls -ld .??* // Muestra solo los archivos ocultos en el directorio actual.
	

- **pwd** - Muestra la ruta del directorio actual de trabajo.

	```bash
	$ cd ~
	$ pwd
	/Users/tu_usuario
	```
	
- **source** - 

	```bash
	source .zshrc			// Actualiza el shell
	```

- **mdfind** kind:folder "folder_name"

- **pwd | pbcopy** Copia en el porta papeles la ruta actual.
- **pbpaste** Pega lo que tiene el porta papeles.

- Para abrir una aplicacion en ventana nueva:
    ```bash
    $ code ~/Documents/README.MD --new-windown
    ```
                                        
## Text Command Line Shortcuts 
[agradecimientos](https://wilsonmar.github.io/mac-osx-terminal/#open-terminal-several-ways)

* control + C = Close processing
* control + L = CLear screen
* control + A = Go to Beginning of line (as in A to Z)
* control + E = Go to End of line (hit E using longest finger)
* control + F = Forward cursor
* control + B = Backward
* control + H = Backspace left of cursor
* control + D = Delete right of cursor
* control + K = Kill line from under the cursor to the end of the line.
* control + U = "U get out of here" - Clear entire line
* control + P = Previous line
* control + N = Next line
* control + Y = Retrieve line
* control + ` = cycle through session windows
* control + left = previous session
* control + right = previous session


