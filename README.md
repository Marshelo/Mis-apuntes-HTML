# Mis apuntes de HTML5
**Indice**
  * [Sintaxis](#sintaxis)
    * [Formato de etiquetas](#formato-de-etiquetas)
    * [Comentarios](#comentarios)
  * [Lo primero](#lo-primero)
    * [Herramienta del navegador]("#herramienta-del-navegador)
    * [HTML](#html)
    * [Head](#head)
    * [Body](#body)
  * [Etiquetas básicas](#etiquetas-básicas)
    * [Párrafos](#párrafos)
    * [Saltos de linea](#salto-de-linea)
  * [Metadatos](#metadatos)
    * [Descripción](#descripción)
  * [Multimedia](#multimedia)
    * [Imágenes](#imágenes)
    * [Video](#video)
  * [Enlaces útiles](#enlaces-útiles)


------------


## Sintaxis
### Formato de etiquetas
La forma en que en html comunicamos nuestras ideas es en un formato peculiar, el cual consiste en etiquetas. Estas etiquetas pueden estar escritas de 3 formas diferentes:
* Con una etiqueta para abrir y otra para cerrar.
    ```html
    <nombre-etiqueta opción info-extra="valor">Contenido de la etiqueta</nombre-etiqueta>
    ```
* O con solo una etiqueta que se cierra sola.
    ```html
    <nombre-etiqueta opción info-extra="valor" />
    ```
    De esta forma la etiqueta se cierra sola y por comodidad se puede omitir el "/" al final quedando así:
    ```html
    <nombre-etiqueta opción info-extra="valor">
    ```
    y el navegador lo interpretará perfectamente.
> Nota: no importa cuantos saltos de linea, espacios o tabs pongas dentro del contenido de una etiqueta, nunca afectará su funcionamiento, a no ser que fuerces a que ocurra algo.

Y por último unos ejemplos:
* Etiqueta de apertura y cierre:
    ```html
    <video controls preload="auto">
        <source src="https://storage.coverr.co/videos/TYNd6glBOcCmIS7cbW4hoyEOtoA9fzXo?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhcHBJZCI6Ijg3NjdFMzIzRjlGQzEzN0E4QTAyIiwiaWF0IjoxNjMwNTY0NDQ1fQ.tGc5QS6w3ooK7sN6eLz6_ZPHeJb_IHciKNAosisaXew">
    </video>
    ```
* Solo una etiqueta:
    ```html
    <meta charset="UTF-8" />
    ```
    ```html
    <meta charset="UTF-8">
    ```
> Nota: el funcionamiento de estas etiquetas se aclarará más adelante; estos son solo ejemplos ;).

### Comentarios
Los comentarios en cualquier código son una gran herramienta, ya que nos permiten documentar el funcionamiento del código en sí mismo.
En html todo lo que esté entremedio de `<!--` y `-->` será ignorado por el navegador, pero lo podrás ver de todas formas como comentario en el código fuente desde el navegador.
```html
<!-- Contenido
   del 😎
comentario -->
```
> Cuidado!: Si no cierras con "`-->`" el comentario, todo el código que venga después será también un comentario, así que dejará de ser funcional.


------------


## Lo Primero
Antes que nada tienes que abrir tu editor de código favorito y crear un archivo con la extensión `.html`.

### Herramienta del navegador
En los navegadores más populares, como chrome, firefox, etc, hay una herramienta que nos permite ver todo el código fuente de una página web. Por lo general esta herramienta se activa con la tecla `F12`, pero en algunos casos puede que sea con `Fn + F12`.

### HTML
El esqueleto de un html siempre será el siguiente:
```html
<!DOCTYPE html>
<html lang="es">
    <head>
        <!-- Contenido -->
    </head>
    <body>
        <!-- Contenido -->
    </body>
</html>
```
`<!DOCTYPE ...>` es de extrema importancia, ya que esta etiqueta definirá cómo el navegador interpretará el archivo html. Con `<!DOCTYPE html>` el archivo se interpretará como HTML5. La etiqueta `<html>` puede ser implicita, pero para poner `lang="idioma"` es estrictamente necesario ponerla explicita. En `lang="idioma"` se e indica al buscador cuál es el idioma del html, para hacer una búsqueda más eficiente.
> Nota: "es" es español, y "en", inglés.
### Head
El head es todo el código que tiene que cargar antes de visualizar cualquier cosa en la página, aquí van cosas como los metadatos, hojas de estilos, el titulo de la página, la descripción, entre otros.
```html
<head>
    <meta charset="UTF-8">
    <title>Compras online</title>
    <meta name="description" content="En Compras Online encontrarás los mejores precios con el mejor despacho a domicilio de la región">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="robots" content="index.html,follow">
</head>
```
> Nota: estas etiquetas y cada metadato será aclarado más adelante; es solo un ejemplo.

### Body
El body es el todo cuerpo de la página, desde el header hasta el footer. Aquí pueden ir etiquetas como las de titulos, párrafos, multimedia, tablas, entre otros.
```html
<!-- Completar :) -->
```

------------


## Etiquetas básicas
Para empezar a escribir algo de código te mostraré algunas etiquetas básicas que sí o sí tienes que saber.
### Párrafos
En html se usa la etiqueta `<p>` para escribir en párrafos:
```html
<p>Aquí todo el contenido que quieras escribir en un párrafo</p>
<p>Y aquí otro párrafo, porque sí no más :P</p>
```
### Salto de linea
Cuando escribes con saltos de lineas normales (con ENTER), los párrafos no lo leerán ni ninguna etiqueta, y es por eso que existe esta etiqueta solo para hacer saltos de linea:
```html
<p>
Una linea.<br/>
Una segunda linea.<br>
Y otra más.
</p>
```

------------

## Metadatos
### Descripción
Esta etiqueta sirve para mostrar una breve descripción de la página web en el buscador.
```html
<head>
    <meta name="description" content="Contenido de la descripción">
</head>
```
##### Ejemplo
* En google:
![Descripción de la rae vista desde el buscador google](./src/pag-rae.png)
* Código fuente:
![Descripción de la rae vista desde el buscador google](./src/descripcion-rae.png)


------------


## Multimedia
### Imágenes
```html
<figure>
    <img src="URL o archivo" alt="Txt si la img no se ve">
    <figcaption>Texto a los pies de la img</figcaption>
</figure>
```
`<figure>` es lo mismo que `<div>`, pero semánticamente más apropiado, y además viene con una etiqueta propia: `<figcaption>`, la cual sirve para mostrar texto a los pies de la imagen.

### Video
```html
<section>
    <video controls preload="auto">
        <source src="URL o archivo#t=73,88">
    </video>
</section>
```
En la etiqueta `<video>` está la opción `controls` para activar los controles básicos de reproducción de un video.
> Nota: sin `controls` no se puede reproducir el video manualmente, y como está penalizado en los navegadores más populares la reproducción de un video automaticamente, nunca se reproducirá el video.

Con `preload="auto"` se especifica que el navegador al cargar la página, va a cargar con él el video, por lo que para el usuario será más cómodo, ya que no tendrá que esperar a que cargue cuando le de play.

------------

## Enlaces útiles
* [Todas las etiquetas HTML](https://i.emezeta.com/weblog/html5-cheatsheet/html5-cheatsheet-2019.pdf "Torpedo HTML")
