# HTML
## ESTRUCTURA - III

**Atributos globales**

Aunque la mayoría de los elementos estructurales tienen un propósito implícito que se refleja en sus nombres, esto no significa que se deban usar sólo una vez en el mismo documento. Por ejemplo, **section** y **aside** pueden usarse muchas veces para representar diferentes partes de la estructura, y **div** también suele ser usado de forma repetida para separar contenido dentro de secciones. Por esta razón, HTML define atributos globales para asignar identificadores personalizados a cada elemento...

`id` Nos permite asignar un identificador único a cada elemento.

`class` Asigna el mismo identificador a un grupo de elementos.

Por ejemplo, para dar una identificación única a cada una de las partes `<section>` dentro del documento HTML, podemos hacer:

```
<main>
  <section id="noticias">
    Artículos largos
  </section>
  <section id="noticiaslocales">
    Artículos cortos
  </section>
  <aside>
    Cita de articulo uno
    Cita de articulo dos    
  </aside>
</main>
```

 De esta manera podemos asignar diferentes estilos a cada una de las secciones `<section>`

 Si por el contrario queremos definir múltiples espacios dentro de una misma sección con `<div>`, podemos usar el atributo **class** para luego dar un mismo estilo a esas divisiones que albergarán un contenido similar:

 ```
 <main>
  <section>
    <div class="libros">Libro: IT, Stephen King</div>
    <div class="libros">Libro: Carrie, Stephen King</div>
    <div class="libros">Libro: El resplandor, Stephen King</div>
    <div class="libros">Libro: Misery, Stephen King</div>
  </section>
  <aside>
    Cita del artículo uno
    Cita del artículo dos
  </aside>
</main>
```

Es buena práctica a la hora de nombrar las clases incluir solo letras y números, siempre comenzar con una letra y evitar caracteres especiales.
