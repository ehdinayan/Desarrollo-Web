# Propiedeades - 7ª parte

## Continuación Gradientes

- **linear-gradient(posición,angulo,colores)** crea un gradiente lineal. La **posición** se declara con los valores *top, bottom, left, right.* El atributo **ángulo** define la dirección del gradiente y se puede declarar con las unidades *deg* (grados), *grad* (gradianes), *rad* (radianes), o *turn* (espiras). El atributo colores es la lista de colores que participan en el gradiente separados por coma. También pueden incluir un segundo valor separado por un espacio para definir mediante porcentaje la posición donde finaliza el color:

```
header {
  margin: 30px;
  padding: 15px;
  text-align: center;
  border: 1px solid;
  background: -moz-linear-gradient(top, #FFFFFF, #666666);
}
```
![](Media/linear-gradient.png)

También se puede comenzar el gradiente desde una esquina del elemento, como en el siguiente ejemplo:

`background: -moz-linear-gradient(top right, #FFFFFF, #666666);`

![](Media/linear-gradient2.png)

También podemos configurar la dirección con un ángulo en grados:

`background: -moz-linear-gradient(30deg, #FFFFFF, #666666);`

![](Media/linear-gradient3.png)

*NOTA: Con esta configuración, los valores 0, 90, 180, 270 equivalen a las posiciones left, bottom, right, y top respectivamante.*

También es posible crear gradientes multicolor:

`background: -moz-linear-gradient(top, white 15%, lightblue 50%, blue);`

![](Media/linear-gradient4.png)

Otra cosa que podemos hacer es que el gradiente sea translúcido, de forma que el fondo se vea a través de él. Este efecto también se puede lograr usando la propiedad rgba() vista anteriormente. Aqui asignamos una imagen de fondo al cuerpo del documento para realizar la comprobación:

```
body {
  background: url("Media/ladrillosclaros.jpg");
}
header {
  margin: 30px;
  padding: 15px;
  text-align: center;
  border: 1px solid;
  background: -moz-linear-gradient(top, transparent, #666666);
}
```

![](Media/linear-gradient5.png)
