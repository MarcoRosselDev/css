# ¿Qué son el CSS en línea, interno y externo, y cuándo usar cada uno? 

El CSS se puede aplicar a una página web de tres maneras principales: 
en línea, interno o externo. 
Cada método tiene su propio caso de uso, ventajas y limitaciones, 
y saber cuándo usar cada uno es esencial para escribir código limpio, 
eficiente y fácil de mantener. 
Analicemos los tres tipos de CSS y cuándo usarlos.
---
## CSS en línea (Inline CSS)
El CSS en línea se escribe directamente dentro de un elemento HTML utilizando el atributo `style`. 
Aplica estilos a un elemento específico. 
Aquí tienes un ejemplo de uso de CSS en línea:
```html
<p style="color: green;">This is an inline-styled paragraph.</p>
```
En este ejemplo, usamos el atributo `style` para establecer el texto del párrafo en verde. 
El CSS en línea se usa generalmente para estilos rápidos y puntuales o para anular 
otros estilos para un elemento específico. 
Sin embargo, debe evitarse en la mayoría de los casos, 
ya que puede saturar el HTML y dificultar el mantenimiento del código. 
Casi siempre, es mejor usar CSS interno o externo para mantener los estilos organizados y fáciles de mantener.
---
## CSS interno (Internal CSS)
El CSS interno se escribe dentro de las etiquetas style <style> en la sección <head> de un documento HTML. 
Aplica estilos a toda la página y es útil cuando se necesita dar estilo a un solo documento.  
Aquí tienes un ejemplo de CSS interno:
```html
<head>
  <style>
    p {
      color: blue;
    }
  </style>
</head>
<body>
  <p>This paragraph is styled using internal CSS.</p>
</body>
```
En el ejemplo anterior, el CSS interno aplica texto azul a todos los elementos `<p>` de la página. 
El CSS interno se utiliza mejor cuando se necesitan aplicar estilos a una página específica, 
en lugar de a varias páginas. 
Es útil para sitios web de una sola página o cuando los estilos no necesitan reutilizarse en otros lugares.
Sin embargo, tiene algunas desventajas, como no fomentar la reutilización en varias páginas. 
Además, al igual que el CSS en línea, mezcla HTML y CSS, 
lo que dificulta el mantenimiento del código en proyectos grandes.
---
## CSS externo (External CSS)
El CSS externo se escribe en un archivo .css independiente 
y se enlaza al documento HTML mediante el elemento `link` en la sección `<head>`. 
Permite aplicar estilos a varias páginas de forma coherente y es el método preferido 
en el desarrollo web profesional. 
Aquí tienes un ejemplo de cómo aplicar estilos a todos los elementos de párrafo:
```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <p>This paragraph is styled using external CSS.</p>
</body>
```
En una lección anterior, aprendiste que el elemento `link` tiene un atributo `rel` que especifica 
la relación entre el documento actual y el recurso enlazado, 
como por ejemplo, un enlace a una hoja de estilos o un recurso externo. 
Por otro lado, el atributo `href` especifica la URL del recurso enlazado, 
indicando desde dónde se debe obtener dicho recurso. 
El CSS externo es ideal para proyectos grandes donde se desea mantener un estilo coherente en varias páginas.

Promueve la separación de responsabilidades al permitir que HTML gestione la estructura y CSS el estilo, 
lo que hace que el código sea más mantenible y escalable. 
Comprender cuándo usar cada tipo de CSS es crucial para un desarrollo web eficiente y efectivo. 
En la mayoría de los casos, el CSS externo debería ser la opción preferida, 
especialmente para proyectos más grandes y complejos.