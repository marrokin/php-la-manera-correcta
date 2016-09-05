### Como Definir y Configurar Dependencias

Primero, se crea un archivo composer.json en el mismo directorio donde se encuentra composer.phar. Enseguida, encontramos un ejemplo que define el paquete [Twig](http://twig.sensiolabs.org) como una dependencia del proyecto:

`{`

`"require": {`

`"twig/twig": "1.8.*"`

`}`

`}`

El siguiente paso es ejecutar Composer desde el directorio raíz de su proyecto:

php composer.phar install

Esto descargara y configurara la dependencia dentro de un directorio llamado vendors\/. Una vez configurado, añada esta línea de código al archivo principal de su aplicación:

`<?php`

`require 'vendor/autoload.php';`

Esta instrucción le dice a su programa que use el cargador automático de Composer para cargar cualquier dependencia que haya configurado. Ahora sus dependencias serán cargadas dinámicamente según su programa las requiera.

* [Aprenda más acerca de Composer](http://getcomposer.org/doc/00-intro.md)

