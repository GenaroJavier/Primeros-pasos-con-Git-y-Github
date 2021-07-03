## Creación de ramas

- **gti branch (nombre de la rama)**  Comando que nos permite crear una rama. 

- **Git checkout (nombre de la rama)** Nos permite movernos a una rama diferente. 

- **Git branch** Nos permite ver las ramas creadas en nuestra carpeta.

- **Git merge (nombre de la rama)** fusiona la rama en la que estamos posicionados actualmente con la rama a la que estamos apuntando. 

### Comandos adicionales para ramas

```bash
# nos muestra las ramas existentes y su historia 
$ git show-branch 

# Nos muestra lo mismo pero con un poco mas de informacin. 
$ git show-branch --all 

# Ejemplo 
# Listado de las ramas creadas en nuestro repositorio
! [cabecera] Agregue una imagen nueva al post
 ! [galeria] Adición de imagenes al post
  * [master] Eliminacion de una nota que no tenia nada que ver con este curso
   ! [origin/cabecera] Agregue una imagen nueva al post
    ! [origin/master] Eliminacion de una nota que no tenia nada que ver con este curso

# Commits mas recientes de estas ramas
-----
  * + [master] Eliminacion de una nota que no tenia nada que ver con este curso
  * + [master^] Eliminacion de una nota que no tenia nada que ver con este curso
  * + [master~2] Creación de la carpeta notas, con el fin de guardar los apuntes que estado realizando durante mis practicas en git y github
  * + [master~3] Adición de una nueva imagen.
  * + [master~4] Modificacion en las estilos de las imagenes del post.
  * + [master~5] Agregue una nueva imagen en la carpeta.
  * + [master~6] Modifique el titulo de la pagina
  * + [master~7] Incluimos el nombre del autor
  - - [master~8] Fusión de mi repositorio local con github Merge branch 'master' of https://github.com/GenaroJavier/Primeros-pasos-con-Git-y-Github
  * + [master~8^2] Initial commit
  * + [master~9] Correción de color de fuente
  - - [master~10] Correción de errores en el merge
  * + [master~11] Modificacion de Titulo y color de fondo en la rama Master
+  +  [cabecera] Agregue una imagen nueva al post
+ *++ [cabecera^] Modificacion de Titulo y color de fondo
++*++ [galeria] Adición de imagenes al post


# Con este comando se nos abrira una interfaz grafica con la que podremos observar la historia de nuestro proyectro de una forma mas detallada.
$ gitk 
```

## Creación de mi repositorio remoto en Github

- Para poder subir nuestro repositorio local a github necesitamos haber creado nuestra cuenta previamente. 

- Despues es necesario crear nuestro repositorio para poder obtener nuestro link http. 

- **git remote add origin (ruta http)** nos permite especificar el origen al que vamos a mandar nuestros archivos. 

- ej **git remote add origin  https://github.com/GenaroJavier/Practicas-css-diner.git**

- **git remote** nos dice cual es el origen 

- **git remote -v** nos dice el origen junto con la ruta http 

- **git push origin master** Esto dice que enviemos al origen la rama master. 

- Si nos marca un error, esto se debe a que estas fusionando una rama con otra, siendo mas especifico se origina puesto que al crear un repositorio se crea su propia historia (rama) y entonces nosotros al mandarle nuestra rama, crean un conflicto, es especial si estas ramas se llaman iguales. por consecuente debemos hacer lo siguiente. 

- **git pull origin master**  Trae archivos del repositorio remoto al local 

- **git pull origin master --allow-unrelated-histories** Corrige el error entre ramas con el mismo nombre

- **git push origin master** Envia los archivos del repositorio local al remoto. 

## Notas

- **HEAD** Es el indicador de cual versión de commit estoy viendo de los archivos.
- **pull** Significa traer cosas
- **push** Significa llevar cosas 
- **delta** Es el número de cambios 
