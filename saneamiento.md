### Saneamiento

El saneamiento remueve \(o evita\) los caracteres ilegales o inseguros que provienen de la entrada de datos externa.

Por ejemplo, debería sanear la entrada de datos antes de incluirla en el código HTML o insertarla a una consulta de SQL. Cuando utiliza parámetros consolidados con [PDO](http://phpdevenezuela.github.io/#bases_de_datos), este saneara la entrada de datos automáticamente.

En veces es requerido que permita que algunas etiquetas de HTML que se consideren inofensivas puedan ser incluidas en la entrada de datos para una página de su sitio. Esto es algo muy difícil de realizar de una manera segura y muchos lo evitan al usar otros estándares de formato de texto más restrictivos como Markdown o BBCode, aunque librerías que proveen una lista blanca de etiquetas como el [HTML Purifier](http://htmlpurifier.org/) se concibieron para este propósito.

[Vea los filtros de saneamiento](http://www.php.net/manual/es/filter.filters.sanitize.php)

