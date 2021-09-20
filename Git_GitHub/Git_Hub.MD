
# Una vez creado el repositorio en GitHub. Estas son las recomendaciones de GitHub:

- Crea un alias para la direccion del repositorio ```git remote add nombre direccion_repositorio```.

    + Ejemplo:

    ```bash
    git remote add origin https://github.com/ajra80/HowTo.git
    ```
- Para ver que repositorio remotos tengo utilizo:
```bash
$ git remote
origin
```


- [git branch -M nombre_nuevo][ la opcion -M, Mueve o cambia el nombre de la rama actual,incluso si esta ya existe]
    + Ejemplo:  $ git branch -M main
- [git push -u origin main][Guarda en el repositorio externo origin la rama main, -u significa aguas arriba]
