# Conexión Git - Github por SSH

### Configuración de llaves SSH propias

- Nos colocamos en el **/home/(usuario)**  de nuestro sistema. 

- **ssh-keygen -t rsa -b 4096 -C "nuestro correo electrónico"** Con este comando generamos nuestro par de llaves. 

- Nos pedirá una ruta para guardar nuestras llaves, si no estamos en el home, es recomendable guardarlo en esa ruta, por el contrario si ya nos encontramos en dicha ruta únicamente presionamos Enter. 

- A continuación nos pedirá una "passphrase" que es una contraseña en la que podemos incluir espacios, después de introducir nuestra contraseña presionamos Enter. 

- Al terminar de introducir estos comandos, se nos generaran 2 archivos, en la siguiente ruta: **cd ~/.ssh** llamados **id_rsa** (llave privada) y **id_rsa.pub** (llave publica). 

- Para poder hacer la conexion Computadora - Github por medio del protocolo SSH es necesario conocer si dicho protocolo esta activo en nuestro ordenador, esto lo podemos verificar con el comando: 
  
  ```bash
  $ eval $(ssh-agent -s)
  ```
  
  Al introducirlo nos arrojara un mensaje como: **Agent pid 4724** esto quiere decir que el servicio se encuentra en ejecución. 

- Por ultimo y no por ello menos importante, es necesario que la computadora conozca nuestra llave privada para poder realizar la conexión con github, de modo que es necesario ubicarnos en la raiz de nuestro sistema y introducimos el siguiente comand:
  
  ```bash
  $ cd /
  $ ssh-add ~/.ssh/id_rsa
  ```
  
  Recuerda que **id_rsa** es nuestra llave privada. Al darle enter nuestra llave privada habrá sido añadida a nuestro sistema. 

### Configuración en Github

- Dentro de github nos dijimos al apartado de configuraciones 

- En el apartado de la izquierda tendremos una lista con varias opciones, damos click en **SSH & GPG keys** 

- Agregamos un titulo 

- Nos dirigimos a la carpeta donde están alojadas nuestras llaves generadas anteriormente. **~/.ssh** y abrimos el archivo que termina en **.pub** una vez dentro copiamos todo el contenido y regresamos a github debajo del titulo esta un recuadro que nos pide la lleve, ahí dentro pegamos lo que estaba en el archivo **.pub** y damos click en el botón **add SSH key** con esto tendremos lista la conexión de git con github por medio de SSH. 

## Notas

- Nunca compartas tu llave privada

- Es recomendable generar un par de llaves SSH (publicas y privadas por equipo) 

- El signo **~** en la terminal significa el **home** siendo mas especifico la ruta **/home/(usuario)** 
