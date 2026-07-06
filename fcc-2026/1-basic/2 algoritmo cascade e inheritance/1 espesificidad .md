# ¿Qué es la especificidad de CSS y cuál es la especificidad para CSS en línea, interno y externo? 

La especificidad de CSS es un concepto fundamental que determina 
qué estilos se aplican a un elemento cuando podrían aplicarse varias reglas. 

Comprender la especificidad ayuda a los desarrolladores a resolver conflictos 
entre diferentes reglas CSS y garantiza que los estilos deseados se apliquen de forma coherente.

La especificidad de CSS se calcula en función del tipo de selectores utilizados. 
La mayor especificidad se atribuye a los estilos en línea, 
que se aplican directamente a un elemento mediante el atributo `style`. 
En este ejemplo, el primer párrafo será rojo, mientras que los demás elementos `<p>` serán azules. 
Esto se debe a que los estilos en línea tienen una mayor especificidad que los selectores de tipo, 
como el selector `<p>` que se muestra en el archivo `styles.css`.
```html
<head>
  <style>
    p {
      color: blue;
    }
  </style>
</head>
<body>
  <p style="color: red;">Red paragraph</p>
  <p>Other paragraph</p>
  <p>Another paragraph</p>
  <p>Yet another paragraph</p>
</body>
```
siguiendo esto, Los selectores ID tienen un nivel alto de especificidad.
```html
<head>
  <style>
    #para {
      color: red; 
    }

    p {
      color: blue;
    }
  </style>
</head>
<body>
  <p id="para">Red paragraph</p>
  <p>Other paragraph</p>
  <p>Another paragraph</p>
  <p>Yet another paragraph</p>
</body>
```
A continuación, entran en juego los selectores de clase, 
los selectores de atributo y las pseudoclases. 
Algunos ejemplos son los selectores de clase como .container y .button, 
los selectores de atributo como [type="text"] y las pseudoclases como :hover. 
Estos tienen un nivel moderado de especificidad. 
NOTA: Aprenderás más sobre las pseudoclases en lecciones futuras.

En este ejemplo, el primer párrafo será rojo porque un selector de ID 
tiene mayor especificidad que los selectores de clase y tipo. 
Los elementos .example-para serán de color verde, mientras que los demás elementos 
de párrafo serán de color azul.
```html
<head>
  <style>
  #para {
    color: red; 
  }

  .example-para {
    color: green;
  }

  p {
    color: blue;
  }
  </style>
</head>
<body>
  <p id="para">Example paragraph</p>
  <p class="example-para">Other paragraph</p>
  <p class="example-para">Another paragraph</p>
  <p>Yet another paragraph</p>
</body>
```
Los selectores de tipo, como div y h1, y los pseudoelementos como ::before y ::after, 
tienen una especificidad menor en comparación con los grupos anteriores. 
NOTA: Aprenderás más sobre los pseudoelementos en lecciones futuras.

Finalmente, el selector universal, representado por un asterisco *, 
tiene la especificidad más baja de todos. 
Aquí hay un ejemplo de cómo establecer el color de todos los elementos a rojo usando el selector *. 
Sin embargo, no verá ningún elemento rojo porque hay selectores de ID y tipo que anulan esos estilos, 
lo que resalta la baja especificidad del selector *.
---
Los valores de especificidad se calculan como un valor de cuatro partes (a, b, c, d): 
* a: Estilos en línea (1 o 0). 
* b: Número de selectores de ID. 
* c: Número de selectores de clase, selectores de atributo y pseudoclases. 
* d: Número de selectores de tipo, pseudoelementos y selectores universales.
Cada parte del valor de especificidad tiene un peso diferente.
---
* Los estilos en línea (a) tienen el mayor peso, aportando un valor de 1 a la primera parte del valor de especificidad.

* Los selectores de ID (b) tienen el siguiente mayor peso, aportando cada ID 1 a la segunda parte del valor de especificidad.

* Los selectores de clase, los selectores de atributo y las pseudoclases (c) tienen un peso moderado, aportando cada uno 1 a la tercera parte del valor de especificidad.

* Los selectores de tipo y los pseudoelementos (d) tienen el menor peso, contribuyendo cada uno con 1 a la cuarta parte del valor de especificidad. 

* Selector universal (*): El selector universal contribuye con 0 al cálculo de la especificidad y no la afecta. Su inclusión en un selector no cambia el valor de especificidad.

El CSS en línea tiene la mayor especificidad porque se aplica directamente al elemento. Sobrescribe cualquier CSS interno o externo. El valor de especificidad para los estilos en línea es (1, 0, 0, 0). Aquí hay otro ejemplo de un estilo en línea:
```html
<p style="color: red;">This text is red.</p>
```
El CSS interno se define dentro de un elemento `style` en la sección `<head>` del documento HTML. 
Tiene menor especificidad que los estilos en línea. 
Tanto el CSS interno como el externo comparten el mismo nivel de especificidad; 
esta viene determinada por los selectores utilizados, no por la ubicación de la definición del CSS. 
Cuando dos reglas tienen la misma especificidad, prevalece la que aparece más adelante en el documento. 
Por lo tanto, si una hoja de estilos externa se enlaza después de un bloque de estilos interno, 
las reglas externas tienen prioridad.
Si ya existe un enlace previo, prevalecen las reglas internas. 
El valor de especificidad para los estilos internos viene determinado por los selectores utilizados. 
Por ejemplo, un selector de ID dentro de CSS interno tiene un valor de especificidad de (0, 1, 0, 0).

```html
<head>
  <style>
    #text {
      color: blue;
    }
  </style>
</head>
<body>
  <div id="text">This text is blue.</div>
</body>
```
En este ejemplo, el texto será azul a menos que se aplique un estilo en línea o un selector más específico. 
El CSS externo se enlaza mediante un elemento de enlace en la sección head 
y se escribe en archivos .css separados. 
Al igual que el CSS interno, la especificidad de los estilos externos está determinada por los selectores utilizados.
El CSS externo proporciona la mejor mantenibilidad para proyectos grandes. 
El valor de especificidad para los estilos externos también está determinado por los selectores utilizados. 
Por ejemplo, un selector de clase dentro del CSS externo tiene un valor de especificidad de (0, 0, 1, 0).
---
En este ejemplo, el color del texto se define en el archivo styles.css 
y se aplicará a menos que se anule mediante un selector más específico o un estilo en línea.