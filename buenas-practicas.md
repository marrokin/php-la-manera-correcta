# Buenas Prácticas

## **Fundamentos**

PHP es un gran lenguaje que permite a cualquier desarrollador producir código de forma rápida y de manera eficiente. Sin embargo, mientras que avanzamos con el lenguaje, a menudo olvidamos \(o pasamos por alto\) las prácticas básicas que aprendimos al inicio, tomando así atajos o malas prácticas. Para ayudar a combatir este problema común, esta sección tiene como objetivo recordar a los desarrolladores las buenas prácticas dentro de PHP.

* Continua leyendo acerca de [Los Fundamentos](http://phpdevenezuela.github.io/php-the-right-way/pages/The-Basics.html)

## Fecha y Hora

PHP dispone de una clase llamada **DateTIme** para asistir en la lectura, escritura, comparación y calculación de la fecha y hora. Existen muchas funciones en PHP relacionadas con la manipulación de la fecha y la hora, sin embargo, la clase **DateTime** provee una mejor interface orientada a objetos para los situaciones más comunes. También tiene la capacidad de utilizar los husos horarios; esta información no se considerará en esta corta introducción.

Para comenzar a trabajar con DateTime primero se convierte la cadena de texto que contiene la fecha y la hora a un objeto con el método de fabricación createFromFormat\(\) o también se puede crear un objeto con new \DateTime que contendrá la fecha y hora actual. Después, puede utilizar el método format\(\) para convertir el objeto DateTime de regreso a una cadena de texto e imprimirla:

&lt;?php

$fecha = '22. 11. 1968';

$inicio = \DateTime::createFromFormat\('d. m. Y', $fecha\);



echo "Fecha de Inicio: " . $inicio-&gt;format\('m\/d\/Y'\) . "\n";

Se puede utilizar la clase DateInterval para realizar calculaciones con DateTime. La clase DateTime tiene métodos como add\(\) y sub\(\) que requieren que pase un DateInterval como argumento. Nunca escriba código que cuente con el mismo número de segundos en todos los días ya que los ajustes de los husos horarios y el horario de verano \(daylight savings time\) invalidaría esa suposición. En vez de eso, utilice los intervalos de fechas para hacer sus calculaciones. Para calcular la diferencia entre fechas utilice el método diff\(\). Este le devolverá un return new DateInterval, lo cual puede ser fácilmente impreso en la pantalla.

`<?php`

`  // Crea una copia de $inicio y añade un mes y 6 días`

`  $final = clone $inicio;`

`  $final->add(new \DateInterval('P1M6D'));`

`  $diff = $final->diff($inicio);`

`  echo "Diferencia: " . $diff->format('%m mes, %d días (total: %a días)') . "\n";`

`  // Diferencia: 1 mes, 6 días (total: 37 días)`



`<?php`

`  if($inicio < $final) {`

`     echo "¡El inicio sucede antes que el final!\n";`

`  }`

Este último ejemplo demuestra cómo se utiliza la clase DatePeriod para iterar sobre eventos periódicos. El objeto toma dos objetos DateTime, uno para el inicio y el otro para el final, y el intervalo que define el número de eventos periódicos que se devuelven.

`<?php`

`  // Imprimir todos los jueves entre $inicio y $final`

`  $intervaloDePeriodo = \DateInterval::createFromDateString('first thursday');`

`  $iteradorDePeriodo = new \DatePeriod($inicio, $intervaloDePeriodo, $final, \DatePeriod::EXCLUDE_START_DATE);`

`  foreach($iteradorDePeriodo as $fecha)`

`  {`

`     // Imprimir cada fecha en el periodo`

`     echo $fecha->format('m/d/Y') . " ";`

`  }`

* [Leer acerca de la clase DateTime](http://php.net/manual/es/book.datetime.php)
* [Como formatear la fecha](http://php.net/manual/es/function.date.php) \(Opciones de los formatos aceptados para una fecha\)

## Patrones de Diseño

Cuando se desarrolla una aplicación es muy bueno utilizar patrones de uso común en su código y patrones para la estructura general de su proyecto. El usar estos patrones ayuda y facilita el manejo de su código y permite a otros desarrolladores a entender fácilmente como es que encajan todas las partes de su aplicación.

Si utiliza un armazón \(_framework_\) para el desarrollo de su proyecto, entonces la mayor parte del nivel superior de su código estará basado en este armazón, así que muchas de las decisiones ya han sido hechas por usted. Pero todavía depende de usted el escoger los mejores patrones a seguir en el código que desarrolla sobre este armazón. Si, por otro lado, no está utilizando un a ra desarrollar su aplicación, entonces necesita encontrar los patrones que mejor se adapten al tipo y tamaño de su proyecto.

Continúe leyendo acerca de los [Patrones de Diseño](http://phpdevenezuela.github.io/php-the-right-way/pages/Design-Patterns.html)

## Working with UTF-8

_This section was originally written by _[_Alex Cabal_](https://alexcabal.com/)_ over at _[_PHP Best Practices_](https://phpbestpractices.org/#utf-8)_ and has been used as the basis for our own UTF-8 advice_.

### There’s no one-liner. Be careful, detailed, and consistent.

Right now PHP does not support Unicode at a low level. There are ways to ensure that UTF-8 strings are processed OK, but it’s not easy, and it requires digging in to almost all levels of the web app, from HTML to SQL to PHP. We’ll aim for a brief, practical summary.

### UTF-8 at the PHP level

The basic string operations, like concatenating two strings and assigning strings to variables, don’t need anything special for UTF-8. However most string functions, like strpos\(\) and strlen\(\), do need special consideration. These functions often have an mb\_\* counterpart: for example, mb\_strpos\(\) and mb\_strlen\(\). These mb\_\* strings are made available to you via the [Multibyte String Extension](http://php.net/manual/en/book.mbstring.php), and are specifically designed to operate on Unicode strings.

You must use the mb\_\* functions whenever you operate on a Unicode string. For example, if you use substr\(\) on a UTF-8 string, there’s a good chance the result will include some garbled half-characters. The correct function to use would be the multibyte counterpart, mb\_substr\(\).

The hard part is remembering to use the mb\_\* functions at all times. If you forget even just once, your Unicode string has a chance of being garbled during further processing.

Not all string functions have an mb\_\* counterpart. If there isn’t one for what you want to do, then you might be out of luck.

You should use the mb\_internal\_encoding\(\) function at the top of every PHP script you write \(or at the top of your global include script\), and the mb\_http\_output\(\) function right after it if your script is outputting to a browser. Explicitly defining the encoding of your strings in every script will save you a lot of headaches down the road.

Additionally, many PHP functions that operate on strings have an optional parameter letting you specify the character encoding. You should always explicitly indicate UTF-8 when given the option. For example, htmlentities\(\) has an option for character encoding, and you should always specify UTF-8 if dealing with such strings. Note that as of PHP 5.4.0, UTF-8 is the default encoding for htmlentities\(\) and htmlspecialchars\(\).

Finally, If you are building an distributed application and cannot be certain that the mbstring extension will be enabled, then consider using the [patchwork\/utf8](https://packagist.org/packages/patchwork/utf8) Composer package. This will use mbstring if it is available, and fall back to non UTF-8 functions if not.

### UTF-8 at the Database level

If your PHP script accesses MySQL, there’s a chance your strings could be stored as non-UTF-8 strings in the database even if you follow all of the precautions above.

To make sure your strings go from PHP to MySQL as UTF-8, make sure your database and tables are all set to the utf8mb4 character set and collation, and that you use the utf8mb4 character set in the PDO connection string. See example code below. This is _critically important_.

Note that you must use the utf8mb4 character set for complete UTF-8 support, not the utf8 character set! See Further Reading for why.

### UTF-8 at the browser level

Use the mb\_http\_output\(\) function to ensure that your PHP script outputs UTF-8 strings to your browser.

The browser will then need to be told by the HTTP response that this page should be considered as UTF-8. The historic approach to doing that was to include the [charset &lt;meta&gt; tag](http://htmlpurifier.org/docs/enduser-utf8.html) in your page’s &lt;head&gt; tag. This approach is perfectly valid, but setting the charset in the Content-Type header is actually [much faster](https://developers.google.com/speed/docs/best-practices/rendering#SpecifyCharsetEarly).

`<?php`

`  // Tell PHP that we're using UTF-8 strings until the end of the script`

`  mb_internal_encoding('UTF-8');`

`  // Tell PHP that we'll be outputting UTF-8 to the browser`

`  mb_http_output('UTF-8');`

`  // Our UTF-8 test string`

`  $string = 'Êl síla erin lû e-govaned vîn.';`

`  // Transform the string in some way with a multibyte function`

`  // Note how we cut the string at a non-Ascii character for demonstration purposes`

`  $string = mb_substr($string, 0, 15);`

`  // Connect to a database to store the transformed string`

`  // See the PDO example in this document for more information`

``  // Note the `set names utf8mb4` commmand!``

`  $link = new \PDO(`

`    'mysql:host=your-hostname;dbname=your-db;charset=utf8mb4',`

`    'your-username',`

`    'your-password',`

`    array(`

`      \PDO::ATTR_ERRMODE => \PDO::ERRMODE_EXCEPTION,`

`      \PDO::ATTR_PERSISTENT => false`

`     )`

`  );`



`  // Store our transformed string as UTF-8 in our database`

`  // Your DB and tables are in the utf8mb4 character set and collation, right?`

`  $handle = $link->prepare('insert into ElvishSentences (Id, Body) values (?, ?)');`

`  $handle->bindValue(1, 1, PDO::PARAM_INT);`

`  $handle->bindValue(2, $string);`

`  $handle->execute();`



`  // Retrieve the string we just stored to prove it was stored correctly`

`  $handle = $link->prepare('select * from ElvishSentences where Id = ?');`

`  $handle->bindValue(1, 1, PDO::PARAM_INT);`

`  $handle->execute();`



`  // Store the result into an object that we'll output later in our HTML`

`  $result = $handle->fetchAll(\PDO::FETCH_OBJ);`



`  header('Content-Type: text/html; charset=UTF-8');`

`?>`

`<!doctype html>`

`<html>`

`  <head>`

`    <meta charset="UTF-8">`

`    <title>UTF-8 test page</title>`

`  </head>`

`  <body>`

`    <?php`

`      foreach($result as $row){`

`        print($row->Body); // This should correctly output our transformed UTF-8 string to the browser`

`      }`

`    ?>`

`  </body>`

`</html>`

### Further reading

* [PHP Manual: String Operations](http://php.net/manual/en/language.operators.string.php)
* [PHP Manual: String Functions](http://php.net/manual/en/ref.strings.php)
  * [strpos\(\)](http://php.net/manual/en/function.strpos.php)

  * [strlen\(\)](http://php.net/manual/en/function.strlen.php)

  * [substr\(\)](http://php.net/manual/en/function.substr.php)


* [PHP Manual: Multibyte String Functions](http://php.net/manual/en/ref.mbstring.php)
  * [mb\_strpos\(\)](http://php.net/manual/en/function.mb-strpos.php)

  * [mb\_strlen\(\)](http://php.net/manual/en/function.mb-strlen.php)

  * [mb\_substr\(\)](http://php.net/manual/en/function.mb-substr.php)

  * [mb\_internal\_encoding\(\)](http://php.net/manual/en/function.mb-internal-encoding.php)

  * [mb\_http\_output\(\)](http://php.net/manual/en/function.mb-http-output.php)

  * [htmlentities\(\)](http://php.net/manual/en/function.htmlentities.php)

  * [htmlspecialchars\(\)](http://www.php.net/manual/en/function.htmlspecialchars.php)


* [PHP UTF-8 Cheatsheet](http://blog.loftdigital.com/blog/php-utf-8-cheatsheet)
* [Stack Overflow: What factors make PHP Unicode-incompatible?](http://stackoverflow.com/questions/571694/what-factors-make-php-unicode-incompatible)
* [Stack Overflow: Best practices in PHP and MySQL with international strings](http://stackoverflow.com/questions/140728/best-practices-in-php-and-mysql-with-international-strings)
* [How to support full Unicode in MySQL databases](http://mathiasbynens.be/notes/mysql-utf8mb4)
* [Brining Unicode to PHP with Portable UTF-8](http://www.sitepoint.com/bringing-unicode-to-php-with-portable-utf8/)

