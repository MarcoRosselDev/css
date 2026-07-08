# ¿Cómo espaciar los elementos de una lista usando márgenes o interlineado? 

Los márgenes y el interlineado son esenciales para espaciar los elementos de una lista 
y mejorar la legibilidad y el atractivo visual. 
¡Primero, veamos cómo espaciar los elementos usando márgenes! 
Los márgenes se pueden usar para crear espacio entre los elementos de una lista 
aplicando propiedades de margen a los elementos `<li>`. 
Este método permite controlar el espacio fuera de cada elemento de la lista, 
aumentando o disminuyendo así el espacio entre ellos.
Veamos un ejemplo de una lista desordenada con tres elementos.
```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```
Por defecto, HTML no aplica mucho espacio entre los elementos de la lista. 
Para aplicar algo de espacio en la parte inferior de cada elemento de la lista, 
puede usar la propiedad margin-bottom de esta manera:
```css
li {
  margin-bottom: 40px;
}
```
En este ejemplo, se aplicará un margen de 40 px en la parte inferior de cada elemento de la lista desordenada. 
Otra forma de espaciar los elementos de la lista sería usar la propiedad line-height. 
La propiedad line-height ajusta el espaciado vertical entre las líneas de texto 
dentro de un mismo elemento de la lista.
Si bien afecta principalmente al espaciado entre líneas de texto dentro de cada elemento, 
también puede influir indirectamente en el espaciado general entre los elementos de la lista 
si estos contienen una sola línea de texto. 
Si los elementos de la lista tienen varias líneas de texto, 
la altura de línea afectará al espaciado entre ellas, 
pero no ajustará directamente el espaciado entre los elementos individuales de la lista. 
Para controlar el espaciado entre elementos individuales de la lista, 
se deben usar las propiedades de margen o relleno.
Utilizando la misma lista desordenada anterior, 
aquí hay un ejemplo de cómo aplicar altura de línea a los elementos de la lista.
```html
<head>
  <style>
    li {
      line-height: 2;
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
En este ejemplo, line-height: 2; establece la altura de línea al doble del tamaño de la fuente, 
creando más espacio vertical dentro de cada elemento de la lista.