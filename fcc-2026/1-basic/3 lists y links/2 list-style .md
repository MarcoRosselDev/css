# ¿Cómo funcionan las diferentes propiedades de estilo de lista? 

En CSS, la propiedad `list-style` se utiliza para controlar la apariencia de las listas en una página web. 
Ya sea que trabajes con listas ordenadas (`ol`) o listas no ordenadas (`ul`), 
la propiedad `list-style` te permite personalizar cómo se muestran los elementos de la lista. 
La propiedad `list-style` es en realidad una abreviatura de otras tres propiedades:
* list-style-type
* list-style-position
* list-style-image
Cada una cumple una función diferente en la apariencia de las listas. 
---
## list-style-type
La propiedad `list-style-type` permite definir el tipo de viñeta o número que se utiliza en una lista. 
Para listas no ordenadas, se puede elegir entre varios estilos de viñeta, como discos, círculos o cuadrados.
Para listas ordenadas, puede utilizar diferentes sistemas de numeración, como decimal, 
números romanos o incluso caracteres alfabéticos. 
Aquí hay un ejemplo de cómo usar `list-style-type`.
```html
<ul style="list-style-type: square;">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```
En este ejemplo, las viñetas de la lista desordenada se convierten en cuadrados. 
La propiedad `list-style-type` es la más utilizada de las tres, 
ya que afecta directamente la apariencia de la viñeta o el estilo de numeración en las listas. 
---
## list-style-position
La propiedad `list-style-position` controla la posición de la viñeta 
o el número en relación con el contenido del elemento de la lista. Se pueden usar dos valores: `inside` y `outside`.
Cuando se utiliza el valor fuera del contenido, la viñeta o el número aparece fuera del mismo, 
que es el comportamiento predeterminado. 
Y, cuando se utiliza el valor dentro del contenido, la viñeta o el número aparece dentro del mismo, 
lo que puede provocar que el texto se ajuste y se alinee con la viñeta o el número. 
Aquí hay un ejemplo de cómo usar list-style-position:
```html
<ul style="list-style-position: inside;">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
<ul style="list-style-position: outside;">
  <li>Item 4</li>
  <li>Item 5</li>
  <li>Item 6</li>
</ul>
```
En este ejemplo, se proporcionan valores `inside` y `outside` para dos etiquetas de lista no ordenada diferentes. 
La propiedad `list-style-position` puede ser útil cuando se desea controlar la alineación del contenido de la lista,
especialmente en situaciones donde hay varias líneas de texto en un solo elemento de la lista.
---
## list-style-image
La propiedad `list-style-image` te permite usar una imagen como viñeta para los elementos de tu lista. 
Esto puede ser útil para añadir un estilo visual único a tus listas. 
Aquí tienes un ejemplo de cómo usar list-style-image.
```html
<head>
  <style>
    ul {
      list-style-image: url('https://cdn.freecodecamp.org/platform/universal/freecodecamp-org-gravatar.jpeg');
      list-style-position: inside;
    }
  </style>
</head>
<body>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
</body>
```
En este ejemplo, las viñetas se reemplazan por un logotipo personalizado de freeCodeCamp, 
lo que le da un toque personal a la lista. 
Al usar `list-style-image`, asegúrese de que la imagen que elija sea pequeña 
y adecuada para el diseño de su página web. 
Si la imagen es demasiado grande o compleja, puede dificultar la lectura de la lista.
Puedes combinar las tres propiedades — `list-style-type`, `list-style-position` y `list-style-image`— 
en una única propiedad abreviada de `list-style`. 
El orden de los valores en la propiedad abreviada no importa, pero se pueden especificar los tres juntos. 
Aquí tienes un ejemplo usando la propiedad abreviada:
```html
<ul style="list-style: circle inside url('https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg');">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```
En este ejemplo, los elementos de la lista utilizan viñetas cuadradas, 
ubicadas dentro del contenido, con una imagen personalizada como viñeta. 
Sin embargo, si la imagen no está disponible o no se muestra, se utilizarán las viñetas cuadradas como alternativa.