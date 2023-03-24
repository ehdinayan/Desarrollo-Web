# HTML
## ESTRUCTURA - I

Para asegurarnos de que el contenido de nuestuos documentos sea interpretado correctamente como código HTML, debemos agregar la declaración <!DOCTYPE> al comienzo del archivo. Esto ayuda al navegador a decidir cómo debe generar la página web:
`<!DOCTYPE html>`

**Elementos estructurales**

Los siguientes son los elementos disponibles para definir la columna vertebral de la estructura y facilitar la información que el navegador necesita para mostrar la página en la pantalla:

`<html>`
Delimita el código html. Puede incluir el atributo *lang* para definir el idioma del documento.

`<head>`
Se usa para definir la información necesaria para configurar la página web. Por ejemplo el título, el tipo de codificación de caracteres y los archivos externos requeridos por el documento.

`<body>`
Este elemento delimita el contenido del documento (la parte visible de la página)

Entre las etiquetas `<head>` debemos definir el título de la página web, declarar el tipo de codificación de caracteres, facilitar información general acerca del documento, e incorporar los archivos externos con estilos y códigos necesarios para generar la página. Excepto por el título e iconos. el resto de la información insertada en medio de estas eriqueras no es visible para el usuario.

La otra sección que forma parte de la organización principal de un documento HTML es el cuerpo, la parte visible que se especifica con el elemento `<body>`

**Cabecera**

La estructura básica ya está lista. Ahora tenemos que construir la página, comenzando por la definición de la cabecera (head). Aqui se incluyen toda la información y recursos para generar la página. Los siguientes son elementos disponibles para este propósito:

`<title>` Define el titulo visible en la pestaña del navegador.

`<base>` Define la URL usada por el navegador para establecer la ubicación real de las URL relativas. El elemento debe incluir el atributo **href** para declarar la URL base.
Cuando se declara este elemento, en lugar de la URL actual, el navegador usa la URL asignada al atributo href para completar las URL relativas.

`<meta>` Metadatos asociados con el documento, como descripción, palabras claves, tipo de codificación de caracteres, etc. Puede incluir atributos como **name** para describir el tipo de metadata, **content** para especificar el valor o **charset** para declarar el tipo de codificación de caracteres a utilizar para procesar el contenido.

`<link>` Especifica la relación entre el documento y un recurso externo que bien pueden ser estilos CSS. Puede incluir el atributo **href** para identificar la ubicación de los recursos, **rel** para definir el tipo de relación, **media** para especificar el medio al que el recurso está asociado, o **type** y **size** para definir el tipo de recurso y su tamaño. Esto último generalmente es usado para incluir un icono o *favicon* en la pestaña del navegador.

`<style>` Se usa para declarar estilos CSS dentro del mismo documento.

`<script>` Se usa para cargar o declarar código JavaScript.

Asi podríamos tener la plantilla de un documento html5 con su cabecera base más o menos de ésta manera:

```
<!Doctype html>
<html lang="es">

<head>
 <title>titulo del documento</title>
 <meta charset = "utf-8">
 <meta name = "description" content = "descripcion del documento">
 <meta name = "keywords" content = "contenido del documento">
 <link rel = "icon" href = "imagenes/favicon.png" type="image/png" sizes="16x16"> <!--incluir favicon en pestaña-->
 <style type="text/css"><!--en caso de ser estilos en local--></style>
 <link rel="stylesheet" href="CSS/estilos.css"><!--en caso de cargar hojas de 		estilos-->
</head>

<body>
</body>

</html>
```
