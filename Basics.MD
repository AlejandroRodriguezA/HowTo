# Heroku

**Nota:** siguiendo las instrucciones de: <https://www.youtube.com/watch?v=UkokhawLKDU>. En la [paguina oficial](https://devcenter.heroku.com/articles/getting-started-with-python) hay mucha informacion y en español.

## Crear un usuario.  

Ir a la paguina <https://www.heroku.com/>

## Descargar el paquete de herramientas.   

En mi caso usando Mac:   

```
✗ brew tap heroku/brew && brew install heroku
```   

Me dio el siguiente error:   

>xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools), missing xcrun at: /Library/Developer/CommandLineTools/usr/bin/xcrun   


Lo resolvi instalando:   

```bash
✗ xcode-select --install 
```   

y reinstalando el heroku:   

```
✗ brew reinstall heroku
```   

Comprobamos la instalacion, ejecutando la version:   

```bash
✗ heroku --version
›   Warning: Our terms of service have changed:
›   https://dashboard.heroku.com/terms-of-service
heroku/7.47.10 darwin-x64 node-v12.16.2
```   


## Se necesita instalar varias cosas en el proyecto de Django para que funcione con heroku:    

1. Web Server:   
	```bash
 (nombre_env) ➜  Proyecto_nombre git:(main) pip install gunicorn
 Successfully installed gunicorn-20.0.4
 ```   
2. Django-heroku: (dj-database-url, whitenoise y otros que necesite)  

	```bash
	(nombre_env) ➜  Proyecto_nombre git:(main) pip install django-heroku
	```   

3. python-decouple:    

	```bash
	(nombre_env) ➜  Proyecto_nombre git:(main) pip install python-decouple
	Successfully installed python-decouple-3.4
	```  

## Se necesita crear un archivo para decirle que tipo de app es, en nuestro caso es una web.   

```bash 
touch Procfile
```   

**NOTA:** Importante que el nombre sea en mayuscula.   


En el proyecto Django, en el archivo wsgi.py vemos el nombre de nuestra app: (En este caso "Project_name")  

```python
os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'Project_name.settings')
```    

En el archivo Procfile escribimos:

```
web: gunicorn Project_name.wsgi
```   


Para indicarle a heroku que la app es web, se llama "Project_name" y usa gunicorn como servidor.   


## Requisitos de la app.   

En nuestro enviroments tenemos instaladas todas las librerias y extenciones necesarias para ejecutar la app, podemos ver que tenemos instalado ejecutando:   


```bash
(nombre_env) ➜  Proyecto_nombre git:(main) ✗ pip freeze
asgiref==3.3.1
certifi==2020.12.5
dj-database-url==0.5.0
Django==3.1.4
django-heroku==0.3.1
django-widget-tweaks==1.4.8
gunicorn==20.0.4
psycopg2==2.8.6
python-decouple==3.4
pytz==2020.4
sqlparse==0.4.1
whitenoise==5.2.0
```   

Para decirle a heroku que necesita instalar se lo pasamos en un archivo llamado "requirements.txt", podemos hacerlo de dos formas:    

1. Crear el archivo y copiar el resultado de "pip freeze".   
2. Ejecutar, crear el archivo e ingresar el resultado en un solo paso:   

	```bash
	(nombre_env) ➜  Proyecto_nombre git:(main) ✗ pip freeze > requirements.txt
	```   
	
## Configurar Django para trabajar con Heroku.

En el archivo setting:    


```python

import django_heroku
import dj_database_url
from decouple import config


STATICFILES_STORAGE = 'whitenoise.storage.CompressedManifestStaticFilesStorage'

django_heroku.settings (locals())
```   


## Guardamos con git para tener actualizada la version actual con los cambios realizados.  


```bash
(nombre_env) ➜  Proyecto_nombre git:(main) ✗ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   PagAJ/settings.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	Procfile
	requirements.txt

no changes added to commit (use "git add" and/or "git commit -a")
(nombre_env) ➜  Proyecto_nombre git:(main) ✗ git add .
(nombre_env) ➜  Proyecto_nombre git:(main) ✗ git commit -a -m "heroku config"
```   

## Configuracion de Heroku.   

1. Necesitamos loggearnos a heroku desde el terminal. 
	```bash
(nombre_env) ➜  Proyecto_nombre git:(main) heroku login
heroku: Press any key to open up the browser to login or q to exit:
Logging in... done
Logged in as loqueseatu@tumail.com
```    
 
2. Agregar las llaves o identificadores:  

	```bash
	(nombre_env) ➜  Proyecto_nombre git:(main) heroku keys:add
	Could not find an existing SSH key at ~/.ssh/id_rsa.pub
? Would you like to generate a new one? (Y/n)
Uploading /Users/.../.ssh/id_rsa.pub SSH key... done
	```   
	
3. Crear la app en heroku:   

```bash
(nombre_env) ➜  Proyecto_nombre git:(main) heroku create
Creating app... done, ⬢ murmuring-river-88654
https://murmuring-river-88654.herokuapp.com/ | https://git.heroku.com/murmuring-river-88654.git
(nombre_env) ➜  Proyecto_nombre git:(main)
```   

Ya la direccion que da como respuesta (https://murmuring-river-88654.herokuapp.com/) funciona, pero para cambiar el nombre se usa:   

```bash
heroku rename <nombre_escogido>
```   

## Pasar el proyecto a Heroku.   

Utilizando git, se hace un push del proyecto a heroku.   

```bash
git push heroku main
```   

**NOTA 1:** en mi caso el branch es main, recuerden que git el branch por defecto es master, utilizar el que tengan.

**NOTA 2:** Este paso siempre da errores, normalmente heroku te da la solucion, sino San_google que todo lo resuelve. En mi caso tengo que ejecutar:   

```bash
heroku config:set DISABLE_COLLECTSTATIC=1
```   

y se vuelve ha ejecutar el push inicial y ya deberia estar funcionando.   


**NOTA 3:** Me da un error que no encuentra llave secreta de mi proyecto Django, yo tengo configurada mi llave con las variables del envarioments, asi como claves de emails y base de datos.



https://docs.djangoproject.com/en/3.1/howto/deployment/wsgi/

<https://docs.djangoproject.com/en/3.1/howto/deployment/wsgi/gunicorn/> gunicorn myproject.wsgi



 python manage.py collectstatic
 heroku local web
 git push heroku main
heroku open
  







 /app/templates/AJ/AJ/home.html (Source does not exist)
django.template.loaders.app_directories.Loader

	
	
AJ/Templates/AJ/home.html
	
	
Para generar una nueva clave:
	
python:    
    
   ```python shell
	>>> import secrets
	>>> secrets.token_hex(24)
	'55095e4cff3b9440ee625d4f35a420c3fe3320ce48bf2ab1'
	```
	
	Para verificar si tenemos progresql en heroku:
 ➜  Django_Pag git:(main) heroku addons
 
heroku run python manage.py migrate
 heroku run bash
	


 
 



