# HTML Y CSS :clipboard:

> **Resumen de referencia rápida y guía de aprendizaje para HTML5 y CSS3.**

## Índice

* [HTML](#html-)

  * [Estructura Base (`<head>`)](#estructura-html-head-)

  * [Configuración del Head](#head)

  * [Estructura Semántica (`<body>`)](#estructura-html-body-)

  * [Contenido del Body](#body)

  * [Encabezados y Navegación](#header)

  * [Enlaces (`<a>`)](#anchor)

  * [Agrupación y Semántica](#main-y-div)

  * [Texto y Formato](#p)

  * [Tablas](#table-tr-td-th)

  * [Multimedia](#figure-figcaption-img)

  * [Formularios](#form)

* [CSS](#css-)

  * [Sintaxis Básica](#sintaxis-de-css)

  * [Propiedades de Texto y Color](#propiedades---texto)

  * [Selectores y Especificidad](#selector-universal-o-por-etiqueta)

  * [Unidades de Medida](#unidades-de-medida)

  * [Modelo de Caja (Box Model)](#modelo-de-caja)

  * [Visualización y Posicionamiento](#display)

# HTML 🏗️

HTML (*HyperText Markup Language*) es el lenguaje de marcado que define la estructura y el contenido de una página web.

## Estructura HTML (head) 📁

```
<!DOCTYPE html>
<html lang="es">
<head>
    <!-- Configuración básica y metadatos -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Título de la Página</title>

    <!-- Enlaces a archivos externos -->
    <link rel="stylesheet" href="styles.css">
    <script src="script.js" defer></script>
</head>
<body>
    <!-- Contenido visible de la página -->
</body>
</html>

```

## Head

La etiqueta `<head>` contiene información sobre el documento (metadatos) que no se muestra directamente en el navegador, pero es fundamental para el funcionamiento, indexación (SEO) y diseño de la página.

* `<title>`: Define el título visible en la pestaña del navegador y en los resultados de búsqueda.

* `<link>`: Permite enlazar recursos externos como hojas de estilo (`CSS`), fuentes web o el icono de la página (*favicon*).

* `<script>`: Carga y ejecuta código JavaScript.

* `<meta>`: Define los metadatos como la codificación de caracteres, la descripción para buscadores o el viewport responsive.

```
<!-- Enlace a estilos e icono -->
<link rel="icon" type="image/x-icon" href="favicon.ico">
<link rel="stylesheet" type="text/css" href="styles.css">

<!-- Inclusión de JavaScript -->
<script src="app.js"></script>

<!-- Metadatos de la página -->
<meta name="author" content="Nombre del Autor">
<meta name="description" content="Descripción concisa sobre el contenido de la web para motores de búsqueda.">

```

## Estructura HTML (body) 📁

```
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Estructura Semántica</title>
</head>
<body>
    <header>
        <h1>Título Principal</h1>
        <nav>
            <ul>
                <li><a href="#inicio">Inicio</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section>
            <article>
                <h2>Título del Artículo</h2>
                <p>Contenido explicativo del artículo.</p>
            </article>
        </section>

        <aside>
            <p>Contenido secundario o barra lateral.</p>
        </aside>
    </main>

    <footer>
        <p>&copy; 2026 Todos los derechos reservados.</p>
    </footer>
</body>
</html>

```

## Body

El elemento `<body>` contiene todo el contenido ejecutable y visual (texto, imágenes, tablas, enlaces, reproductores) que será renderizado directamente en la pantalla del navegador.

## Header

Engloba la cabecera principal de la página o de una sección. Suele contener:

* Logotipos o nombres de la marca.

* El encabezado principal (`<h1>`).

* Menús de navegación (`<nav>`).

* Buscadores internos.

## h1, h2, h3, h4, h5, h6

Definen la jerarquía de los encabezados del sitio web. Ayudan tanto a la lectura visual como al posicionamiento SEO y a la accesibilidad.

* **`<h1>`**: Encabezado principal de mayor importancia. **Solo debe haber uno por página.**

* **`<h2>` a `<h6>`**: Subencabezados de nivel secundario a inferior organizados de forma jerárquica.

## Nav

Indica un bloque principal de navegación. Agrupa enlaces internos o externos orientados a mover al usuario por la estructura del sitio.

### Listas en navegación

Para estructurar un menú de navegación se suelen utilizar listas:

* `<ul>`: Lista no ordenada (con viñetas).

* `<ol>`: Lista ordenada (con números o letras).

* `<li>`: Elemento individual dentro de la lista.

### Anchor

La etiqueta `<a>` (*anchor*) crea hiperenlaces hacia otros sitios web, archivos, direcciones de correo o secciones internas de la misma página.

**Atributos clave:**

* `href`: Dirección URL o ancla de destino.

* `target`: Define dónde abrir el enlace (`_self` abre en la misma pestaña, `_blank` en una nueva).

```
<nav>
    <ul>
        <li><a href="#seccion1" target="_self">Ir a Sección 1 (Misma pestaña)</a></li>
        <li><a href="https://www.google.com" target="_blank" rel="noopener">Google (Nueva pestaña)</a></li>
        <li><a href="documento.pdf" download>Descargar PDF</a></li>
    </ul>
</nav>

```

## Main y div

* **`<main>`**: Encapsula el contenido único e idóneo de la página web. Solo debe existir uno por documento.

* **`<div>`**: Contenedor neutro a nivel de bloque sin valor semántico. Se utiliza exclusivamente para agrupar elementos y aplicarles estilos CSS o manipularlos desde JavaScript.

## Article y Section

* **`<section>`**: Agrupa un conjunto de contenidos conceptualmente relacionados (ej. sección de comentarios, sección de servicios, bloque de contacto).

* **`<article>`**: Representa una composición autónoma e independiente que tiene sentido por sí misma (ej. una entrada de blog, una noticia, una reseña).

## Aside

Representa un bloque de contenido indirectamente relacionado con el contenido principal (ej. barras laterales, listas de enlaces recomendados, publicidad o cajas de autor).

## P

La etiqueta `<p>` define párrafos de texto. Es el elemento básico para escribir y organizar la lectura en el documento web.

## Footer

Indica el pie de página del documento o de una sección específica.

* Suele incluir avisos legales, enlaces a redes sociales, mapas del sitio y derechos de autor (`copyright`).

* La etiqueta **`<address>`** se emplea dentro de `<footer>` para indicar información de contacto (física, telefónica o digital) del propietario o autor.

## Strong

`<strong>`: Indica que su contenido tiene **alta importancia o urgencia semántica**. Por defecto, los navegadores lo renderizan en **negrita**, aunque mediante CSS su aspecto gráfico puede modificarse.

## em

`<em>`: Otorga **énfasis semántico** a una parte específica del texto dentro de la frase. El navegador la renderiza por defecto en *cursiva*.

## Span

`<span>`: Contenedor neutro en línea (*inline*). No genera saltos de línea ni añade significado semántico; se usa para aislar fragmentos de texto y darles formato con CSS o JS.

## Etiquetas para formatear

Existen etiquetas visuales que modifican la apariencia del texto sin aportar peso semántico. Es aconsejable priorizar CSS para estos fines, aunque siguen vigentes:

| Etiqueta | Función | 
| ----- | ----- | 
| `<b>` | Texto en negrita por estética (sin importancia semántica). | 
| `<i>` | Texto en cursiva (términos técnicos, idioma extranjero, etc.). | 
| `<u>` | Texto subrayado. | 
| `<mark>` | Texto resaltado visualmente. | 
| `<small>` | Texto de tamaño reducido (notas al pie, avisos). | 
| `<br>` | Salto de línea manual. | 
| `<hr>` | Línea divisoria horizontal (cambio temático). | 

## table, tr, td, th

Permiten representar datos tabulares organizados en filas y columnas.

```
<table>
    <caption>Ventas Globales de Videojuegos</caption>
    <thead>
        <tr>
            <th>Posición</th>
            <th>Título</th>
            <th>Ventas</th>
        </tr>
    </thead>
    <tbody>
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
    </tbody>
    <tfoot>
        <tr>
            <td colspan="2">Total acumulado</td>
            <td>565K</td>
        </tr>
    </tfoot>
</table>

```

* **Estructura:**

  * `<caption>`: Título de la tabla.

  * `<thead>`: Agrupa las filas de encabezado.

  * `<tbody>`: Agrupa las filas de datos.

  * `<tfoot>`: Agrupa las filas de cierre o totales.

* **Celda y filas:**

  * `<tr>`: Define una fila.

  * `<th>`: Celda de encabezado (negrita y centrada por defecto).

  * `<td>`: Celda de datos común.

* **Atributos de extensión:**

  * `colspan="n"`: Hace que una celda ocupe el ancho de *n* columnas.

  * `rowspan="n"`: Hace que una celda ocupe el alto de *n* filas.

## Figure, figcaption, img

### Img

Permite insertar imágenes. Es una etiqueta de cierre propio (*self-closing*).

* `src`: Ruta del archivo de imagen.

* `alt`: Descripción textual de la imagen (clave para la accesibilidad y el SEO).

* `width` / `height`: Dimensiones del recurso en píxeles.

### Figure y Figcaption

`<figure>` engloba contenido multimedia autónomo (imágenes, diagramas, código) y admite la etiqueta `<figcaption>` para agregar una leyenda aclaratoria o pie de imagen.

```
<figure>
    <img src="mascota.jpg" alt="Perro labrador jugando con una pelota" width="400">
    <figcaption>Figura 1: Mi perro disfrutando en el parque.</figcaption>
</figure>

```

## Audio

Inserta reproductores de sonido en la web. La etiqueta `<source>` permite suministrar diferentes formatos para garantizar compatibilidad entre navegadores.

```
<audio controls>
    <source src="pista.mp3" type="audio/mpeg">
    <source src="pista.ogg" type="audio/ogg">
    Tu navegador no soporta el elemento de audio.
</audio>

```

## Video

Inserta reproductores de video con características avanzadas de control visual.

```
<video width="640" height="360" controls poster="portada.jpg">
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    Tu navegador no admite reproducción de vídeo.
</video>

```

### Integración mediante Iframe (Youtube, Vimeo...)

Para incrustar reproductores de servicios de video externos se emplea la etiqueta `<iframe>`:

```
<iframe 
    width="560" 
    height="315" 
    src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
    title="Reproductor de vídeo"
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
</iframe>

```

## Form

Permite construir formularios dinámicos interactivos para que los usuarios envíen datos hacia un servidor.

```
<form action="/procesar-datos.php" method="POST">
    <!-- Campo de texto asociado a su etiqueta -->
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" name="nombre" placeholder="Escribe tu nombre" required>

    <label for="correo">Correo electrónico:</label>
    <input type="email" id="correo" name="correo" required>

    <!-- Botón de envío -->
    <button type="submit">Enviar datos</button>
</form>

```

* **Atributos de `<form>`:**

  * `action`: Ruta del servidor que procesará los datos.

  * `method`: Método HTTP con el que se envían los datos (`GET` o `POST`).

* **Atributos y elementos clave:**

  * `<label for="id">`: Asocia un texto explicativo con su respectivo `<input id="id">`.

  * `<input type="...">`: Define el tipo de dato a recoger (`text`, `email`, `password`, `number`, `checkbox`, `radio`, `submit`, etc.).

# CSS 🎨

CSS (*Cascading Style Sheets*) es el lenguaje utilizado para describir la presentación visual, colores, tipografía y distribución de los documentos HTML.

## Sintaxis de CSS

El diseño en CSS se basa en reglas formadas por un **selector**, un conjunto de **propiedades** y sus **valores** correspondientes:

```
selector {
    propiedad: valor;
    propiedad: valor;
}

```

**Ejemplo básico:**

```
p {
    color: #333333;
    font-size: 16px;
}

```

## Propiedades - Texto

Permiten modificar el aspecto de la tipografía y la legibilidad de los textos.

```
p {
    font-family: "Helvetica Neue", Arial, sans-serif; /* Tipografía (con fallback) */
    font-size: 18px;                                 /* Tamaño de fuente */
    font-weight: bold;                               /* Grosor: normal, bold, 100-900 */
    font-style: italic;                              /* Estilo: normal, italic, oblique */
    line-height: 1.5;                                /* Altura e interlineado de la línea */
    letter-spacing: 1px;                             /* Espaciado entre caracteres */
    text-align: center;                              /* Alineación: left, right, center, justify */
    text-decoration: underline;                      /* Decoración: none, underline, line-through */
    text-transform: uppercase;                       /* Conversión: uppercase, lowercase, capitalize */
}

```

## Propiedades Colores

Podemos aplicar color al texto mediante la propiedad `color` utilizando distintas notaciones:

```
.ejemplo-colores {
    color: red;                          /* Nombre del color (Named Colors) */
    color: #FF0000;                      /* Hexadecimal (#RRGGBB) */
    color: rgb(255, 0, 0);               /* Modelo RGB */
    color: rgba(255, 0, 0, 0.8);         /* Modelo RGBA con canal Alfa (Transparencia de 0 a 1) */
    color: hsl(0, 100%, 50%);            /* Modelo HSL (Matiz, Saturación, Luminosidad) */
}

```

## Propiedades para Colores y Fondos

Permiten definir colores de fondo, imágenes decorativas o transparencias sobre elementos HTML.

```
div {
    background-color: #f4f4f4;                 /* Color de fondo */
    background-image: url('imagen.jpg');      /* Imagen de fondo */
    background-repeat: no-repeat;              /* Mosaico: repeat, no-repeat, repeat-x, repeat-y */
    background-position: center center;        /* Posición de la imagen */
    background-size: cover;                    /* Ajuste: cover, contain, auto */
    opacity: 0.9;                              /* Opacidad general del elemento (0 a 1) */
}

```

## Selector Universal o por Etiqueta

* **Selector Universal (`*`):** Selecciona **todos los elementos** dentro del documento HTML.

```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

```

* **Selector por Etiqueta / Elemento:** Afecta a todas las instancias de esa etiqueta HTML específica.

```
h1 {
    color: navy;
}

/* Agrupación de selectores compartiendo propiedades */
h2, h3, h4 {
    color: #2c3e50;
    font-family: sans-serif;
}

```

## Selector de Clase (.)

Aplica estilos a elementos específicos que compartan un atributo `class="..."`. Un mismo elemento puede tener múltiples clases asignadas separadas por espacios.

```
<p class="destacado texto-grande">Este texto usará ambas clases CSS.</p>
<em class="destacado">Este texto usará solo destacado.</em>

```

```
/* Aplica a cualquier elemento con class="destacado" */
.destacado {
    background-color: yellow;
}

/* Aplica únicamente a las etiquetas <em> que tengan class="destacado" */
em.destacado {
    color: red;
}

```

## Selector de Identificador (#)

Aplica estilos a un único elemento que posea un atributo `id="..."` específico. Un identificador **debe ser único** por página.

```
<p id="titular-principal">Este es el título único.</p>

```

```
#titular-principal {
    color: green;
    font-weight: bold;
}

```

> ⚠️ **Jerarquía y Especificidad CSS:**
>
> `Estilos en línea (style="")` > `#id` > `.clase` > `etiqueta` > `*`

## Unidades de Medida

### Relativas

Se calculan en relación con la pantalla, el elemento padre o la raíz del documento. Son ideales para diseño responsive.

* `em`: Relativa al tamaño de fuente (`font-size`) del **elemento padre**.

* `rem`: Relativa al tamaño de fuente (`font-size`) definido en el **elemento raíz (`<html>`)**.

* `vw`: Porcentaje del ancho total de la ventana (*Viewport Width*). `1vw = 1%`.

* `vh`: Porcentaje del alto total de la ventana (*Viewport Height*). `1vh = 1%`.

* `ch` / `ex`: Basadas en el ancho del carácter `0` o en la altura de la letra `x` de la fuente actual.

### Absolutas

Tienen un valor fijo independiente del dispositivo o contexto.

* `px` (píxeles): La unidad fija más extendida en diseño de pantallas.

* `pt` (puntos): `1pt = 1/72` de pulgada (muy usado en archivos para impresión).

* `cm`, `mm`, `in`: Centímetros, milímetros y pulgadas reales.

### Porcentuales (%)

Miden proporcionalmente el tamaño del elemento con respecto a las dimensiones de su elemento contenedor o padre.

### Tamaño: width y height

Definen los anchos y altos límites que pueden tomar los elementos.

```
.caja {
    width: 100%;           /* Ocupa el 100% del contenedor padre */
    height: 300px;         /* Altura fija */
    min-width: 250px;      /* Ancho mínimo: jamás se encogerá por debajo de este valor */
    max-width: 1200px;     /* Ancho máximo: jamás se estirará más allá de este valor */
}

```

## Modelos de Caja

En CSS, todo elemento expuesto en pantalla se considera una **caja rectangular**. El **Box Model** está compuesto por 4 áreas concéntricas de dentro hacia afuera:

1. **Content (Contenido):** Área interna donde residen el texto o las imágenes.

2. **Padding (Relleno):** Espacio transparente entre el contenido y el borde.

3. **Border (Borde):** Borde delimitador que rodea el padding.

4. **Margin (Margen):** Espacio exterior transparente que separa la caja de otras cajas vecinas.

```
+-----------------------------------+
|               MARGIN              |
|  +-----------------------------+  |
|  |           BORDER            |  |
|  |  +-----------------------+  |  |
|  |  |        PADDING        |  |  |
|  |  |  +-----------------+  |  |  |
|  |  |  |     CONTENT     |  |  |  |
|  |  |  +-----------------+  |  |  |
|  |  +-----------------------+  |  |
|  +-----------------------------+  |
+-----------------------------------+

```

```
.caja-ejemplo {
    width: 200px;
    padding: 20px;
    border: 2px solid black;
    margin: 15px;
}

```

### Margin y Padding

Tanto `margin` como `padding` pueden especificarse para lados individuales o mediante la sintaxis abreviada (*shorthand*):

```
.ejemplo-espaciado {
    /* Forma individual */
    margin-top: 10px;
    margin-right: 15px;
    margin-bottom: 10px;
    margin-left: 15px;

    /* Sintaxis abreviada: [top] [right] [bottom] [left] (sentido de las agujas del reloj) */
    padding: 10px 15px 10px 15px;

    /* Sintaxis abreviada: [top/bottom] [left/right] */
    padding: 10px 15px;

    /* Sintaxis abreviada: los 4 lados iguales */
    margin: 20px;
}

```

## Display

Controla cómo se comporta una caja en la maquetación y la forma en que interactúa con sus elementos adyacentes.

* `display: block;`
  Ocupa todo el ancho disponible horizontalmente y fuerza un salto de línea antes y después. Se le pueden aplicar propiedades de ancho (`width`) y alto (`height`). *(Ejemplo: `<div>`, `<p>`, `<h1>`)*.

* `display: inline;`
  Solo ocupa el ancho de su propio contenido y se coloca al lado de otros elementos en línea sin hacer salto de página. **No permite** modificar `width` ni `height`. *(Ejemplo: `<span>`, `<a>`, `<strong>`)*.

* `display: inline-block;`
  Se alinea horizontalmente con otros elementos como si fuera `inline`, pero **sí admite** personalizar dimensiones de `width`, `height`, `margin` y `padding`.

* `display: none;`
  Oculta por completo el elemento de la pantalla y el DOM renderizado. **No ocupa espacio**.

## Visibilidad de Capas

A diferencia de `display: none;`, la propiedad `visibility` y `opacity` permiten controlar el estado visual sin destruir el espacio reservado de la caja:

* `visibility: hidden;` Oculta el elemento, pero este **sigue ocupando su espacio físico** dentro de la maquetación.

* `opacity: 0;` Vuelve transparente el elemento, pero este sigue presente en pantalla e interactúa con el cursor/eventos.

## Overflow

Determina la forma en que el navegador reacciona cuando el contenido de un elemento excede las dimensiones (`width`/`height`) del contenedor donde está encerrado.

```
.caja-overflow {
    width: 200px;
    height: 100px;
    
    overflow: visible; /* (Por defecto) El contenido sobrepasa los bordes de la caja */
    overflow: hidden;  /* Recorta y oculta el contenido que sobresalga */
    overflow: scroll;  /* Agrega barras de desplazamiento siempre visibles */
    overflow: auto;    /* Muestra barras de desplazamiento solo cuando sea necesario */
}

```

## Position

Define la estrategia utilizada para calcular la ubicación física de un elemento dentro de la página web.

* `position: static;` *(Valor por defecto)*
  Sigue el flujo natural del documento. Las propiedades de coordenadas (`top`, `right`, `bottom`, `left`, `z-index`) **no surten efecto**.

* `position: relative;`
  El elemento se desplaza respecto a la posición original que ocuparía en el flujo. No altera la posición de los elementos que le rodean.

* `position: absolute;`
  El elemento se descuelga del flujo normal del documento y se posiciona en relación con su **contenedor ancestro más cercano que tenga una posición distinta a `static`**.

* `position: fixed;`
  El elemento se descuelga del flujo y se posiciona respecto a la ventana del navegador (*Viewport*). Se mantendrá **fijo en pantalla** aunque el usuario haga desplazamiento/scroll.

* `position: sticky;`
  Combinación de `relative` y `fixed`. Se comporta como `relative` hasta que el desplazamiento alcanza un punto determinado, momento en el que se vuelve `fixed` y queda anclado.

```
/* Ejemplo de menú fijo superior */
header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
}

```
