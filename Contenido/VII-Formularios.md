# Formularios - 3ª parte

Otra entrada que genera una herramienta visual en el navegador es **date**. Algunos navegadores lo implementan como un calendario que se despliega cada vez que se hace click en el campo date, que contendrá un *value* para mostrar por defecto en formato año-mes-dia:

`<input type="date" name="fecha" value="2017-02-05">`

En Firefox si funciona, pero no he podido capturar la imagen del calendario desplegado:

![](Media/form6.png)

El tipo **date** no es el único para insertar fechas:

- `datetime-local` **formato año-mes-díaThoras:minutos:segundos.** La **T** en medio no es un error.

- `week` **formato año-semana con W entre los valores: 2023-W27.**

- `month` **formato año-mes.**

- `time` **formato horas-minutos.**

Todos estos valores para el atributo *type* del elemento **input** sirven para enviar los datos requeridos de forma optimizada.

Existe la posibilidad de enviar también colores como información en forma de número hexadecimal, para lo cual HTML también provee el tipo de entrada **color:**

`<input type="color" name="micolor" value="#99BB00">`

![](Media/form7.png)

Para el botón de "submit" o el envío de datos, podemos optar por el tipo "image", que permite incluir una imagen en el botón para mejorar el diseño indicando el *src* y las proporciones.

`<input type="image" src="botonenviar.png" width="100">`

![](Media/form8.png)

HTML ofrece un elemento más versátil para crear botones llamado `<button>`

Este resulta más apropiado para ser personalizado con estilos CSS o ser usado para ejecutar código JavaScript, como se verá más adelante.

Si tenemos un formulario que necesita reproducir información relacionada a medidas, tenemos los elementos `progress` y `meter`.
Aunque no son elementos propios de formulario, son útiles para estos casos.

- `<progress>` **se usa para indicar el progreso de una tarea. Requiere el atributo value para representar el progreso logrado hasta el momento y el atributo max para determinar el nivel a alcanzar para dar por terminada la tarea:**

  `<progress value="30" max="100">0%</progress>`

  ![](Media/form11.png)

- `<meter>` **se usa para representar un rango de valores predefinido, por ejemplo el espacio ocupado en un disco duro. Utiliza los atributos min, max y value para representar el valor medido entre un máximo y un mínimo. Además, se vale de los atributos low, high y optimum, que se usan para segmentar el rango en secciones diferenciadas y declarar la posición óptima:**

  `<meter value="60" min="0" max="100" low="40" high="80" optimum="100">60</meter>`

  ![](Media/form12.png)

El color de la barra depende del valor actual respecto a las secciones implementadas. Si el valor es inferior a low, la barra será roja, si está entre low y high, naranja y si supera el nivel de high será verde (en Firefox, al menos).

## Enviando el formulario

Los datos introducidos se envían al servidor usando la sintaxis *nombre/valor*, donde nombre es el valor del atributo **name** y valor el **contenido introducido por el usuario.**

Los navegadores usan dos métodos para enviar esta información: **GET** y **POST**, dependiendo del valor asignado al atributo `method` del elemento `<form>`. Si el método se ha declarado como GET, los  pares nombre/valor se agregarán al final de la URL, pero si se ha declarado como post, los valores se incluyen en el cuerpo de la solicitud HTML.

Es decir, debemos usar POST cuando se trate de información personal y privada la que estamos enviando al servidor, de otra manera podemos usar el método GET, ya que la información será visible y restringida por el número máximo de caracteres que soporta la URL.

Un ejemplo de código sencillo para un formulario a ser enviado por método GET sería el siguiente:

```
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <title>Formularios</title>
</head>
<body>
  <section>
    <form name="formulario" method="get" action="procesar.php">
      <p><input type="text" name="val"></p>
      <p><input type="submit" value="Enviar"></p>
    </form>
  </section>
</body>
</html>
```
En este ejemplo un archivo llamado *procesar.php* es declarado a cargo de procesar la información. Cuando se pulsa el botón Enviar, el navegador crea una solicitud HTTP que incluye la URL que apunta a dicho archivo, seguido del signo ? e inmediatamente a continuación los pares *nombre/valor* se agregan separados por el signo **=**. Si hubiera más campos de información a ser enviados, se incluirían en la URL separados por el signo &:

`www.dominiodeejemplo.com/procesar.php?val=10&val=20`...etc

En el servidor, el archivo procesar.php es ejecutado produciendo a su vez un archivo de salida HTML para el navegador.

En este caso para figurar un ejemplo sencillo, el código contenido en el archivo *procesar.php* podría ser algo así:

```
<?php
  print('El valor es: ' . $_GET['val']);
?>
```

Las llaves \<?php - ?> abren y cierran el código PHP para que en el servidor sea ejecutado como tal. El resto del documento puede ser un documento de estructura HTML vacío de contenido, con el código PHP en el lugar donde nos interesa que aparezca la respuesta, por ejemplo entre unas etiquetas `<p>` dentro de un apartado `<section>`

La función **print()** devuelve la cadena *El valor es:* seguida de la información introducida en el campo por el usuario capturada en el nombre `$_GET` ( si se hubiera enviado por POST sería `$_POST`) y referida por el valor del atributo **name=** *'val'*.

Si se hubieran enviado más campos, entonces entre corchetes aparecería el valor dado al atributo **name** en cada uno de ellos en líneas diferentes.
