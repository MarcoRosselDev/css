# ¿Cuál es la especificidad de los selectores de clase? 

Los selectores de clase son una parte fundamental de CSS, 
ya que permiten a los desarrolladores seleccionar varios elementos con el mismo atributo 
de clase y aplicarles un estilo coherente. 
Esto los hace muy versátiles y eficientes para aplicar estilos en todo un sitio web.
Los selectores de clase se definen mediante un punto (.) 
seguido del nombre de la clase. 
Se pueden aplicar a cualquier elemento del documento HTML. 
Aquí hay un ejemplo que utiliza un selector de clase:
```html
<head>
  <style>
    .highlight {
      color: green;
    }
  </style>
</head>
<body>
  <p class="highlight">Example paragraph</p>
</body>
```
En este ejemplo, cualquier elemento con la clase highlight tendrá su color de texto establecido en verde. 
Los selectores de clase tienen una especificidad mayor que los selectores de tipo, 
pero menor que los selectores de ID y los estilos en línea. 
El valor de especificidad para un selector de clase es (0, 0, 1, 0). 
Esto significa que los selectores de clase pueden anular a los selectores de tipo, 
pero pueden ser anulados por los selectores de ID y los estilos en línea.

Los selectores de clase se pueden combinar con otros selectores para crear reglas más específicas. 
Aquí hay un ejemplo que combina un selector de tipo de párrafo con un selector de clase:
```html
<head>
  <style>
    p.bold-text {
      font-weight: bold;
    }
  </style>
</head>
<body>
  <p class="bold-text">Example paragraph</p>
  <p class="bold-text">Example paragraph</p>
  <p>Another paragraph</p>
  <p>Yet another paragraph</p>
</body>
```
Esta regla se aplica solo a los elementos p que también tienen la clase bold-text, 
lo que hace que su texto sea negrita.