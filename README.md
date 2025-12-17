# HTML Y CSS :clipboard:
RESUMEN DE HTML Y CSS PARA EXAMEN 

# HTML

## Estructura HTML (head) 📁
```HTML
<!DOCTYPE html>
<html lang="en">
   <head> <!-- información de la página y será lo primero que se cargue-->
       <meta charset="UTF-8">
       <title>Document</title>
       <!--
       enlazar archivos css
       enlazar archivos js
       añadir fuentes externas
       metadatos (keywords, descriptions, robots, author, owner)
        -->
   </head>
   <body> <!-- contenido de la página -->
   </body>
</html>
```
## Head 
- La etiqueta *head* contiene informacion que se precarga
- *title* indicaremos el nombre de la pagina
- *link* nos permite "incluir" diversos ficheros entre ellos, como el icono de la pagina

- Usaremos *link* o *script* para hacer referencias a ficheros css que use nuestra web
```HTML
<script src="file_name.js"></script>
<link rel=¨stylesheet¨ type=¨text/css¨ href=¨file_name.css¨>
```
- *meta* nos permite definir metadatos de nuestra pagina web, por ejemplo: autor, descripcion...
```HTML
<meta name="author" content="Chris Mills">
<meta name="description" content="The MDN Learning Area aims to provide complete beginners to the Web with all they need to know to get started with developing web sites and applications.">
```

## Estructura HTML (body) 📁 
```HTML
<!DOCTYPE html>
<html lang="en">
<head><title></title></head>
<body>
   <header><!--Logo, título principal, menús de navegación, etc…-->
       <h1>Título principal</h1>
       <h2>Subtítulo</h2>
       <nav>Menú navegación</nav>
   </header>
   <main><!-- Pondremos todo el contenido principal -->
       <section><!--Sección del contenido-->
           <article><!--artículo dentro de la sección-->
               <h3>Título del artículo</h3>
               <p>Contenido del artículo</p>
           </article>
       </section>
   </main>
   <footer>Document</footer>
</body>
</html>
```

## Body 
Elemento principal, es el contenedor de toda la inforamcion que sera renderizada en el navegador y donde ira nuestro contenido

## Header 
El elemento que engloba a todos los elementos que pertenen a una cabecera, en este caso a la cabezera de nuestra pagina.
Ahi encontraremos el titulo de la pàgiona, el logo, menu de navegacion, buscador, enlaces a rrss

## h1, h2, h3, h4, h5 
Cada h1, h2, h3... representa un titulo dentro de nuestra pagina y servira para organizarla
- h1 debe estar dentro del header que es lo que primero analiza

## Nav
Indica que hay un menu de navegacion y agrupa el resto de elementos que permite movernos dentro de la pagina o otras paginas del site
- Dentro del nav podemos encontrar:
  - ul: lista de elementos desordenada
    - li: representa un elemento de la lista
    -  a: enlace
  - ol: lista ordenada
    - li: representa un elemento de la lista
    - a: enlace    

### Anchor
Dentro de una lista podemos definir enlñaces que tenga, para eso usaremos:
- a: Todo su contenido sera el que nos envie al enlace definido
  - href: Indicaremos la direccion del enlace
  - target: Si se abre en una nueva pestaña o no
```HTML
 <nav>
       <ul>
           <li><a href="#sec2art4" target="_self">sec2art4</a></li>
           <li><a href="http://www.google.com" target="_blank">Google</a></li>
           <li><a href="imagenes/rana.jpg" target="_blank">Rana</a></li>
           <li><a href="otraPagina.html">Otra página de mi web</a></li>
       </ul>
   </nav>
```

## Main y div 
*main* donde esta la informacion principal del cuerpo de nuestra pagina
*div* la etiqueta mas empleada puesto que permite agrupar elementos y esto nos permite organizarnos

## Article y Section
*article* engloba muchos elementos diferentes que juntos dan un contenido. 
*section* permite englobar un conjunto de contenido que tienen relacion entre si, podemos tener una seccion, muchos otros elementos lo importante esque todos estan relacionados entre ellos

## Aside
*aside* contiene los elementos que no son parte del contenido principal, pero que sí están relacionado con él. 

## P
La etiqueta *p* de párrafo es esencial para introducir contenido dentro de la página. 

