# 05 Git Ignore



Imaginemos que estamos desarrollando una pagina web utilizando el API de twitter, recodando como es trabajar con dicha API, poder poder tener conexión con la misma es requerido 2 pares de credenciales, las cuales son privadas y usadas únicamente por el desarrollador. 

Otro ejemplo claro son las imágenes en las paginas web, si queremos que nuestra web tenga imágenes en alta calidad estas requieren de un tamaño considerable, ademas que es una mala practica subir archivos binarios cuando trabajamos con github o cualquier gestor de repositorios remotos.

Teniendo en consideración estos ejemplos, es necesario que algunos archivos específicos no sean enviados al repositorio remoto en github. Para ello existe la herramienta de .gitignore la cual especifica que algunos archivos no sean enviados a github. 

## Creación

Para poder crearlo es tan simple como crear un archivo y nombrarlo **.gitignore** o si queremos sentirnos hackers podemos hacerlo todo desde consola. 

```bash
$ touch .gitignore
$ nano .gitignore
#Dento del archivo especificamos que archivos queremos que no sean enviados
#puden ser desde todos los archivos que compartan el mismo tipo o 
#especificar que archivo desea que no se envie. ej
*.jpg
historia.txt
```

Ahora que se a realizado la creación del archivo .gitignore y la especificación de los archivos que no queremos que sean enviados, tenemos que especificarle a git que se realizo la creación de dicho archivo. para ello introducimos: 

```bash
$ git add .gitignore
$ git status 
$ git commit -am "Cambio realizado"
$ git pull origin master
$ git push origin master
```


