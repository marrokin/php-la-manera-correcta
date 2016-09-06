## Filtrado de Datos

Nunca, jamás, se confíe de los datos que provienen del exterior de su aplicación PHP. Siempre sanee y verifique los datos de entrada antes de usarlos en su código. Las funciones filter\_var\(\) y filter\_input\(\) proporcionan saneamiento de los datos y verifican la validez del formato del texto \(por ejemplo, las direcciones de correo electrónico\).

Los datos de entrada exteriores pueden contener cualquier cosa: los datos provenientes de formularios en $\_GET y $\_POST, algunos valores provenientes del súper global $\_SERVER, el cuerpo de la solicitud HTTP vía la función fopen\('php:\/\/input', 'r'\). Recuerde que la entrada exterior de datos no está limitada a los datos que provienen de un usuario a través de un formulario, también provienen de la subida y descarga de archivos, valores de sesión, datos de cookies, y los servicios web exteriores.

Aunque los datos que provienen del exterior pueden ser guardados, combinados y se puede acceder a ellos posteriormente, todavía siguen siendo datos exteriores. Cada vez que procesa, imprime, concatena, o los incluye con otros datos en su código, pregúntese si los datos han sido filtrados apropiadamente y si es confiable.

Los datos pueden ser _filtrados_ de diferente manera dependiendo de su proposito. Por ejemplo, cuando se pasan datos sin filtrar a la salida de HTML de su página, corre el riesgo de ejecutar código sin verificar de HTML o JavaScript en su sitio. Esto es conocido \(en inglés\) como Cross-Site Scripting \(XSS\), y puede causar mucho daño a su aplicación. Una manera de prevenir estos ataques es sanear todas las etiquetas de HTML en sus datos de entrada al remover etiquetas o convirtiéndolas en entidades de HTML.

Otro ejemplo es cuando se pasan opciones que van a ser ejecutadas en la línea de comando. Esto puede ser extremadamente peligroso y en general no es una buena idea. Sin embargo, puede usar la función escapeshellarg que viene incluida en PHP para sanear los argumentos de ejecución de un comando.

Un último ejemplo es el de aceptar la entrada de datos para determinar que archivo se necesita cargar del sistema de archivos. Esto puede ser explotado al cambiar el nombre del archivo a una ruta de archivo diferente. En este caso es necesario remover los caracteres “\/”, “..\/”, [bytes nulos](http://php.net/manual/es/security.filesystem.nullbytes.php) y otros de la ruta de archivo para que no permita cargar archivos escondidos, no públicos, o de otra manera sensitivos.

* [Aprenda acerca del filtrado de datos](http://www.php.net/manual/es/book.filter.php)
* [Aprenda acerca de la función filter\_var](http://php.net/manual/es/function.filter-var.php)
* [Aprenda acerca de la función filter\_input](http://www.php.net/manual/es/function.filter-input.php)
* [Aprenda como manipular los bytes nulos](http://php.net/manual/es/security.filesystem.nullbytes.php)

