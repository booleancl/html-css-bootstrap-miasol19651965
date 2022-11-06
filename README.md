# HTML CSS BOOTSTRAP

# HTML CSS BOOTSTRAP

Html CSS y Javascript son los pilares de toda aplicación o sitio web. Cualquier cosa que funcione dentro de un navegador web (chrome, mozilla, safari) utiliza estos pilares. Y no solo eso, hoy también se pueden hacer aplicaciones "nativas" con estas tecnologías.

## HTML

Significa **Hyper Text Markup Language**, que en castellano sería algo como Lenguaje de marcado de hyper texto. Lenguaje de marcado es por la *Etiquetas*. Dependiendo de su etiqueta el navegador lo procesa de diferente forma. Y el hyper texto se refiere a que estos documentos están enlazados por *links*.

Con HTML crearemos *documentos estructurados* mediante etiquetas que el navegador puede interpretar.

El documento principal de un sitio o aplicación de debe llamar **index.html**. Todo junto y en minúsculas.

### Doctype

Esta primera etiqueta indica al navegador la versión de HTML. En este caso indica que es la versión 5.
```html
  <!DOCTYPE html>
```

### html
Luego de eso viene la primera etiqueta que es parte del documento. la famosa etiqueta **html**:
```html
<html lang="es">
  ...
</html>
```

Del ejemplo anterior vemos que esta etiqueta se compone de 2 partes principales. La etiqueta de apertura `<html>` y la de cierre `</html>`.

Entremedio de las etiquetas de apertura y cierre irá el contenido.

Además vemos la etiqueta de apertura tiene el **atributo** `lang="es"`, lo que le indica al navegador en qué idioma está el contenido del documento.

>**ATENCIÓN**: Solo las etiquetas de apertura pueden tener atributos, Las etiquetas de cierre no.

### head

A continuación viene etiqueta `head`. Esta etiqueta entrega información al **Navegador** sobre como visualizar el contenido que vendrá en las siguientes secciones. Por ejemplo se indica mediante etiquetas `meta` el set de caracteres que utilizará la página. Ejemplo:

```html
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hola Microsystem</title>
</head>
```

La tercera etiqueta `meta` que tiene el atributo `name="viewport"` permite que el contenido se cargue inicialmente considerando el tamaño de pantalla disponible, desde grandes a muy pequeños.

Además dentro del head se encuentra la etiqueta `title`, que es la encargada de mostrar el nombre del sitio en la pestaña del navegador.

Por otra parte dentro del `head` podemos cargar otros recursos que utilizará el documento como por ejemplo hojas de estilo CSS o archivos Javascript

### Estructura Jerárquica

Algo que es muy muy muy importante notar y que no es tan evidente, es que los documentos HTML forman una estructura jerárquica bien definida del tipo árbol. Donde la etiqueta raíz es la etiqueta `html`. Lo podemos visualizar de la siguiente forma

```html
  <html>
    <head></head>
    <body></body>
  </html>
``` 

Esto es muy importante de comprender ya que luego manejaremos las etiquetas pensando en su ubicación relativa dentro del árbol. Y pensaremos que las etiquetas son **nodos** que tienen **nodos padre**, **hermanos** y **nodos hijos**.

## Etiquetas principales

### Tìtulos
Las etiquetas para hacer tìtulos son las etiquetas **h** con nùmeros del 1 al 6. Ejemplos
```html
<h1>Sùper tìtulo</h1>
 <h2>Super sub titulo</h2>
 <h3>Supr sub sub titulo</h3>
<h4>....</h4>
<h5>...</h5>
<h6>..</h6>
```
### Links
Los links son el corazòn de internet y los crearemos frecuentemente. Se componen de el atributo `href` que indica el destino del link y su contenido, que es lo que se muestra al usuario
```html
 <a href="headings.   html">Tìtulos</a>
 ```
### Imagenes
 Las imàgenes son una

### Etiquetas no semanticas
Estas etiquetas no tiene un significado propio y sirven como contenedor para agrupar otras etiquetas
## div
```html
<div>
  <p>Hola mundo</p>
</div>
```
## spam
La etiqueta span se puede usar dentro de un texto.
```html
<div>
  <p>Hola<span>mundo</span></p>
</div>
```
La idea detras de los elementos no sematicos es utilizar css para darles estilo.
Mas adelante, en este modulo veremos lo frecuente de su uso el marco de trabajo o framework Bootstrap.

