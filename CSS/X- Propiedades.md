# Propiedades - 6ª parte

## Sombras

Otro efecto interesante que podemos aplicar a un elemento son las sombras. CSS incluye las siguientes propiedades para generar sombras para la caja de un elemento y también para formas irregulares como texto:

- **box-shadow** declara una sombra para la caja. Acepta hasta seis valores. Podemos declarar el *desplazamiento horizontal y vertical de la sombra*, el *radio de difuminado*, el *valor de propagación*, el *color de la sombra* y también podemos incluir el valor *inset* para que la sombra se proyecte dentro de la caja.

- **text-shadow** genera una sombra desde un texto. Podemos declarar el *desplazamiento horizontal y vertical* de la sombra, el *color* y el *radio de difuminado.*

**box-shadow** precisa al menos tres valores para poder determinar el color y el desplazamiento de la sombra. 0 es sin desplazamiento, valores positivos ubican la sombra a la derecha y bajo el elemento, valores negativos la ubican a la izquierda y sobre el elemento.

Ejemplo de sombra sencilla sobre elemento cabecera de documento:

```
header {
  margin: 30px;
  padding: 15px;
  text-align: center;
  border: 1px solid;
  box-shadow: rgb(150,150,150) 5px 5px;
}
#titulo {
  font: bold 26px Verdana, sans-serif;
}
```
![](Media/formato23.png)

Y ahora la misma sombra agregando una distancia de difuminado:

`box-shadow: rgb(150,150,150) 5px 5px 20px;`

![](Media/formato24.png)

Al agregar otro valor en píxeles al final de la propiedad, podemos propagar la sombra. Si añadimos otro valor más, estaremos estableciendo el valor de propagación del la sombra del elemento:

`box-shadow: rgb(150,150,150) 5px 5px 5px 10p;`

![](Media/formato25.png)

Podemos sustituir el valor de propagación por la palabra *inset* para mcombrobar como la sombra se proyecta en el interior del elemento:

`box-shadow: rgb(150,150,150) 5px 5px 10px inset;`

![](Media/formato26.png)

 
