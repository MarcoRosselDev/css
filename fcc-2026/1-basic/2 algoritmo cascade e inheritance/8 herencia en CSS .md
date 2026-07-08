# ¿Cómo funciona la herencia en CSS a grandes rasgos? 
La herencia es un concepto clave en CSS que determina cómo se transmiten 
los estilos de los elementos padre a sus elementos hijo. 
Al igual que en el mundo real, donde los hijos suelen heredar rasgos de sus padres, 
en CSS, ciertas propiedades pueden ser heredadas por los elementos hijo de sus elementos padre.
Esto permite una forma más eficiente de aplicar un estilo consistente en todo un documento. 
En CSS, no todas las propiedades se heredan por defecto. 
Por ejemplo, propiedades como color, font-family y line-height se heredan. 
Esto significa que si estableces el color del texto en un elemento padre, 
todos sus elementos hijos heredarán ese color a menos que lo anules específicamente.
Por ejemplo, considere el siguiente ejemplo donde un elemento div padre tiene su color establecido 
mediante un estilo en línea, y el elemento p hijo hereda ese color:
En este caso, tanto el div padre como el p hijo mostrarán su texto en azul porque el color se hereda. 
Por otro lado, propiedades como margin, padding, border y background no se heredan por defecto. 
Si desea que un elemento hijo herede estos estilos, debe configurarlos explícitamente, 
ya sea directamente en el elemento hijo o utilizando la palabra clave inherit.
---
## inherit
La palabra clave `inherit` se puede usar para forzar la herencia de una propiedad de un elemento padre, 
incluso si esa propiedad normalmente no se hereda. 
Por ejemplo, si desea que un elemento hijo específico tenga el mismo relleno que su padre, 
puede establecer `padding: inherit` en el elemento hijo:
```html
<div style="padding: 20px;">
  This is the parent element with padding.
  <p style="padding: inherit;">This is the child element inheriting the padding.</p>
</div>
```
En este caso, el elemento hijo `p` heredará el relleno de 20px de su elemento padre `div`. 
La herencia es especialmente útil para mantener la coherencia y reducir la redundancia en las hojas de estilo. 
En lugar de escribir la misma regla de estilo para varios elementos, 
se puede definir una sola vez en un elemento padre, y los elementos hijos la heredarán. 
Esto puede hacer que el CSS sea más conciso y fácil de gestionar.
Sin embargo, es importante recordar que la herencia solo funciona en una dirección, 
de padre a hijo. 
Si se modifica un estilo en un elemento hijo, esto no afectará al elemento padre.