# ¿Qué son algunos estilos predeterminados del navegador aplicados a HTML? 

Al empezar a trabajar con HTML y CSS, 
notará que algunos estilos se aplican a sus páginas web incluso antes de escribir cualquier código CSS. 
Estos estilos se denominan "estilos predeterminados del navegador" o "estilos del agente de usuario". 
Estos estilos predeterminados del navegador proporcionan un formato básico 
para garantizar que los elementos HTML se muestren de forma legible en todos los navegadores.

Sin embargo, estos estilos pueden variar ligeramente de un navegador a otro, 
por lo que es importante comprenderlos al diseñar una apariencia consistente para su sitio web. 

Veamos algunos estilos predeterminados comunes de los navegadores aplicados a varios elementos HTML. 

Los encabezados (h1-6) son uno de los elementos HTML más utilizados y, 
por defecto, tienen diferentes tamaños y grosores.

Sin embargo, estos estilos pueden variar ligeramente de un navegador a otro, 
por lo que es importante comprenderlos al diseñar una apariencia consistente para su sitio web. 
Veamos algunos estilos predeterminados comunes de los navegadores aplicados a varios elementos HTML. 
Los encabezados son uno de los elementos HTML más utilizados y, 
por defecto, tienen diferentes tamaños y grosores.
```html
<!-- Headers del 1 al 6 -->
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```
Otro elemento con estilos predeterminados es el elemento `<hr>`, 
que crea una línea horizontal que se usa a menudo para separar visualmente secciones de contenido. 
Los navegadores generalmente aplican un estilo de línea simple a este elemento. 
Para entenderlo mejor, veamos este ejemplo de código:
```html
<p>Paragraph 1</p>
<p>Paragraph 2</p>
<hr>
<p>Paragraph 3</p>
<p>Paragraph 4</p>
```
La línea horizontal aparece como una línea fina con espacio por encima y por debajo del texto para diferenciar las secciones de contenido. 
---

A continuación, veremos el elemento `blockquote`. 
Los blockquotes se utilizan para indicar una sección de texto que es una cita de otra fuente. 
Los navegadores suelen añadir sangría y, a veces, ponen el texto en cursiva. 
La sangría ayuda a distinguir los blockquotes del resto del texto, 
dejando claro que este contenido es una cita de otra fuente.

Veamos un ejemplo:
```html
<p>Paragraph 1</p>
<p>Paragraph 2</p>
<blockquote>I think, therefore I am. (Rene Descartes)</blockquote>
<p>Paragraph 3</p>
<p>Paragraph 4</p>
```
En el ejemplo anterior, el elemento blockquote producirá una sangría en el texto, 
aplicada por los estilos predeterminados del navegador. 
---
Otro elemento con estilos predeterminados es el elemento de anclaje `(<a>)`, 
que tiene un color azul predeterminado y está subrayado para que se reconozca como un enlace. 
Veamos el siguiente ejemplo HTML.
```html
<p>Paragraph 1</p>
<p>Paragraph 2</p>
<a href="https://freecodecamp.org/">Visit the freeCodeCamp learn page</a>
<p>Paragraph 3</p>
<p>Paragraph 4</p>
```
El código anterior tiene cuatro elementos de párrafo con un elemento de anclaje en el medio. 
El elemento de anclaje está estilizado en azul con un subrayado para indicar 
a los usuarios que vayan a la página de aprendizaje de freeCodeCamp.
--- 
Finalmente, veremos los elementos de lista desordenada y ordenada. 
Los navegadores añaden formato básico a las listas, 
incluyendo sangría y viñetas o números, 
dependiendo de si se trata de una lista desordenada (ul) o una lista ordenada (ol).
Veamos un ejemplo.
```html
<p>Sample Paragraph</p>
<ol>
  <li>item 1</li>
  <li>item 2</li>
  <li>item 3</li>
</ol>
<ul>
  <li>item</li>
  <li>another item</li>
  <li>yet another item</li>
</ul>
<p>Ending Paragraph</p>
```
En el ejemplo de código anterior, estamos usando una lista desordenada y una lista ordenada. 
Ambas listas tendrán una ligera sangría a la derecha por defecto. 
En todos estos ejemplos, viste cómo el navegador aplicó espaciado predeterminado, 
diferentes tamaños de fuente y grosores a estos elementos HTML. 

En lecciones posteriores, aprenderás cómo restablecer algunos de estos estilos predeterminados usando un restablecimiento de CSS.