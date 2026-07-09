# ¿Cómo se personalizan los diferentes estados de un enlace? 

Un enlace puede tener diferentes estados, como enlace, visitado, al pasar el cursor, enfocado y activo. 
Estos estados son importantes para ayudar a los usuarios a reconocer los enlaces 
y proporcionarles información clara después de interactuar con ellos, 
lo que mejora tanto la usabilidad como la accesibilidad.
Dar estilo a los diferentes estados de los enlaces es crucial para la usabilidad 
y la accesibilidad, ya que proporciona señales visuales sobre el estado actual del enlace. 
Esto ayuda a los usuarios a comprender qué enlaces han visitado, 
con cuál están interactuando y qué sucederá al hacer clic. 
Para los usuarios con discapacidades visuales o cognitivas, 
estos estilos distintos pueden hacer que la navegación sea mucho más fácil e intuitiva.
Además, los estados claros de los enlaces mejoran la experiencia general del usuario al proporcionar
retroalimentación inmediata sobre sus interacciones, lo que reduce la confusión y mejora la navegabilidad del sitio.
Estos estados se pueden personalizar mediante `pseudo-class` en CSS. 
Una `pseudo-class` es una palabra clave que se agrega a un selector para especificar un estado especial 
del elemento seleccionado.
Por ejemplo, `:hover` puede cambiar el color de un botón cuando el puntero del usuario se sitúa sobre él, 
mientras que `:visited` puede cambiar el color de un enlace que ya ha sido visitado. 
Las `pseudo-class` permiten aplicar estilos a los elementos en función de su estado 
o de la interacción del usuario con ellos, sin necesidad de añadir código HTML adicional. 
La sintaxis de una `pseudo-class` es similar a esta, donde `A` es el selector y `:B` es la pseudoclase:
```css
A:B {
  property: value;
}
```
Para comprender mejor cómo aplicar estilos a los diferentes estados de los enlaces, 
veamos algunos ejemplos. 
La pseudoclase `:link` aplica estilos a los enlaces no visitados, indicando que se puede hacer clic en ellos. 
Aquí hay un ejemplo de cómo seleccionar un elemento de anclaje y usar la pseudoclase `:link`.
```css
/* Normal state (unvisited link) */
a:link { 
  color: red;
}
```
El ejemplo anterior cambiará el color azul predeterminado del enlace a rojo cuando no se haya visitado. 
`:visited` aplica estilos a los enlaces que ya se han visitado o en los que se ha hecho clic, 
lo que ayuda a los usuarios a saber en qué enlaces han hecho clic anteriormente. 
Aquí hay un ejemplo de uso de la pseudoclase `:visited`.
```css
a:visited {
  color: green;
}
```
Este código coloreará el enlace de verde cuando se haga clic en él. 
:hover cambia el estilo del enlace cuando el usuario pasa el cursor sobre él, 
proporcionando una señal visual de que el enlace es interactivo. 
Aquí hay un ejemplo de uso de la pseudoclase :hover:
```css
/* Hover state */
a:hover {
  color: green;
}
```
Este código coloreará los enlaces de verde al pasar el ratón por encima. 
El atributo `:focus` añade estilos alrededor del enlace cuando está enfocado, 
por ejemplo, al navegar con el teclado o para mejorar la accesibilidad. 
Aquí tienes un ejemplo que utiliza la propiedad `outline` para aplicar un contorno naranja sólido 
cuando el enlace está enfocado.
```css
/* Focus state */
a:focus {
  outline: 2px solid orange;
}
```
`active` cambia los estilos del enlace mientras se hace clic en él, 
proporcionando al usuario información inmediata sobre el registro de su acción. 
Aquí hay un ejemplo de uso de la pseudoclase `:active`.
```css
/* Active state */
a:active {
  color: pink;
}
```
Este ejemplo de código hará que el enlace cambie a color rosa inmediatamente al hacer clic en él.