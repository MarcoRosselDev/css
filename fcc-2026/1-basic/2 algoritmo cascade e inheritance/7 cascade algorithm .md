# ¿Cómo funciona el algoritmo de cascada a grandes rasgos? 

El algoritmo de cascada es el proceso que utiliza el navegador 
para decidir qué reglas CSS aplicar cuando hay varios estilos dirigidos al mismo elemento. 
Garantiza que se utilicen los estilos más apropiados, basándose en un conjunto de reglas bien definidas.
El proceso comienza con la relevancia. 
El navegador primero filtra todas las reglas CSS para encontrar 
aquellas que realmente se aplican al elemento en cuestión. 
Esto incluye la coincidencia de selectores y la consideración de las consultas de medios que puedan estar activas.
Una consulta de medios(media query) es una técnica CSS que se utiliza para aplicar estilos en función 
de las características del dispositivo o la ventana gráfica, como su ancho, alto u orientación.
A continuación, el algoritmo considera el origen y la importancia. 
Las hojas de estilo CSS pueden provenir de diferentes fuentes: 
los estilos predeterminados del navegador (agente de usuario), 
los estilos definidos por el usuario y los estilos escritos por el autor (usted). 
Tras considerar el origen, el algoritmo evalúa la importancia de cada regla, 
dando prioridad a las reglas marcadas con !important, 
que prevalecen sobre las demás independientemente de su origen.

Tras filtrar por origen e importancia, el algoritmo analiza la especificidad. 
Cuando se aplican dos reglas del mismo origen y nivel de importancia, 
se aplica la regla con mayor especificidad. 
La especificidad mide el grado de precisión de un selector, 
y los selectores más específicos tienen prioridad sobre los más generales.

Finalmente, si todo lo demás es igual, entra en juego el orden de aparición. 
Cuando dos reglas tienen la misma especificidad, se aplicará la que aparezca última en el CSS. 
Por eso, el orden en que escribes tus estilos a veces puede afectar el resultado. 
Veamos un ejemplo.
En el archivo HTML, hay un único elemento de párrafo. 
Luego, dentro del CSS, tenemos dos reglas, cada una dirigida al elemento de párrafo.
```html
<head>
  <style>
    p {
      color: blue;
    }
    p {
      color: green;
    }
  </style>
</head>
<body>
  <p>example paragraph</p>
</body>
```
La primera regla establece todos los elementos de párrafo en color azul, 
mientras que la segunda regla los establece en color verde. 
Entonces, ¿qué color se aplicará? 
Se aplicará el color verde a los elementos de párrafo. 
Al considerar la relevancia, el origen y la importancia, la especificidad y el orden de aparición, 
el algoritmo Cascade garantiza que su CSS se comporte de manera predecible, 
lo que le permite diseñar páginas web más complejas y con más matices.