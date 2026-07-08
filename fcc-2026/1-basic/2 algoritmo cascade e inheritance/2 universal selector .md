# ¿Qué es el selector universal y cuál es su especificidad? 

El selector universal (*) es un tipo especial de selector CSS que coincide con cualquier elemento del documento. Se suele utilizar para aplicar un estilo a todos los elementos de la página, lo que puede ser útil para restablecer o normalizar estilos en diferentes navegadores.
El selector universal se puede utilizar para seleccionar todos los elementos dentro de un contexto específico o globalmente en todo el documento. Aquí hay un ejemplo de cómo usar el selector universal para establecer el margen y el relleno para todo el documento HTML.
```html
<head>
  <style>
    * {
      margin: 0;
      padding: 0;
    }
  </style>
</head>
<body>
  <h1>Heading element</h1>
  <p>example paragraph element</p>
</body>
```
En este ejemplo de código, el selector * restablece el margen y el relleno de todos los elementos a cero, 
que es una técnica común utilizada en los restablecimientos de CSS. 
El selector universal tiene el valor de especificidad más bajo de cualquier selector. 
Contribuye con 0 a todas las partes del valor de especificidad (0, 0, 0, 0).
Esto significa que cualquier otro selector, incluidos los selectores de tipo, 
de clase, de ID y los estilos en línea, anulará los estilos establecidos por el selector universal. 
Veamos el siguiente ejemplo de HTML y CSS:
```html
<head>
  <style>
    * {
      color: blue;
    }
    p {
      color: red;
    }
    .highlight {
      color: green;
    }
    #unique {
      color: purple;
    }
  </style>
</head>
<body>
  <p id="unique" class="highlight">This text has multiple styles applied.</p>
</body>
```
El selector universal * establece el color del texto en azul para todos los elementos. Sin embargo, el selector de tipo p anula esta configuración estableciendo el color del texto en rojo específicamente para los elementos p.
Si un elemento tiene la clase highlight, el selector de clase tiene prioridad, cambiando el color del texto a verde. Finalmente, el selector de ID #unique, que tiene la mayor especificidad, anulará a todos los demás, estableciendo el color del texto a morado.