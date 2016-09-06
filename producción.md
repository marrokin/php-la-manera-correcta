### Producción

Para esconder los errores en su entorno de **producción**, configure su archivo php.ini de la siguiente manera:

* display\_errors: Off
* error\_reporting: E\_ALL
* log\_errors: On

Con estas opciones en su entorno de producción, los errores seguirán siendo registrados en los registros de errores de su servidor web, pero no serán mostrados al usuario. Para más información en cuanto a estas opciones, vea el manual de PHP:

* [Error\_reporting](http://www.php.net/manual/es/errorfunc.configuration.php#ini.error-reporting)
* [Display\_errors](http://www.php.net/manual/es/errorfunc.configuration.php#ini.display-errors)
* [Log\_errors](http://www.php.net/manual/es/errorfunc.configuration.php#ini.log-errors)

