# ¿Cómo funcionan el tamaño, la repetición, la posición y la fijación de las imágenes de fondo? Al trabajar con imágenes de fondo en CSS, dispones de varias propiedades para controlar cómo se muestran. Las principales propiedades en las que nos centraremos son background-size, background-repeat, background-position y background-attachment.
Primero, echemos un vistazo a la propiedad background-imag
```html
<style>
  body {
    background-image: url("https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg");
  }
</style>
```
El CSS anterior establece una imagen de fondo de un gato para el elemento body. Si deseas establecer el tamaño de la imagen de fondo, puedes usar la propiedad background-size. Puedes usar contain para escalar la imagen al tamaño máximo posible sin recortarla ni estirarla. Aquí tienes un ejemplo con background-size: contain:
```html
<style>
  body {
    background-image: url("https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg");
    background-size: contain;
    min-height: 100px;
  }
</style>
```
Estamos estableciendo la altura mínima en 100 px para que la imagen de fondo sea visible y el diseño mantenga una altura base, asegurando que incluso con contenido mínimo, el diseño se vea equilibrado y visualmente atractivo. Si cambiamos la propiedad background-size para usar el valor cover, la imagen de fondo se escalará para cubrir todo el elemento body manteniendo su proporción de aspecto.
```html
<style>
  body {
    background-image: url("https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg");
    background-size: cover;
    min-height: 100px;
  }
</style>
```
En los ejemplos anteriores, probablemente notaste que la imagen de fondo se repetía continuamente. Por defecto, las imágenes de fondo se repiten tanto horizontal como verticalmente para cubrir todo el elemento. Sin embargo, puedes controlar este comportamiento. Puedes usar la propiedad `background-repeat` con el valor `no-repeat`.
```html
<style>
  body {
    background-image: url("https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg");
    background-size: contain;
    background-repeat: no-repeat;
    min-height: 100px;
  }
</style>
```
Si estableces background-size en contain y background-repeat en no-repeat, la imagen ya no se repetirá en la pantalla. Si deseas que la imagen de fondo se repita horizontalmente, puedes usar el valor repeat-x para la propiedad background-repeat.
```html
<style>
  body {
    background-image: url("https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg");
    background-size: contain;
    background-repeat: repeat-x;
    min-height: 100px;
  }
</style>
```
Si desea repetir la imagen de fondo verticalmente, puede usar el valor repeat-y para la propiedad background-repeat.
```html
<style>
  body {
    background-image: url("https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg");
    background-size: contain;
    background-repeat: repeat-y;
    min-height: 100px;
  }
</style>
```
Para posicionar una imagen de fondo en la pantalla, puede usar la propiedad `background-position`. Esta propiedad le permite definir la posición de la imagen de fondo dentro del elemento. Puede usar palabras clave como `top`, `bottom`, `left`, `right` y `center`, o valores específicos en píxeles o porcentajes. A continuación, se muestra un ejemplo con `center` y `top` para la propiedad `background-position`:
```html
<style>
  body {
    background-image: url("https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg");
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center top;
    min-height: 100px;
  }
</style>
```
Este código CSS centra la imagen de fondo horizontalmente y la coloca en la parte superior verticalmente. Por último, `background-attachment` determina si la imagen de fondo se desplaza con el contenido o permanece fija al desplazarse la página. Los valores principales son `scroll` (predeterminado), donde la imagen de fondo se desplaza con el contenido, y `fixed`, donde la imagen de fondo permanece en la misma posición en la pantalla.
Aquí hay un ejemplo que utiliza el valor fijo para la propiedad background-attachment:
```html
<style>
  body {
    background-image: url("https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg");
    background-position: center top;
    background-attachment: fixed;
  }
</style>
```
Este código CSS hace que la imagen de fondo permanezca fija incluso al desplazarse por la página. Si desea combinar varias propiedades en una sola línea, puede hacerlo utilizando la propiedad abreviada `background`. Aquí tiene un ejemplo:
```html
<style>
  body {
    background: center top fixed
      url("https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg");
  }
</style>
```
El ejemplo anterior combina background-image, background-position y background-attachment en una sola línea. Al dominar estas propiedades, tendrás un gran control sobre cómo se muestran las imágenes de fondo en tus diseños web, lo que te permitirá crear diseños más atractivos y funcionales.