## Formacion
Contiene controles interactivos para ingresar informacion
```html
<form action="/searc" method="get">
```
</form>
```
Cuando enviamos el formulario mediante el estago ´get´, los parametros ingresados quedan reflejados en la url despues del sigo ´?´ y separados por ´&´.

## CSS

Hojas de estilo en cascada (cascada style sheets) CSS nos permite entregar al sitio el aspecto que queremos . Lo hace aplicando reglas de estilo sobre los diferentes elementos del HTML.

Los navegadores tienen estilos predefinidos para mostrarlas diferentes etiquetas.

Cuando el codigo CSS esta definido dentro del mismo archivo HTML , se denomina css-inline, pero no es la mejor forma de definir los estilos que se van a utilizar en varias paginas. Para eso es mejor utilizar un archivo externo y vincularlo al html.

## selectores

En el ejemplo anterior el selector era la misma etiqueta, es decir, la regla de estilo aplica a **todas** las etiquetas de ese tipo. Tenemos otros 2 selectores muy frecuentes. El selector por 'id' y por 'clase'.

El 'id' es un atributo de las etiquetas HTML. Toda etiqueta HTML puede tener el atributo 'id' para diferenciarlos del resto. Y podemos usar este abributo como selector css usando la notacion '#'

'''css
#fname{ 
    border-radius: 6px;
} 
'''

Ejemplo de selector por clase
'''css
.some-class{ 
    border-radius: 6px;
}
'''
css es muy flexible y permite combinar selectores. Ej:

'''css
/* Esta regla aplica a los parrafos con clase centered*/
p.centerred { 
    text-align: center;
    color: purple;
}
'''

Si tenemos reglas que se repiten . ejemplo

'''css
h1 { 
    text-align: center:
    color: blue
}

'''

Podemos refactorizarlo en una sola regla:

'''css
h1 h2{ 
    text-align: center;
    color: blue
}
'''

Slector | Ejemplo | descripcion
--------|---------|-------|
#id | #some-id | selecciona el elemento con 'id="some-id"'
.class | .some-class | Selecciona TODOS los elementos con clase 'class="some-class"'
element.class | p. intro | Selecciona solo los '<p>' con clase 'class="intro"'
element, element  | div, p | Selecciona todos los elementos '<div>' y '<p>'

### Modelo de caja

En esencia cada elemento html esta inserto dentro de una caja que consiste de: Margen, borde, Padding y contenido.

![Box Model](img/box-model.png)

### Unidades de medidas

En general, no solo en desarrollo, podemos clasificar las unidades de medidas en dos grupos:

- Unidades Absolutas: px
- Unidades Relativas: %, rem, em, vh, vw

### rem
Es una unidad de medida relativa al font-size del elemento raiz.

### em
Es relativa al front-size del mismo elemento

### vh
Es relativo al 1% del alto de la pantalla (viewport)

### vw
Es relativo al 1% del ancho de la pantalla o viewport

### Tipos de diseño

- El diseño estatico: sirva para un solo tamaño de pantalla

- El diseño fluido: Se basa en porcentajes(%)dependiendo del tamaño de la pantalla.

- Diseño responsivo: Tiene puntos de quiebre (distintos tamaños)para aplicar diferentes estilos.

### CSS Mediaqueries

Utiliza la regla '@media' para incluir un bloque de propiedades CSS solo si la condicion es verdadero. Ejemplo:

'''css
/* si el tamaño de la pantalla es de 600px o menor, el color del fondo del body sera verde*¨/@media only screen and (max-width: 600px){ 
    body { 
        background-color: green
     }
}
'''
Existen ciertos tamaños de pantallas mas o menos estandarizados y estas serian sus respectivas media queries:

'''css

'''css
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {...}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {...}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {...}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {...}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {...} 

### Display

*/si el tamaño de la pantalla es de 600px o menor, el color de fondo del body sera verde */ @media only screen and (max-width: 600px){ 
    body { 
        background-color: green
    }
    p{ 
        display: none
    }
}
'''

El valor de la propiedad display modifica como el navegador posicionara la caja del elemento.

La caja puede ser de lado a lado, en este caso la propiedad display tendra ell valor 'block'. Tambien podemos establecer el valor como 'inline' y en ese caso, la caja sera del menor tamaño posible.  Ejemplo:

'''css
.side-to-side{ 
    display: block;
    margin: solid
}
.narrow{ 
    display: inline
    margin: solid
}
'''

### Marcos de trabajo o frameworks CSS

Los marcos de trabajo CSS traen hecho el css responsivo listo para ser utilizado. En general se utilizara mediante clases css. El framework define una serie  de clases y utilidades que han sido disenadas y probadas para cumplir con los requisitos de un diseno moderno y usable.

Uno de los mas famosos es Bootstrap. Un marco de trabajo de codigo libre utilizado en millones de sitios y apps.

### Bootstrap

Bootstrap basa su enfoque en dividir el espacio disponible en una grilla de filas y columnas. Mediante las clases 'row' y 'col'.

Bootstrap es un framework orientado al desarrollo mobile, es decir, su principal preocupacion son los dispositivos pequeños. Se llama a si mismo un framework "Mobile Firt"

