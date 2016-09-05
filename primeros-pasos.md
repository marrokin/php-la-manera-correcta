# Primeros pasos

## Use la versión estable actual \(5.6\)

Si está dando sus primeros pasos con PHP, asegúrese de usar con la última versión estable \(current stable\) de [PHP 5.6](http://www.php.net/downloads.php). En los últimos años se ha progresado mucho añadiendo [nuevas y potentes características](http://phpdevenezuela.github.io/php-the-right-way/#language_highlights) a PHP. Aunque la diferencia entre las versiones 5.2 y 5.6 aparenta ser mínima, en realidad la nueva versión representa _grandes_ mejoras en el sistema. Si estás buscando alguna función en particular o su modo de uso, la documentación oficial en [php.net](http://www.php.net/manual/es/) tendrá la respuesta.

## Servidor Web Integrado

Usted puede comenzar a aprender PHP sin tener que instalar y configurar un servidor web completo \(se requiere la versión PHP 5.4\). Para iniciar el servidor integrado se necesita correr el siguiente comando en la terminal desde el directorio raíz de su proyecto:

&gt; php -S localhost:8000

* [Aprenda más acerca del servidor web integrado](http://www.php.net/manual/es/features.commandline.webserver.php)

## Configuración en Mac

El sistema OSX viene previamente configurado con un PHP que normalmente no está actualizado a la versión corriente. El sistema “Lion” viene configurado con PHP 5.3.6, el sistema “Mountain Lion” con la versión 5.3.10 y el sistema “Mavericks” con al versión 5.4.17.

Para actualizar la versión de PHP en el sistema OSX se puede instalar por medio de diferentes [gestores de paquetes](http://www.php.net/manual/en/install.macosx.packages.php), sin embargo, recomendamos el paquete [php-osx by Liip](http://php-osx.liip.ch/).

La otra opción disponible es que [usted compile](http://www.php.net/manual/en/install.macosx.compile.php) el paquete de instalación. En tal caso debe asegurarse de tener la aplicación para desarrollo _Xcode_ o, como sustituto, las herramientas [“Command Line Tools for Xcode”](https://developer.apple.com/downloads) que se pueden descargar directamente del _Mac Developer Center_ de Apple.

También existen paquetes tipo “todo incluido” con un control gráfico de configuración bastante simple, [MAMP](http://www.mamp.info/en/downloads/index.html) o [XAMPP](http://www.apachefriends.org/es/xampp.html). Estos incluyen una configuración de PHP junto con el servidor web Apache y el gestor de base de datos MySQL.

## Configuración en Windows

Hay un sinnúmero de maneras de configurar PHP en el sistema Windows. Usted puede [descargar los binarios](http://phpdevenezuela.github.io/php-the-right-way/php-downloads) y recientemente el paquete de instalación estaba disponible en el formato ‘.msi’. Este paquete de instalación ya no se actualiza y la última versión fue PHP 5.3.0.

Para aprender PHP o el desarrollo local, se puede utilizar el servidor web embebido que viene con la versión PHP 5.4, así no tendrá que preocuparse por configurar un servidor por separado. Ahora bien, si le gustaría disponer de una solución tipo “todo incluido”, que le ofrece un servidor web completo junto con el gestor de base de datos MySQL, entonces herramientas como el [Web Platform Installer](http://www.microsoft.com/web/downloads/platform.aspx), [XAMPP](http://www.apachefriends.org/en/xampp.html) y [WAMP](http://www.wampserver.com/) le ayudaran a configurar un entorno de desarrollo web en Windows más fácilmente y en menos tiempo. Tenga en consideración que estas herramientas son un poco diferentes a las que usara en su sistema de producción, así que tenga cuidado de las diferencias en el entorno de su aplicación si es que la desarrolla en Windows pero la despliega en Linux.

Si necesita correr un sistema de producción en Windows entonces el servidor IIS 7 le ofrecerá un entorno más estable y con el mejor rendimiento. Una herramienta como [phpmanager](http://phpmanager.codeplex.com/) \(un complemento GUI para IIS 7\) le simplificara la gestión y configuración de PHP en este servidor. IIS 7 viene configurado con FastCGI listo para su uso, solo necesita apuntar a PHP como controlador. Para más información y recursos adicionales refiérase a la [área dedicada en iis.net](http://php.iis.net/) para PHP.

