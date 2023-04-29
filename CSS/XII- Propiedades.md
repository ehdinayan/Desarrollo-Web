# Propiedades - 8ª parte

## Transformaciones

Podemos modificar la posición, tamaño y apariencia de los elementos HTML con el atributo **transform**. Esta propiedad realiza cuatro transformaciones básicas: escalado, rotación, inclinación y translación, valiéndose de las siguientes funciones:

- **scale(x,y)** modifica la escala mediante números decimales o enteros. El tamaño original se preserva con el valor 1. Si damos un valor negativo a cualquiera de los ejes, se invierte la posición del elemento en el eje indicado. Si sólo se declara un valor, ese mismo valor se usa para ambos ejes. También se puede usar las funciones **scale(x)** y **scale(y)** para modificar las escalas de cada eje de forma independiente.

  ```
  header {
  background: url("Media/ladrillosclaros.jpg");
  margin: 30px;
  padding: 15px;
  text-align: center;
  border: 1px solid;
  box-shadow:5px 5px 2px #010080;
  transform: scale(2);
  }
  ```

  ![](Media/tranformaciones.png)

  `transform: scale(1, -1);`

  ![](Media/transformaciones2.png)

- **rotate(ángulo)** rota el elemento. Se puede declarar en *deg(grados), grad(gradianes), rad(radianes)* o *turn(espiras)*.

  Aquí rotamos 45 grados la cabecera en el sentido de las agujas del reloj:

  ```
  header {
  background: url("Media/ladrillosclaros.jpg");
  margin: 30px;
  padding: 15px;
  text-align: center;
  border: 1px solid;
  box-shadow:5px 5px 2px #010080;
  transform:rotate(45deg);
  }
  ```

  ![](Media/transformaciones3.png)

- **skew(ángulo)** inclina el elemento, cambiando su simetría. El atributo representa los grados de desplazamiento en el eje vertical y horizontal. Los valores se pueden declarar en las mismas unidades que en la propiedad **rotate** y también de forma independiente:

  ```
  header {
  background: url("Media/ladrillosclaros.jpg");
  margin: 30px;
  padding: 15px;
  text-align: center;
  border: 1px solid;
  box-shadow:5px 5px 2px #010080;
  transform:skew(20deg);
  }

  .plane img {
  width:350px;
  transform:skew(-20deg, -15deg);
  }
  ```

  ![](Media/transformaciones4.padding)

- **translate(x,y)** Esta función desplaza el elemento a la posición determinada por los valores de los ejes x e y. Utiliza el sistema de coordenadas de píxeles en pantalla para establecer la posición del elemento en base a su posición actual, por lo que valores negativos siempre ubicarán el objeto a posiciones por encima y a la izquierda de donde se encuentra. Para declarar varias transformaciones a la vez para un mismo elemento, hay que separar las funciones por un espacio:

  ```
  .plane img {
  width:350px;
  transform:translateX(100px) rotate(45deg) skew(20deg) scale(1.5);
  }
  ```
  ![](Media/transformaciones5.png)

  Cuando se aplican varias funciones de transformación a un elemento, se debe considerar que el orden es importante, ya que se alteran aspectos como el punto de origen o el centro del mismo, propiedades sobre las que las funciones siguientes trabajan.
