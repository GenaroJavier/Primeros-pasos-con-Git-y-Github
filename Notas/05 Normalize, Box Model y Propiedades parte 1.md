# Normalize

 Los navegadores siempre tienen un estilo por defecto, esto quiere decir que el navegador asigna propiedades a los elementos de una pagina web. 

**Normalize** es un fichero CSS con un tamaño de 8 KB, cuyo principal objetivo es mantener los estilos similares en los navegadores, ya que cada uno agrega sus propios estilos por defecto, por ejemplo te suelen agregar distintos paddings, margins, font-sizes,etc.

Para poder descargarlo debemos acceder al siguiente link [Normalize.css: Make browsers render all elements more consistently.](https://necolas.github.io/normalize.css/) o bien usar el siguiente comando **npm install normalize.css** lo mandamos a llamar como cualquier archivo de CSS. 

# Box Model

Es la caracteristica mas importante de CSS, ya que condiciona el diseño de todas las paginas web, Es el comportamiento que hace que todos los elementos de las paginas se representen mediante cajas rectangulares. 

Las cajas de una pagina se crean automáticamente. Cada vez que se inserta una etiqueta HTML. se crea una nueva caja rectangular que encierra los contenidos de ese elemento. 

| content | line-height |
| ------- | ----------- |
| padding | padding     |
| border  | border      |
| margin  | margin      |

![Screenshot_20210402_231255.png](/home/genaro_javier/Imágenes/Screenshot_20210402_231255.png)

# # Propiedades de cajas

- **background-color** Color de fondo. 

- **display** Cuenta con varios tipos: 
  
  - inline-block Hace que la caja se comporte como si fuese de tipo lineal.

- **pading** Es la distancia que hay entre el texto y la caja, ademas que es un propiedad que podemos acortar 
  
  - **right** derecha 
  
  - **top** arriba 
  
  - **left** izquierda 
  
  - **bottom** abajo 
  
  Para usar el padding lo podemos utilizar de diferentes formas
  
  ```css
  h2 {
      /*Aqui estamos diciendo que hay un padding de 20px en
  todas las direcciones de la caja, top, rigth, bottom y left*/
      padding: 20px; 
  }
  
      /*Si nosotros ponemos lo siguiente, estamos asignando 
  un valor a cada dirección del padding en el siguiente orden
  top, rigth, bottom, left como si fuesen las manesillas del
  reloj*/
  h3 {
      padding: 10px 15px 20px, 30px; 
  }
  ```

- **margin** Es la distancia que hay entre dos cajas y es similar al padding, 

- **border-radius** Nos permite manejar un porcentaje o valor del borde el cual podemos redondear. 

- **border** Con esta propiedad podemos modificar mas aspectos del borde ej. 
  
  ```css
  h1 {
  /*Modificamnos primero grosor del borde, tipo del borde y
  color*/
      border: 4px solid #2C3E50; 
  }
  ```

- **box-shadow**  Es una propiedad que nos permite dar una propiedad a la caja. 
  
  ```css
  h2 {
  /*eje x, eje y, tamaño del desenfoque, tamaño del borde y
  por ultimo el color*/
      box-shadow: 2px 4px 10px 0 #2C3E50;
  }
  ```

- **text-shadow** Es lo mismo pero con el texto con la única diferencia que no tiene el tamaño del borde, si quieres mas intencidad basta con duplicar el efecto. (copiar lo que tienes y pegarlo dos veces, separado con comas)

- **transform** - **rotate()** Rota las cajas segun los grados que tu le indiques. 
  
  #### Outline
  
  Funciona como si fuese un border, con la diferencia de que el Outline no utiliza espacio, el contrario que el border; supongamos que tenemos que una caja con 200px, si nosotros ponemos un border de 10px pues nuestra caja aumentaría nuestra caja a 210px.
  
  Un ejemplo claro de un outiine, es el borde que tiene un input. En pocas palabras el border ocupa un lugar real y afecta a las demás cajas.

## Código Final

```html
<!DOCTYPE html>
<html>
<head>
    <title>Propiedades de Texto</title>
    <link rel="stylesheet" type="text/css" href="css/estilos2.css">
    <link rel="stylesheet" type="text/css" href="css/normalize.css">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Abril+Fatface&family=Hind+Madurai:wght@300&display=swap" rel="stylesheet">
    <!--Fuentes-->
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Abril+Fatface&display=swap" rel="stylesheet">
</head>
<body>
    <!--cajita-->
    <div class="contact-form--2">
        <!--h2-->
        <h1 class="contact-form--2__h1">Titulo 1</h1><h1 class="contact-form--2__h1">Titulo 2</h1>
    </div>
</body>
</html>
```

```css
.contact-form--2{
    font-size: 20px; 
}

.contact-form--2__h1 {
    font-size: 2em; 
    font-weight: 50; 
    font-family: 'Abril Fatface', cursive;
    color: #2C3E50;
    background-color: #FFC300; 
    display: inline-block;
    padding: 100px; 
    box-sizing: border-box;
    text-align: center;
    margin: 10px; 
    border-radius: 30px; 
    border: 0px solid #2C3E50; 
    box-shadow: 5px 5px  4px 2px #2C3E50;
    text-shadow: 5px 5px 10px #67655E;
    transform: rotate(-45deg);

}


.contact-form--2__p {
    font-size: 1em; 
    font-family: 'Hind Madurai', sans-serif;
    color: #000;
}
```
