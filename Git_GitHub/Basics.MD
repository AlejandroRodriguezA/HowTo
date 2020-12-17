GIT
===

Paguina del libro: https://git-scm.com/book/en/v2

# Comandos:

- [git init][Inicia el repositorio]. Por defecto crea la rama o branch "master"
- [git status][muestra el estatus de los archivos].
- [git add][Agrega los archivos]. Si los archivos no estan agregados los agrega al stage.
    + $ git add .  -> Agrega todos los archivos
    + $ git add archivo.ext  -> Agrega el archivo espeficifo
- [git rm --cached <file>]: Remueve el archivo y lo deja fuera del proyecto a guardar
    + Si quieren borrarlo de la carpeta usando -f fuerzan su borrado
- [git commit][Guarda en repositorio los archivos]. Pasa al repositorio todos los archivos que esten en "stage".
    + $ git commit -m "Nombre o variable de ese commit"
- [git restore <file>][Descarta los cambios en los archivos que estan en el "stage"]
- [git commit -a][Hace un commit con todos los archivos aunque no esten en "Stage area"]
