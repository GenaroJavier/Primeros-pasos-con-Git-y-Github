## Creación de ramas

- **gti branch (nombre de la rama)**  Comando que nos permite crear una rama. 

- **Git checkout (nombre de la rama)** Nos permite movernos a una rama diferente. 

- **Git branch** Nos permite ver las ramas creadas en nuestra carpeta.

- **Git merge (nombre de la rama)** fusiona la rama en la que estamos posicionados actualmente con la rama a la que estamos apuntando. 

## Creación de mi repositorio remoto en Github

- Para poder subir nuestro repositorio local a github necesitamos haber creado nuestra cuenta previamente. 

- Despues es necesario crear nuestro repositorio para poder obtener nuestro link http. 

- **git origin add (ruta http)** nos permite especificar el origen al que vamos a mandar nuestros archivos. 

- **git remote** nos dice cual es el origen 

- **git remote -v** nos dice el origen junto con la ruta http 

- **git push origin master** Esto dice que enviemos al origen la rama master. 

- Si nos marca un error, esto se debe a que estas fusionando una rama con otra, siendo mas especifico se origina puesto que al crear un repositorio se crea su propia historia (rama) y entonces nosotros al mandarle nuestra rama, crean un conflicto, es especial si estas ramas se llaman iguales. por consecuente debemos hacer lo siguiente. 

- **git pull origin master**  Trae archivos del repositorio remoto al local 

- **git pull origin master --allow-unrelated-histories** Corrige el error entre ramas con el mismo nombre

- **git push origin master** Envia los archivos del repositorio local al remoto. 

## Notas

- **HEAD** Es el indicador de cual versión de commit estoy viendo de los archivos. 
- **fetch** Significa traer cosas \
- **pull** Significa traer cosas
- **push** Significa llevar cosas 
- **delta** Es el número de cambios 
