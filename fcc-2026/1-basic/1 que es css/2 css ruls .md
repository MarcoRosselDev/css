# ¿Cuál es la anatomía básica de una regla CSS? 

CSS es responsable de los estilos de una página web. 
Todos estos estilos se componen de varias reglas CSS. 
Una regla CSS se compone de dos partes principales: 
un selector y un bloque de declaración. 
Veamos la sintaxis básica.
```css
selector {
  property: value;
}
```
Un selector es un patrón utilizado en CSS para identificar y aplicar estilos a elementos HTML específicos. 
Algunos ejemplos de selectores son los de tipo(type), clase(class) e ID. 
Las llaves que aparecen en la sintaxis básica se conocen como bloque de declaración. 
Un bloque de declaración aplica un conjunto de estilos a uno o varios selectores.

Dentro del bloque de declaración, encontrará una serie de declaraciones. 
Cada declaración consta de una propiedad y un valor. 
La propiedad es el identificador CSS que especifica qué elemento se está estilizando. 
Un ejemplo de propiedad sería la propiedad `background-color`. 
El valor sería la configuración específica aplicada a esa propiedad. Por ejemplo, 
si la propiedad es `background-color`, un valor podría ser `purple`, 
que establece el color de fondo en morado.

Después de cada nombre de propiedad, debes colocar dos puntos, 
y después de cada valor, un punto y coma. 
Ahora que conoces la sintaxis de una regla CSS, veamos un ejemplo. 
Habilita el editor interactivo y haz clic en la pestaña styles.
css para ver el código CSS.
```css
p {
  color: blue;
}
```
En esta regla CSS, un selector de tipo apunta a todos los elementos de párrafo en la página. 
Dentro del bloque de declaración, hay una declaración. 
La declaración consiste en la propiedad color con un valor establecido en azul. 
Esto cambiará el color del texto de todos los elementos de párrafo a azul. 
Si desea aplicar el mismo conjunto de estilos a varios selectores, 
puede crear una lista de selectores con cada selector separado por una coma.

Aquí tienes un ejemplo de cómo aplicar estilos a varios selectores 
(para interactuar con el ejemplo, habilita el editor interactivo):

```css
#title,
.subheading {
  color: navy;
}
```
En esta lista de selectores, hay un selector de ID que apunta al elemento HTML con el ID "title". 
Todos los selectores de ID deben comenzar con el símbolo de almohadilla (#). 
A continuación, hay una coma seguida de un selector de clase que apunta a todos los elementos HTML 
con el valor de clase "subheading". 
Todos los selectores de clase deben comenzar con un punto. 
Toda la lista de selectores recibirá el mismo estilo, 
con el color del texto establecido en azul marino.