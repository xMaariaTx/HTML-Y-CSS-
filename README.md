# HTML Y CSS :clipboard:
RESUMEN DE HTML Y CSS PARA EXAMEN 

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
- La etiqueta <head> contiene informacion que se precarga
- *<title>* indicaremos el nombre de la pagina
- *<link>* nos permite "incluir" diversos ficheros entre ellos, como el icono de la pagina

- Usaremos *<link>* o *<script>* para hacer referencias a ficheros css que use nuestra web
```HTML
<script src="file_name.js"></script>
<link rel=¨stylesheet¨ type=¨text/css¨ href=¨file_name.css¨>
```
- <meta> nos permite definir metadatos de nuestra pagina web, por ejemplo: autor, descripcion...
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
<main></main>
 
