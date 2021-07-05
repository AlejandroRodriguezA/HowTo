# How to manage Multiples environments and variables  

Documentacion <https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html>

1. Create environment

	```
	Conda create --name <name_env> <library1> <library2> <libraryetc>
	```   
	
2. conda activate <name_env>
3. conda deactivate
4. conda env export > environment.yaml
5. Para crear en environment clonando de otro ambiente:   
	```
	conda env create -f environment.yaml
	```   
6. Para mostrar los ambientes que existen: 
	```
	conda env list
	```

7. Borrar un ambiente:
	
	```
	conda env remove --name project-env

	```
 
	
		
## Para crear variables

7. Ir a la carpeta del environment, ```$ conda env list ``` y crear dos carpetas:   
	- mk -p etc/conda/activate.d   
	- mk -p etc/conda/deactivate.d
	   
8. Dentro de cada carpeta, crear un archivo:   
	- env_vars.sh (.sh para Mac, .bat para windows).   

9. En el archivo de activate:   
	- export VARIABLE="VALOR DE LA VARIABLE"   

10. En el archivo de deactivate:  
	- unset VARIABLE  

## Para el auto-activate

**NOTA:** Hay dos(2) opciones adicionales para hacer esto:   
	- autoenv
	- direnv
   
11. Para programarlo en la terminal:   

	- La carpeta debe contener el archivo environment.yaml
	- En la terminal (bash, zshrc, etc) crear el script:   

	```bash
	chpwd() {
	    if [ -e "environment.yaml" ]; then
	        # echo "environment.yml file found"
	        ENV_NAME=$(head -n 1 environment.yaml | cut -f2 -d ' ')
	        # Check if you are already in the environment
	        if [[ $CONDA_PREFIX != *$ENV_NAME* ]]; then
	          # Check if the environment exists
	          conda activate $ENV_NAME
	          if [ $? -eq 0 ]; then
	            :
	          else
	            # Create the environment and activate
	            echo "Conda env '$ENV' doesn't exist."
	            conda env create -q
	            source activate $ENV
	          fi
	        fi
	    else
	        conda deactivate
	        #PS1=$(echo "$PS1" | perl -pe 's/^\(base\)\s*//' )
	    fi
	}
	
	# Hacemos la llamada a la funcion.
	chpwd
	``` 


	```
	$ conda create --name pag_env --clone Landing_AJ_env
	$ conda env list
	$ conda activate pag_env
	$ conda env export > environment.yaml
	$ conda 
	

## Ver los paquetes del environment

- Si el ambiente no esta activado:

```
conda list -n myenv
```
- Si el ambiente esta activado:

```
conda list
```

- Para ver si un paquete especifico esta en el ambiente:

```
conda list -n myenv scipy
```
