[Curso](https://youtube.com/playlist?list=PL4cUxeGkcC9gUgr39Q_yD6v-bSyMwKPUI)

Nota: tsc --init Para crear el archivo tsconfig

"outDir": "./public",                        /* Redirect output structure to the directory. */
"rootDir": "./src",                       /* Specify the root directory of input files. Use to control the output directory structure with --outDir. */

al final se incluye lo siguiente:
 "include":["src"]

 Para que solo compile lo que esta dentro de la carpeta "src"

Para compilar cada vez que se guarde de forma automatica
```bash
tsc ~w 
Starting compilation in watch mode...
```