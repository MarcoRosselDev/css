# ¿Qué es la especificidad de los selectores de ID? 

Los selectores de ID se encuentran entre los selectores más potentes de CSS, 
ya que permiten a los desarrolladores aplicar estilos a elementos específicos con identificadores únicos. 
Esto los hace muy eficaces para seleccionar elementos individuales que requieren un estilo único.
Los selectores de ID se definen mediante el símbolo de almohadilla (#) seguido del nombre del ID. 
Deben ser únicos dentro de un documento HTML, es decir, dos elementos no deben compartir el mismo ID. 
Aquí hay un ejemplo que utiliza un selector de ID:
```html
<head>
  <style>
    #unique {
      color: purple;
    }
  </style>
</head>
<body>
  <p id="unique">Example paragraph</p>
  <p>Another paragraph</p>
  <p>Yet another paragraph</p>
</body>
```
En este ejemplo, el elemento con el ID único tendrá su color de texto establecido en morado. 
Los selectores de ID tienen una especificidad muy alta, mayor que la de los selectores de tipo y de clase, 
pero menor que la de los estilos en línea. 
El valor de especificidad para un selector de ID es (0, 1, 0, 0). 
Esto significa que los selectores de ID pueden anular los selectores de clase y de tipo, 
pero pueden ser anulados por los estilos en línea.