# Curso de Sass 2018

Un **pre-procesador** es una herramienta que nos permite escribir pseudo-código que más adelante es convertido a CSS.

[**Sass**](https://sass-lang.com/) es un pre-procesador maduro, estable y poderoso que funciona como una extensión de CSS. \
Esta herramienta permite potenciar las funcionalidades y habilidades de CSS.

Alguna de las cosas que podemos hacer con Sass:

- Manejar mixins.
- Manejar mixins paramétricos.
- Aplicar ciclos.
- Usar módulos.

## Comenzar a utilizar en nuestro proyecto

A diferencia de CSS, los archivos de SASS tienen la extensión `.scss`. \
Dentro de estos archivos podemos agregar código CSS sin ningún problema.

El problema que tenemos ahora es que el navegado no puede interpretar los archivos `.scss`, para solucionar esto debemos utilizar algún compilador de **Sass**.

En el curso muestran dos:

- Codekit para Mac.
- Preposs para Windows.

O incluso si usamos Visual Studio Code podemos descargar un extensión para que haga este trabajo automáticamente.

- Live Server
- Live Sass Compiler

En mi caso yo estoy en Ubuntu y prefiero utilizar un paquete de Node para este trabajo, el paquete se llama `sass`. \
Lo podemos instalar en nuestro proyecto con `npm install sass` y de forma global con `sudo npm install -g sass`.

## Compilar código Sass

Ahora tenemos las herramientas para compilar el Sass, ahora toca **compilar**.

Usando **Node** lo hacemos con `sass --watch /entada.scss:/salida.css`. \
Usamos `--watch` para que cada vez que hagamos un cambio se vuelva compilar el código.

Para mayor productividad yo cree dos Scripts:

```json
{
  "scripts": {
    "css-compile": "sass --watch  --source-map --embed-sources --no-error-css src/scss/:dist/css/",
    "css-minify": "sass --style=compressed --source-map --embed-sources --no-error-css src/scss/style.scss dist/css/style.min.css"
  }
}
```

`npm css-compile`, compile all the sass code into the `./src/scss/` folder.
`npm run css-minify`, does the same as `npm css-compile` and then minifies the compiled files.

## Separar los archivos por módulos
