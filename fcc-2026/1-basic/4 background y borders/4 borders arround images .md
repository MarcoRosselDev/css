# ¿Cuáles son las diferentes maneras de agregar bordes a las imágenes?

En CSS, existen varias formas de agregar bordes a las imágenes, 
cada una con diferentes opciones de estilo y niveles de control. 
Exploremos algunos de los métodos más comunes y versátiles.
La forma más sencilla de añadir un borde a una imagen es mediante la propiedad `border`. 
Esta propiedad permite definir simultáneamente el ancho, el estilo y el color del borde.
```css
img {
  border: 2px solid red;
}
```
Esta regla CSS añade un borde rojo sólido de 2 píxeles de ancho alrededor de todos los elementos `<img>`. 
Puedes ajustar el ancho, el estilo (como punteado, discontinuo o doble) y el color según tus necesidades de diseño.
Si necesitas más control sobre cada lado del borde, 
puedes usar las propiedades específicas para cada lado.
```css
img {
  border-top: 10px solid red;
  border-right: 10px dashed green;
  border-bottom: 10px dotted blue;
  border-left: 10px double purple;
}
```
Esto permite crear estilos de borde únicos para cada lado de la imagen. 
Otra forma de crear un efecto de borde es mediante la propiedad `outline`. 
Si bien es similar a `border`, `outline` no afecta las dimensiones ni el diseño del elemento.
```css
img {
  outline: 3px solid gold;
}
```
Esto crea un contorno dorado alrededor de la imagen sin cambiar su tamaño ni posición. 
Si desea crear esquinas redondeadas en su borde, 
puede usar la propiedad border-radius junto con border:
```css
img {
  border: 2px solid black;
  border-radius: 10px;
}
```
Recuerda que estas técnicas se pueden combinar y personalizar para crear efectos de borde únicos. 
La elección del método depende de tus requisitos de diseño específicos y del nivel de complejidad que necesites.