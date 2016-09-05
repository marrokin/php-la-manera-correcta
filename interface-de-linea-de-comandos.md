## Interface de Línea de Comando \(CLI\)

PHP fue creado principalmente para desarrollar aplicaciones web, pero también es muy útil para implementar programas que corren en la interface de línea de comando \(CLI\). Los programas de línea de comando en PHP pueden ayudarle a automatizar tareas comunes como pruebas, despliegues y la administración de aplicaciones.

Los programas CLI en PHP son muy potentes porque el código de la aplicación se puede utilizar directamente sin tener que crear o asegurar un GUI web para su uso. Por esta razón, ¡asegúrese de no colocar sus programas CLI en su directorio raíz público!

Intente correr PHP desde la línea de comando:

`> php -i`

La opción -i imprimirá la configuración de PHP, como sucede con la función [phpinfo](http://php.net/manual/es/function.phpinfo.php). La opción -a habilita una consola interactiva muy similar al IRB de Ruby o a la consola interactiva de Python. Existen varias [opciones de línea de comando](http://www.php.net/manual/es/features.commandline.options.php) que resultan muy útiles. Vamos a escribir un programa simple que imprima “Hola, $nombre” a la línea de comando. Para empezar, vamos a crear un archive llamad hola.php como se muestra enseguida:

`<?php`

`if($argc != 2) {`

`echo "Uso: php hola.php [nombre].\n";`

`exit(1);`

`}`

`$nombre = $argv[1];`

`echo "Hola, $nombre\n";`

PHP hace disponibles dos variables especiales basados en los argumentos que recibe el programa el ser ejecutado. El variable de tipo _entero_ [$argc](http://php.net/manual/es/reserved.variables.argc.php) contiene el _count_ o número de argumentos y el variable de tipo _array_ [$argv](http://php.net/manual/es/reserved.variables.argv.php) contiene el _value_ o valor de cada uno de los argumentos que se pasaron durante la ejecución. El primer argumento siempre es el nombre del archivo del programa PHP, que en este caso es hola.php.

La expresión exit\(\) se puede usar con un número que no es cero para dejarle saber a la consola que el comando ha fallado. [Aquí](http://www.gsp.com/cgi-bin/man.cgi?section=3&topic=sysexits) puede encontrar los códigos de salida más comúnmente usados.

Para ejecutar el programa desde la línea de comando:

`> php hola.php`

Uso: php hola.php \[nombre\]

`> php hola.php mundo`

Hola, mundo

* [Aprenda acerca de la ejecución de PHP desde la línea de comando](http://php.net/manual/es/features.commandline.php)
* [Aprenda como configurar Windows para ejecutar PHP desde la línea de comando](http://www.php.net/manual/es/install.windows.commandline.php)

