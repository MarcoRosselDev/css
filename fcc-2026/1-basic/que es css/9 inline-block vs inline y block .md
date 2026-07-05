# ¿Cómo funciona `inline-block` y en qué se diferencia de los elementos `inline` y `block`? 

Al trabajar con CSS, a menudo te encuentras con tres tipos diferentes de comportamiento 
de visualización para los elementos: 
        `inline`, `block` e `inline-block`. 
Cada una de estas propiedades afecta cómo se posicionan los elementos 
y cómo interactúan con otros elementos en la página.

En esta lección, nos centraremos en cómo funciona la propiedad `inline-block` 
y en qué se diferencia de los elementos `inline` y `block`. 
Los elementos `block` se comportan como grandes contenedores 
o "bloques" que ocupan todo el ancho de su contenedor padre. 
Siempre comienzan en una nueva línea y su altura y anchura se pueden ajustar. 
Los elementos `inline` solo ocupan el espacio necesario. 
Se ajustan al contenido circundante y no saltan a una nueva línea.
---
La propiedad `inline-block` es un híbrido de estos dos comportamientos. 
Al igual que los elementos `inline`, los elementos `inline-block` permanecen en el flujo de texto 
sin comenzar en una nueva línea. 
Sin embargo, a diferencia de los elementos inline, puede ajustar el ancho y la altura de un elemento `inline-block`, 
al igual que lo haría con los elementos de nivel de bloque.

En resumen, la principal diferencia entre inline e `inline-block` es que los elementos inline 
no permiten controlar su tamaño, mientras que los elementos `inline-block` permiten un control total 
sobre las dimensiones sin dejar de estar alineados con el resto del contenido. 
Veamos un ejemplo.
```html
<head>
  <style>
    .inline-block-element {
      display: inline-block;
      width: 150px;
      height: 100px;
    }

    .element1 {
      background-color: lightblue;
    }

    .element2 {
      background-color: lightgreen;
    }
  </style>
</head>
<body>
  <div class="container">
    <span class="inline-block-element element1">Inline-Block</span>
    <span class="inline-block-element element2">Inline-Block</span>
  </div>
</body>
```
En el ejemplo anterior, tenemos un div con la clase container. 
Dentro de ese elemento div, tenemos dos elementos span. 
Cada uno de los elementos span tiene la propiedad `display:inline-block`
y también tiene un ancho y alto definidos. 
Los elementos `inline-block` aparecerán uno al lado del otro porque se comportan como elementos `inline`, 
pero también tienen un ancho y alto especificados, lo que les da propiedades de bloque.

Pero, si eliminas la propiedad `display:inline-block`, 
ni la altura ni el ancho se aplicarán aunque los hayas definido claramente.
---
Comprender cómo funciona el formato `inline-block` es útil porque 
permite crear diseños que requieren tanto alineación como control de dimensiones dentro 
de un flujo de texto continuo.