# ¿Qué es un degradado de fondo y cómo funciona? 

En CSS, un degradado de fondo es una transición suave entre dos o más colores 
que se puede aplicar al fondo de un elemento. 
Los degradados permiten crear fondos visualmente atractivos sin necesidad de imágenes.
En CSS existen dos tipos principales de degradados: 
  degradados lineales y degradados radiales. 
---
## Degradado lineal
Un degradado lineal realiza una transición de colores a lo largo de una línea recta. 
Se puede definir la dirección y los colores involucrados. 
Esta es la sintaxis básica:
```js
background: linear-gradient(direction, color-stop1, color-stop2, ...);
```
En este ejemplo, utilizamos la propiedad CSS `background` con un valor de degradado lineal. 
La dirección especifica la dirección del degradado. 
Puede ser un ángulo (como 45 grados), una palabra clave (como a la derecha o abajo) o un lado/esquina.
color-stop especifica los colores y las posiciones donde se producen las transiciones de degradado. 
Para comprender mejor cómo funcionan los degradados lineales, 
veamos el siguiente ejemplo:
```css
.linear-gradient{
  background: linear-gradient(to right, red, yellow);
  height: 40vh;
}
```
Este CSS crea un degradado lineal que va del rojo a la izquierda al amarillo a la derecha. 
El degradado se aplica a un elemento con una altura del 40 % de la altura de la ventana gráfica. 
Aprenderás más sobre las unidades vh en una lección posterior. 
La dirección hacia la derecha indica que el degradado se extiende horizontalmente de izquierda a derecha.
---
## degradado radial
Otro tipo de degradado sería el degradado radial. 
Un degradado radial hace que los colores transicionen desde un origen (generalmente el centro) 
hacia afuera en forma circular o elíptica. 
Esta es la sintaxis básica:
```js
background: radial-gradient(shape size at position, color-stop1, color-stop2, ...)
```
En la sintaxis, `shape` especifica la forma del degradado, que puede ser un círculo o una elipse. 
`size` determina el tamaño de la forma final del degradado, 
que puede ser `closest-side`, `closest-corner`, `farthest-side` o `farthest-corner`. 
`position` determina la posición del centro del degradado, 
que puede especificarse mediante palabras clave (como `center`, `top left`, `bottom right`) 
o valores precisos (como `50% 50%`, `10px 20px`).
Por último, los puntos de color son una lista de colores por los que pasa el degradado. 
Cada punto de color puede incluir opcionalmente un valor de posición 
(porcentaje o longitud) que indica dónde debe colocarse el color. 
Un ejemplo sería:
```js
.radial-gradient{
  background: radial-gradient(circle closest-side at center, red, yellow 50%, green);
  height: 60vh;
}
```
Este CSS crea un degradado radial circular centrado en el elemento. 
Comienza con rojo en el centro, cambia a amarillo al 50% del radio y termina con verde. 
La palabra clave `closest-side` hace que la forma final del degradado se ajuste al lado más cercano del elemento. 
El degradado se aplica a un elemento con una altura del 60% de la altura de la ventana gráfica.
Saber cómo trabajar con degradados CSS puede mejorar significativamente tus diseños, 
ya que proporcionan fondos visualmente atractivos sin necesidad de imágenes. 
Con opciones como degradados lineales para transiciones suaves y degradados radiales para efectos circulares, 
ofrecen flexibilidad y creatividad en el diseño web.