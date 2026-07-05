# ¿Cuál es la diferencia entre elementos en línea y elementos de `block` en CSS? 

En HTML y CSS, los elementos se clasifican como elementos en línea o elementos de `block`, 
y esta clasificación determina su comportamiento en el diseño del documento. 
Comprender esta diferencia es fundamental para controlar cómo se muestra el contenido en una página web.
---
## block elements (elementos en bloque)
Los elementos de nivel de `block` son aquellos que ocupan todo el ancho disponible por defecto, 
extendiéndose a lo largo de su contenedor. 
Estos elementos siempre comienzan en una nueva línea y desplazan el resto del contenido a la siguiente, 
creando un "`block`" de contenido. 
Los elementos de nivel de `block` tienen aplicada por defecto la propiedad CSS `display: block;`. 
Esta propiedad garantiza que el elemento se extienda para llenar el ancho del contenedor 
y aparezca en una nueva línea.

Algunos elementos comunes de nivel de bloque son los elementos div, los párrafos, los encabezados, 
las listas ordenadas, las listas no ordenadas y los elementos section. 
Aquí hay un ejemplo de código de un elemento de nivel de bloque:
```html
<p style="border: 2px solid red;">
  First paragraph
</p>
<p>Second paragraph</p>
```
En este ejemplo, tenemos dos elementos de párrafo, donde el primero tiene un borde rojo. 
Los dos elementos de párrafo no comparten la misma línea porque, 
por defecto, son elementos de bloque. 
Por lo tanto, ambos elementos de párrafo ocuparán todo el ancho de su contenedor, 
que en este caso es el elemento body.

Los elementos de bloque son ideales para organizar el contenido verticalmente, 
como párrafos, secciones o bloques de texto extensos. 
Se utilizan habitualmente para definir la estructura y el diseño de una página web. 
---
## Inline elements (elemntos en linea)
Los elementos en línea, a diferencia de los de bloque, 
solo ocupan el ancho necesario y no comienzan en una nueva línea. 
Estos elementos se integran con el contenido, permitiendo que el texto 
y otros elementos en línea aparezcan junto a ellos.

Los elementos en línea tienen la propiedad CSS `display: inline;` aplicada por defecto. 
Esta propiedad garantiza que el elemento permanezca dentro del flujo del contenido 
y no salte a una nueva línea. 
Algunos ejemplos comunes de elementos en línea son `<span>`, `<a>` e `<img>`.
Aquí tienes un ejemplo para comprender mejor los elementos en línea:
```html
<p>This is a
  <span style="color: red; border: 2px solid green;">red</span>
  word inside a paragraph.
</p>
```
En este ejemplo, tenemos un elemento `<span>` anidado dentro de un elemento `<párrafo>`. 
El elemento `<span>` tiene texto rojo con un borde verde para que la palabra resaltada se vea mejor. 
Como puede observar, el elemento `<span>` solo ocupa el espacio de la palabra "rojo" 
y no desplaza el contenido siguiente a una nueva línea.
Los elementos en línea se utilizan mejor para dar estilo a porciones más pequeñas de texto 
o contenido dentro de una línea, como enfatizar una palabra, crear hipervínculos 
o aplicar estilos específicos a partes de un párrafo.