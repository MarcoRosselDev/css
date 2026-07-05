# ¿Qué es CSS y cuál es su función en la web? 

CSS, siglas de Cascading Style Sheets (Hojas de Estilo en Cascada), 
es un componente fundamental del desarrollo web moderno. 
Es un lenguaje de hojas de estilo que se utiliza para aplicar estilos a HTML. 
En términos más sencillos, si HTML es la estructura de una página web, 
CSS es lo que le da una buena apariencia. 
Aquí tienes un ejemplo de cómo aplicar estilos a una barra de navegación.

NOTA: No te preocupes por entender el código CSS todavía. 
Aprenderás cómo funciona todo esto en lecciones y talleres futuros. 
Esto es solo para darte una idea de lo que puedes hacer con un poco de CSS.

```html
<link rel="stylesheet" href="styles.css" />

<nav class="navbar">
    <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</nav>
```
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', sans-serif;
  background-color: #f4f4f4;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #333;
  padding: 1rem 2rem;
  color: white;
}

.navbar .logo {
  font-size: 1.5rem;
  font-weight: bold;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}

.nav-links a {
  color: white;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #ff9800;
}
```
La función principal de CSS es separar el contenido de una página web de su presentación visual. 
Esta separación permite a los desarrolladores web crear sitios web más flexibles y fáciles de mantener. 
Con CSS, puedes controlar el diseño, los colores, las fuentes 
y la apariencia visual general de las páginas web sin alterar la estructura HTML.

Consideremos una analogía sencilla. 
Si imaginamos un sitio web como una casa, HTML sería la base y la estructura, 
mientras que CSS sería la pintura, el papel tapiz y la decoración que le dan un aspecto atractivo y único. 

CSS funciona seleccionando elementos HTML y aplicándoles estilos. 
Aquí vemos un ejemplo con un botón sin estilo y otro con estilo. 
Para interactuar con este ejemplo, deberá habilitar el editor interactivo.

```css
.round-btn {
  font-size: 1rem;
  font-family: 'Segoe UI', sans-serif;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.2s ease;
  background-color: #2ecc71;
  color: white;
  border-radius: 50px;
  padding: 0.6rem 1.6rem;
}
.round-btn:hover {
  background-color: #27ae60;
  transform: translateY(-2px);
}
```
Estos estilos pueden incluir propiedades como el color, el tamaño de la fuente y muchas más. 
Al modificar estas propiedades, puedes alterar drásticamente la apariencia 
de una página web sin cambiar su contenido. 
Uno de los aspectos más potentes de CSS es su capacidad para crear diseños adaptables. 
Esto significa que, con CSS, puedes lograr que tu sitio web se vea genial en cualquier dispositivo, 
ya sea una computadora de escritorio, una tableta o un teléfono inteligente.

CSS permite ajustar el diseño, el tamaño de la fuente y otros elementos visuales 
según el tamaño de la pantalla del dispositivo que visualiza el sitio web. 

#

Otra característica importante de CSS es su naturaleza en cascada, 
de ahí el término "cascada" en su nombre. 
Esto significa que los estilos se pueden heredar y sobrescribir, 
lo que permite una estructura jerárquica de estilos. 
Aprenderás más sobre cómo funciona esto en lecciones futuras. 
CSS también admite el uso de hojas de estilo externas.

Esto significa que puedes mantener todas tus reglas de estilo en un archivo separado, 
que luego puedes vincular a varias páginas HTML. 
Esta función mejora enormemente la facilidad de mantenimiento de los sitios web, 
especialmente los más grandes. 
En lugar de tener que cambiar los estilos en cada página individual, 
puedes realizar cambios en un único archivo CSS que afectará a todas las páginas vinculadas. 
En el mundo del desarrollo web, CSS desempeña un papel fundamental en la creación de sitios web 
visualmente atractivos, responsivos y fáciles de usar.

Permite a los desarrolladores transformar documentos HTML sencillos en experiencias 
web atractivas que captan la atención de los usuarios y mejoran su interacción con el contenido web.