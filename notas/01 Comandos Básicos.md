# Curso Git y Github

Para instalarlo en manjaro **sudo pacman -S git** 

### Configuración inicial

- **git config** Nos muestras las configuraciones de git 

- **git config --list** Configuración por defecto

- **git config --list --show-origin** Muestra la ubicación donde se encuentran las configuraciones de git. 

- **git config --global user.name "Mi nombre"** Configura el nombre del usuario. 

- **git config --global user.email "Mi correo"** Configura mi correo elecronico. 

### Empecemos

##### Comandos basicos

introducimos git init dentro de la carpeta donde vamos a estar trabajando. Esto creara los archivos necesarios para poder utilizar esta herramienta, si deseas visualziarlos ya sea dentro de la terminal **ls -al**  o en el adminstrador de archivos debesmos mostrar los archivos ocultos. 

- **git status** Nos muestra el status de los archivos 

- **git add**  "Archivo" agregamos el arhivo, poner los cambios de los archivos en memoria ram

- **git add .** Nos agrega a un area en memoria llamada "**Staging**" todos los archivos de la carpeta. 

- **git rm** o **git rm --cathed** Para borrar el archivo en memoria. 

- **git commit -m "Mensaje"** Manda los cambios al repositorio. 

- **git show "Archivo"** Mustra los cambios en un archivo 

- **git log "Archivo"** Muestra los commits realizados en un archivo. 

- **git log --stat** Muestra cambios en los commits pero mas especificos.

- **git diff "Id1" "Id2"** Nos muestra la diferencia en dos versiones del archivo, nos muestra si quitamos algo o pusimos algo etc. Es necesario hacer uso de los IDs de los commits. 

- **git reset** "Id" -- **Hard** o **Soft** Nos permite volver a una versión anterior de un commit, hay dos tipos de reset el duro (**Hard**) este es el que borra cualquier cambio y el mas peligroso aunque es el mas usado, tambien tenemos el suave (**Soft**) que este nos permite guardar los cambios que tengamos en staging, se recomiendo tener cuidado al usar el reset --hard puesto que borra todos TODOS los commits anteriormente realizados a la versión en la que se regreso. 
  
  Este comando nos ayuda a volver en el tiempo. Pero no como git checkout que nos deja ir, mirar, pasear y volver. Con git reset volvemos al pasado sin la posibilidad de volver al futuro. Borramos la historia y la debemos sobreescribir. No hay vuelta atrás.
  Este comando es muy peligroso y debemos usarlo solo en caso de emergencia. Recuerda que debemos usar alguna de estas dos opciones:
  Hay dos formas de usar git reset: con el argumento **--hard**, borrando toda la información que tengamos en el área de staging (y perdiendo todo para siempre). O, un poco más seguro, con el argumento --soft, que mantiene allí los archivos del área de staging para que podamos aplicar nuestros últimos cambios pero desde un commit anterior.

- **git reset --soft** Borramos todo el historial y los registros de Git pero guardamos los cambios que tengamos en Staging, así podemos aplicar las últimas actualizaciones a un nuevo commit.

- **git reset --hard** Borra todo. Todo todito, absolutamente todo. Toda la información de los commits y del área de staging se borra del historial.

- **git reset HEAD** Este es el comando para sacar archivos del área de Staging. No para borrarlos ni nada de eso, solo para que los últimos cambios de estos archivos no se envíen al último commit, a menos que cambiemos de opinión y los incluyamos de nuevo en staging con git add, por supuesto.

- **git checkout "Id" "Nombre del archivo"** Nos regresa a una version de commit anterior, dependiento del Id del commit. 

- **git checkout master "Archivo"** Trae de regreso el ultimo archivo de la rama master. 

- **git rm --cached** Elimina los archivos del área de Staging y del próximo commit pero los mantiene en nuestro disco duro.

- **git rm --force** Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados). 

### Puntos importantes

history ----> Te muestra el historial de comandos que has introducido en la consola. 

**c335fea233aefd18815d0b69f202277bd81cd342** Esto es un identificador de un commit almacenado en la base de datos de git. 

**@@ -1,6 +1,6 @@** Muestra cuantos bytes cambiarón. 

El termino **Merge** hace referencia a cuanto unes los cambios de una rama con otra. 