## Footer 
*footer* es la etiqueta que indica el pie de página, la encontraremos por lo tanto al final del código.
*address* es una etiqueta usal del footer en la cual encontraremos la dirección postal de la entidad de la página.

## Strong
**strong** nos permite hacer más énfasis a ese texto, darle más fuerza semántica, destacarlo. Visualmente se verá en negrita (o no), pero este no es su cometido, en CSS podríamos cambiarlo.

## em
*em* es una etiqueta que al igual que <strong> permite dar más relevancia a la parte del texto que contiene, pero esta vez su formato será en itálico

## Span
*span* etiqueta que no hace saltos de línea, visualmente en el navegador no hay ningún cambio

## Etiquetas para formatear
Etiquetas que no dan valor semántico al contenido sino que las usamos para cambiar la manera visual del texto en cuestión.

## table, tr, td, th
*table* para crear la table
*tr* para crear cada fila
*td* para crear cada columna
```HTML
<table>
 <tr>
   <th>Rank</th>
   <th>Title</th>
   <th>Sales</th>
 </tr>
 <tr>
   <td>1</td>
   <td>Minecraft</td>
   <td>350K</td>
 </tr>
 <tr>
   <td>2</td>
   <td>Grand Theft Auto V</td>
   <td>215K</td>
 </tr>
  <tr>
   <td>3</td>
   <td>Wii Sports</td>
   <td>83K</td>
 </tr>
</table>
```
- Existen los atributos rowspan y colspan que nos permiten decir cuantas filas o columnas ocupa esa celda.
- La etiqueta <caption> sirve para establecer el título de una tabla:
- Las partes que componen las tablas complejas se definen mediante las etiquetas:
   - *thead*: la cabecera de la tabla
   - *tbody*: sección de datos
   - *tfoot*: el pie de la tabla que pongamos donde pongamos aparecerá al final (ver ejemplo).

## Figure, figcaption, img 
*figure* es la etiqueta específica para poner una imagen que engloba varios elementos más:

Usaremos la etiqueta *img* y usaremos los atributos: 
   - src (source) para indicar la ruta relativa de la imagen.
   - alt* para indicar el texto informativo que aparece cuando mouse hover y cuando no se puede cargar la imágen.
   - width: permite especificar el ancho de la imagen (px, %, ...). 
   - height: permite especificar el alto de la imagen (px, %, ...).
```HTML
<img src="https://picsum.photos/id/237/200/300" alt="perro hambriento"/>
<img src="imagenes/logo_itb.png" alt="logo de ITB" width="100"/>
```

A *figure* le podemos añadir la etiqueta *figcaption* para poner el texto que acompaña a la imagen, su leyenda.
```HTML
<h1>The figure and figcaption element</h1>

<figure>
  <img src="pic_trulli.jpg" alt="Trulli" style="width:100%">
  <figcaption>Fig.1 - Trulli, Puglia, Italy.</figcaption>
</figure>
```

## Audio
La etiqueta *audio* es la que nos permite añadir un audio dentro de nuestra página, en el caso que queramos añadir más de un audio usaremos el elemento *source*

## Video
La etiqueta *video* es la que nos permite añadir un vídeo dentro de nuestra página, en el caso que queramos añadir más de un video usaremos el elemento *source*

Usar *iframe* para añadir un enlace al vídeo en youtube:
   - width, height  para marcar la anchura y altura del reproductor, en píxels.
   - src (source) para indicar la ruta del archivo, en este caso una url
   - frameborder=”0” para activar los controles de reproducción de audio (play, stop, etc).
   - allowfullscreen permite reproducir el video a pantalla completa (no hay que darle valor, solo añadir esta propiedad).

## Form
- Para crear un formulario en HTML, debemos usar el elemento *form*.
- A partir de aquí se irán añadiendo los elementos que queremos que estén en nuestro formulario usando **input type=""**. 
- El atributo action del <form> nos permite indicar qué acción se llevará a cabo en el momento de hacer “submit” en el botón del formulario.
- *label* es la etiqueta que permite poner un nombre/título al campo del formulario.
```HTML
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="Your name"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Your surname"><br><br>
  <input type="submit" value="Submit">
</form>
```

 # CSS
