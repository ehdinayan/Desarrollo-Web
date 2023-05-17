# Propiedades - 9ª parte

## Transiciones

Ya que una animación real requiere de una transición entre los dos pasos del proceso, podemos valernos de las siguientes propiedades CSS para generar dichas transiciones:

- **transition-property** especifica las propiedades que participan en la transición. Podemos incluirlas todas asignando el valor *all*.

- **transition-duration** especifica la duración en segundos.

- **transition-timing-function** determina la función que se usa para calcular los valores de la transición. Los valores disponibles son *ease, ease-in, ease-out, ease-in-out, linear, step-start, step-end*

- **transition-delay** indica al navegador el tiempo a esperar antes de iniciar la animación.

- **transition** nos permite declarar todos los valores de la transición al mismo tiempo.

Añadiendo esta línea a la regla de la imagen anterior veremos como se anima automáticamente al pasar el ratón por encima hasta alcanzar la posición especificada por la propiedad *transform*:

```
.plane img {
  width:350px;
  transition: transform 1s ease-in-out 0s;
```
![](Media/transiciones.png)

La propiedad transition puede recibir hasta cuatro parámetros separados por un espacio. El primer valor es la propiedad que se considerará para crear la transición (transform en el ejemplo), el segundo parámetro determina la duración (1 seg), el tercero determina la manera en que se llevará a cabo la transición por medio de una curva Béizer, y el último parámetro determina cuantos segundos tarda la animación en comenzar.
