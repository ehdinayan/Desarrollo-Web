# II - Referencias

Se da la situación de que amenudo tal vez no nos interese aplicar una misma regla a todos los elementos de un mismo tipo, sino que sólo a algunos. Por ejemplo, podemos usar los valores de los atributos *id* y *class* para referenciar el elemento al cual queremos aplicar un estilo en particular.

## Nombres

Se puede declarar un mismo estilo a diferentes elementos simplemente incorporando el nombre como nuevo selector en la regla CSS, separándolo por comas del anterior:

```
p, span
{
  font-size:20px;
}
```
De esa manera los elementos `<p>` y `<span>` recibirán los mismos estilos.

También se puede referenciar únicamente un elemento particular definiendo también su elemento padre como selector separados por un espacio:

```
main p
{
    font-size:20px;
}   
```

Ahora los elementos `<p>` dentro de `<main>` son los afectados por el tamaño de fuente, aunque se encuentren a su vez en secciones diferentes del documento (nav, aside, etc).

También se puede referenciar un elemento adyacente al selector de la regla para que se vea afectado por el mismo estilo, esto se hace con los símbolos **+** y **- :**

```
h1 + p
{
  font-size:20px;
}

p - p
{
  font-size:20px;
}
```

En el código de arriba se declara el tamaño para el primer elemento `<p>` que haya tras `<h1>`, mientras que seguidamente se toma como selector a todo elemento `<p>` que a su vez sea precedido por un elemento `<p>`

## Atributo id

Para seleccionar un elemento HTML sin considerar su tipo, podemos usar el atributo *id*, de manera que en el documento HTML tendremos:

`<p id="mitexto">frasecualquiera</p>`

y en la regla CSS habrá:

```
#mitexto
{
  font-size:20px;
}
```
