# Terminal

- **touch** - Crear un archivo:
    * touch \<name_file.ext\>
    
    ```bash
    touch test.txt
    touch Documents/.../test.txt
- **rm** - Borrar un archivo:
	
	```bash
	rm test.html
	```
	
	-rf se utiliza para borrar subcarpetas y documentos
	
	```
		$ rm -rf my-first-proyect-v2
	```
	    
- **mkdir** - Crear un directorio:
    * mkdir \<name_foulder\>    
    
    ```bash
    mkdir text
    mkdir Documents/.../text
    ```
    * mkdir -p /<carpeta>/<carpeta_2>/<file>: Crea, si no existe las carpetas indicadas.
    
- **cat** - Ver el contenido de un archivo por pantalla:
    * cat \<name_file.ext\>   
    
    ```bash
    cat text.txt
    ```
- **pbcopy** - Copiar el contenido del archivo en el porta papeles:

	```bash
		$ cat filename.abc|pbcopy
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
- **cat** Se utiliza para visualizar el contenido de un documento por el terminal.
- **kill** ```kill <pid>``` y **killall** ```kilall mongod```
- **lsof** Indentifica el pid ```lsof -i :<port>```. Otra opcion es instalar nmap con brew.
- **chown** Cambiando el permiso y dueño de archivos y documentos. Con la opcion "-l" del comando "ls" podemos ver los permisos asignados a cada documento y/o archivo, por ejemplo:
	```
Alex: ~
$ ls -l ~/Mongodb/
total 8
drwxr-xr-x  26 Alex  staff  832 Jul 24 11:59 node1
-rw-r--r--   1 Alex  staff  329 Jul 24 11:50 node1.conf
drwxr-xr-x   2 root  staff   64 Jul 24 12:06 pki
	```
	
[mas info en](https://www.cyberciti.biz/faq/how-to-use-chmod-and-chown-command/)


- Para abrir una aplicacion en ventana nueva:

    ```bash
    $ code ~/Documents/README.MD --new-windown
    ```
- **open** Abreel finder del directorio, por ejemplo ```open . ``` abre el actual directorio. [Flavio](https://www.freecodecamp.org/news/the-linux-commands-handbook/)
                                        
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
* command + K = limpia el terminal, la diferencia con control + L, es que no puedes ver lo anterior.
* control + o = Copia la toda la linea. Esto es un plugin "copybuffer" de OHMYZSH!.




1. Informacion importante de LINUX y Terminal para MongoBD: [Info Linux] (https://university.mongodb.com/mercury/M103/2021_July_13/chapter/Chapter_0_Introduction_Setup/lesson/5eaafca87c4bdbe505e9ca5f/lecture). Como por ejemplo:
	* Estructura de directorios en Linux.
	* Permisos en carpetas y documentos.
	* Cambios en el dueno de carpetas/documentos.
	* 

2. Informacion sobre el comando ***chmod*** que se usa para cambiar los permisos de archivos/documentos. [chmod](https://www.december.com/unix/ref/chmod.html)









