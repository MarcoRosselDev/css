# ¿Cómo funcionan el ancho y la altura? 

En CSS, las propiedades de ancho y altura se utilizan para controlar las dimensiones 
de los elementos en una página web. 
Estas propiedades se pueden definir en diferentes unidades, 
como píxeles (px), porcentajes (%), unidades de ventana gráfica "viewport units" (vw, vh), y más.
---
## width (ancho)
La propiedad width especifica el ancho de un elemento. 
Si no se especifica un ancho, el valor predeterminado es auto. 
Esto permite que el navegador determine el ancho del elemento en función de su contenido, 
su elemento padre y su tipo de visualización. 
Para un elemento div, `width: auto` hace que se expanda para llenar todo el ancho de su contenedor padre. 
---
## height (alto)
La propiedad height especifica la altura de un elemento. 
De manera similar, la altura es auto por defecto, lo que significa que se ajustará al contenido interno. 
Aquí hay un ejemplo usando width y height:
```html
<head>
  <style>
    .box {
      width: 100px;
      height: 100px;
      background-color: skyblue
    }
  </style>
</head>
<body>
  <div class="box"></div>
</body>
```
En este ejemplo, tenemos un elemento div con la clase box. 
Este elemento ocupará 100 píxeles de alto y ancho, mientras que el color de fondo será azul cielo. 

Los `píxeles` son una unidad de medida de tamaño fijo en CSS, 
lo que proporciona un control preciso sobre las dimensiones.
---
## min-(width-height)
La propiedad `min-width` especifica el ancho mínimo que puede tener un elemento. 
Aunque el contenido sea menor, el elemento no se reducirá por debajo de este valor.

La `min-height` especifica la altura mínima que puede tener un elemento. Garantiza que el elemento no sea más corto que el valor establecido. 
Aquí hay un ejemplo:
```html
<head>
  <style>
    .box {
      width: 50px;
      min-width: 100px;
      height: 50px;
      min-height: 100px;
      background-color: lightcoral;
    }
  </style>
</head>
<body>
  <div class="box"></div>
</body>
```
El ejemplo anterior muestra cómo funcionan `min-width` y `min-height`. 
Aunque el cuadro tenga un ancho y alto de 50 píxeles, en realidad medirá 100 x 100 píxeles. 
Esto se debe a que `min-width` y `min-heigh` están configurados en 100 píxeles, 
valores mayores que el ancho y alto especificados.

Recuerda que si `min-width`o `min-height` son mayores que `width` o `height`, 
estos últimos prevalecerán sobre los valores menores. 
Esto garantiza que los elementos no se reduzcan demasiado, 
lo cual es importante para mantener un diseño coherente y funcional.
---
## max-(height-width)
max-width especifica el ancho máximo que puede alcanzar un elemento, 
incluso si hay espacio suficiente para que sea más ancho. 
`max-height` especifica la altura máxima que puede alcanzar un elemento, 
independientemente del tamaño del contenido.

Aqui un ejemplo:
```html
<head>
  <style>
    .box {
      width: 200px;
      max-width: 150px;
      height: 200px;
      max-height: 150px;
      background-color: lightgreen;
    }
  </style>
</head>
<body>
  <div class="box"></div>
</body>
```
El ejemplo anterior demuestra cómo `max-width` y `max-height` tienen prioridad sobre `width` y `height`. 
Aunque el cuadro esté configurado a 200 x 200 píxeles, en realidad medirá 150 x 150 píxeles. 
Esto se debe a que `max-width` y `max-height` están configurados a 150 píxeles, un valor menor. 

Recuerda que cuando `max-width` o `max-height` son menores que `width` o `height`, estos últimos tienen prioridad.
Esto es importante para controlar el tamaño máximo de los elementos en tus diseños.

CSS prioriza `min-width` y `min-height` sobre `width` y `max-height`.
`max-width` y `max-height` restringen las dimensiones si los valores superan sus límites. 
Por ejemplo, si se establece `width` en 600 px y `max-width` en 500 px, el elemento se limitará a 500 px de ancho.
`max-width` anula la configuración anterior, manteniendo el elemento dentro del tamaño máximo especificado. 
Esto garantiza que los elementos se mantengan dentro de los rangos de tamaño deseados, 
independientemente de los valores estándar de ancho y alto.