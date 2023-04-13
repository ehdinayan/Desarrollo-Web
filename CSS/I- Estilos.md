# Estilos

CSS es un lenguaje que facilita instrucciones que podemos usar para asignar estilos a los documentos HTML, como colores, tipos de letra, tamaño, etc. Los estilos deben definirse en CSS y luego asignarlos a los elementos HTML hasta que logremos el diseño visual que queremos para nuestra página.

En CSS, los estilos se declaran con propiedades y sus valores correspondientes separados por dos puntos y entre llaves. CSS define una sintaxis que facilita el proceso de asignar múltiples propiedades a un mismo elemento: **la regla.**

Por ejemplo, la siguiente regla se identifica con el selector **p**, por lo tanto sus propiedades se aplicarán a todos los elementos `<p>` del documento:

```
p{
  color:#FF0000;
  font-size: 24px;
}
```
**Con esta regla** asignamos a nuestro documento una letra en color rojo y de tamaño 24px para todos los elementos `<p>`

## Aplicando Estilos

Para que nuestros estilos sean aplicados, debemos incluirlos en el documento. Existen tres técnicas disponibles para este proceso:

- **Estilos en linea:** Utiliza un atributo global llamado *style* para incluir los estilos directamente en el elemento. No es muy aconsejable debido a que si queremos hacer cambios a posteriori en nuestro documento, deberemos ir elemento a elemento cambiándolos uno por uno. Además, implica que el tamaño del documento sea más grande de la cuenta haciéndolo más engorroso de actualizar y mantener y seguramente tendremos mucho código repetido. En cambio, puede ser práctico para ver como quedan estilos antes de ser implementados, por ejemplo.

  `<p style="font-size:20px;">Mi texto</p>`

- **Estilos incrustados:** HTML provee el elemento `<style>` que normalmente se ubica en la cabecera del documento para declarar allí todos los estilos del documento mediante reglas. Hacerlo así ahorra espacio y hace que el código sea más coherente y fácil de mantener, pero requiere que copiemos las mismas reglas en cada uno de los documentos de nuestro sitio web. Debido a que varias de nuestras páginas compartirán el mismo diseño, varias de nuestras reglas se duplicarán.

    ```
    <!DOCTYPE html>
    <html lang="es">
    <head>
      <title>Este texto es el título del documento</title>
      <meta charset="utf-8">
      <style>
        p {
          font-size: 20px;
        }
      </style>
    </head>
    <body>
      <main>
        <section>
          <p>Mi texto</p>
        </section>
      </main>
    </body>
    </html>
    ```


- **Hojas de estilos:** Probablemente sea el mejor modo de implementar los estilos. Usamos el elemento `<link>` para enlazar un documento `.css` que será cargado desde el documento o página que lo necesite. Aqui se carga la hoja de estilos **misestilos.css:**

    ```
    <!DOCTYPE html>
    <html lang="es">
    <head>
      <title>Este texto es el título del documento</title>
      <meta charset="utf-8">
      <link rel="stylesheet" href="misestilos.css">
    </head>
    ```

## Hojas de estilo en cascada - Cascading Style Sheets

Se llamó así porque el uso apropiado de este lenguaje implica que los estilos aplicados a los elementos de los niveles más bajos de la jerarquía heredan los estilos de los niveles más altos.

Por ejemplo, si asignamos el tamaño de letra al elemento `<section>` en vez de al elemento `<p>`en nuestro fichero de estilos, ocurrirá que todos los elementos que sean hijos de ese `<section>` se verán afectados.

Para que los elementos hijos no hereden estilos de los elementos padre, simplemente deberán tener declarados sus propios estilos en una regla propia.

 
