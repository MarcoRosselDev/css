# ¿Cuál es la especificidad de los selectores de tipo? 

Los selectores de tipo, también conocidos como selectores de elementos, se dirigen a elementos en función de su nombre de etiqueta. Estos selectores son fundamentales en CSS y permiten aplicar estilos a todas las instancias de un elemento HTML específico.
Los selectores de tipo son fáciles de usar y se escriben simplemente como el nombre de la etiqueta del elemento al que se desea aplicar estilo. Aquí hay un ejemplo de un selector de tipo que se aplica a todos los elementos de párrafo de la página:
```html
<head>
  <style>
    p {
      color: blue;
    }
  </style>
</head>
<body>
  <p>Paragraph one</p>
  <p>Paragraph two</p>
  <p>Paragraph three</p>
</body>
```
En este ejemplo, todos los elementos p tendrán su color de texto establecido en azul. 
Los selectores de tipo tienen una especificidad relativamente baja en comparación con otros selectores. 
El valor de especificidad para un selector de tipo es (0, 0, 0, 1).
Esto significa que los selectores de tipo serán anulados por los selectores de clase, 
los selectores de ID y los estilos en línea, 
pero aún se pueden aplicar estilos a menos que existan reglas de mayor especificidad. 
Veamos un ejemplo donde los selectores de clase anularán los estilos del selector de tipo. 
Aquí hay un ejemplo con dos elementos de párrafo:
```html
<p class="para">I am a paragraph</p>
<p class="para">Here is another paragraph</p>
```
Ambos elementos de párrafo tienen una clase llamada para. 
Dentro del archivo CSS, el selector de tipo apunta a los párrafos 
y el selector de clase apunta a los elementos con la clase para.
```css
p {
  color: blue;
}

.para {
  color: red;
}
```
Todos los párrafos de la página con la clase "para" tendrán el color del texto establecido en rojo 
en lugar de azul porque los selectores de clase tienen una especificidad mayor que los selectores de tipo.