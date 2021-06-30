# Tags y Versiones

Las tags nos sirven para delimitar un avance en nuestro proyecto, particularmente se usan en github, pero son creadas desde git. 

Para ver mas a detalle la historia de nuestro proyecto podemos hacer uso del siguiente comando:

```bash
git log --all --graph --decorate --oneline 
```

o también 

```bash
git log --all --graph --decorate --oneline "Archivo"
```

lo que nos arrojara un resultado como el siguiente: 

```bash
* c007ff7 (HEAD -> master, origin/master) Adición de una nueva imagen.
* 7688137 Modificacion en las estilos de las imagenes del post.
* 7043ada Agregue una nueva imagen en la carpeta.
* 81884a5 Modifique el titulo de la pagina
* 1ee1f96 Incluimos el nombre del autor
*   67f6f63 Fusión de mi repositorio local con github Merge branch 'master' of https://github.com/GenaroJavier/Primeros-pasos-con-Git-y-Github
|\  
| * dca99ec Initial commit
* 60af59b Correción de color de fuente
*   9ba8f44 Correción de errores en el merge
|\  
* | 2876899 Modificacion de Titulo y color de fondo en la rama Master
| | * 228256e (origin/cabecera, cabecera) Agregue una imagen nueva al post
| |/  
| * 188137c Modificacion de Titulo y color de fondo
|/  
* 48392db (galeria) Adición de imagenes al post
*   e652686 Ultimas moficaciones antes de la fusion con la rama cabera
|\  
| * 1c3a8ea Creación de la cabecera
| * 15f6b5b Agregamos color de fondo al blog.
| * ffcc154 Commir afuerza por que no se que pedo con esto de las ramas
| * ca849b5 Agregamos gustos musicales
| * b1a7da5 Que hice hoy
| * 0c7e650 Agregamos Autor
| * f5a94ea Creacion de la cabecera
* | b10ad3f Agregue un parrafo adicional al contenido
|/  
| * 3e4a029 (refs/stash) WIP on master: 5ca4768 commit al master del blogpost
|/| 
| * e4b2dca index on master: 5ca4768 commit al master del blogpost
|/  
* 5ca4768 commit al master del blogpost
* 7a1f50b Cambiamos nivel escolar
* c2558c8 Cambio de vida
* f299050 Arranco mi pagina web con HTML y CSS
* be5fad3 Primer commit del archivo
```

# Tags

Creación de una tag 

```bash
$ git tag -a v0.1 -m "Mensaje" 188137c 
# 188137c es el numero del commit donde quieres que se agregue el tag
```

Para listar los tags creados se utiliza el comando: 

```bash
$ git tag 
```

Para poder obtener mas información de un tag, por ejemplo si quieres saber en que parte de la historia se encuentra un tag, se utiliza el siguiente comando. 

```bash
$ git show-ref --tags 
```

Hasta el momento solo hemos estado creando los tags en nuestro repositorio local, donde aquí casi no es de mucha utilidad, por el contrario en github es donde mas importancia toma la creación de los tags, de modo que para enviar nuestros tags locales a guthub se hace lo siguiente: 

```bash
#Traemos el repositorio en github para obtener la versión mas reciente. 
$ git pull origin master 

#Para poder enviar nuestro tag se hace lo siguiente: 
$ git push origin --tags
```

Para poder eliminar un tag se realiza lo siguiente: 

```bash
# Eliminamos el tag "v0.1" es el nombre de tu tag
$ git tag -d v0.1

# Traemos lo que esta en github (es un buena practica)
$ git pull origin master

# Enviamos nuestros tags 
$ git push origin --tags 

# Verificamos que no exista el tag que previamente eliminamos 
$ git tag

# Finalmente eliminamos el tag de manera especial para que no aparezca en github 
$ git push origin :refs/tags/v0.1
```

En linux podemos especificar un alias a un comando que quizas sea un poco complejo de memorizar. Utilizando como ejemplo el comando anterior nuestro alias quedaria de la siguiente forma: 

```bash
$ alias arbolito="git log --all --graph --decorate --oneline"
```

Sin embargo estos alias son temporales, puesto que si reinicias el equipo se pierde el comando. Entonces veamos como declarar un alias para que sea permanente, primero que nada inicamos entrando a la shell de nuestro equipo, esto puede varias segun el SO instalado en nuestra maquina. 

```bash
sudo nano ~/.bashrc 
```

Dentro del archivo, busca un lugar en el archivo donde guardar los alias. Un buen lugar para agregarlos suele ser al final del archivo. Para propósitos de organizaciones, puedes dejar un comentario antes: 

```bash
#alias personalizados
  alias arbolito="git log --all --graph --decorate --oneline"
```

Presionas ctrl + o para guardas, enter y cierras el editar con ctrl + x  y finalizamos actulizando la terminal. 

```bash
source ~/.bashrc
```
