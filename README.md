# php la manera correcta {#php-la-manera-correcta}

**Bienvenido**

Hoy en día existe mucha información anticuada acerca de PHP que guía a nuevos programadores por mal camino, propaga las malas prácticas y código inseguro. _PHP: La Manera Correcta_ es una referencia práctica y fácil de entender, los mejores métodos, estándares de código, enlaces a tutoriales autoritativos alrededor de la Web y lo que los contribuyentes consideran como las mejores prácticas en la actualidad.

_No existe una manera canónica de utilizar PHP_. Este sitio tiene como objetivo introducir a los nuevos desarrolladores en PHP a algunos temas que tal vez no descubran hasta que es demasiado tarde, y también ofrecer nuevas ideas a los profesionales experimentados sobre aquellos temas que han estado haciendo durante años sin reconsiderar. Este sitio no le dirá que herramientas utilizar, en su lugar le ofrecerá diferentes opciones, cuando sea posible se le explicarán las diferencias de enfoque y casos de uso.

Consideramos este sitio como un documento vivo que se continuará actualizando con más información útil y ejemplos según se hagan disponibles.

**Traducciones**

_PHP: La Manera Correcta_ ha sido (o muy pronto será) traducido a diferentes lenguajes:

*   [Alemán](http://rwetzlmayr.github.io/php-the-right-way)
*   [Búlgaro](http://bg.phptherightway.com)
*   [Chino (simplificado)](http://wulijun.github.com/php-the-right-way)
*   [Coreano](http://wafe.github.io/php-the-right-way)
*   [Esloveno](http://sl.phptherightway.com/)
*   [Español](http://phpdevenezuela.github.io/php-the-right-way)
*   [Francés](http://eilgin.github.io/php-the-right-way/)
*   [Indonesio](http://id.phptherightway.com/)
*   [Inglés](http://www.phptherightway.com)
*   [Italiano](http://it.phptherightway.com)
*   [Japones](http://ja.phptherightway.com)
*   [Polaco](http://pl.phptherightway.com)
*   [Portugués](http://br.phptherightway.com)
*   [Rumano](https://bgui.github.io/php-the-right-way/)
*   [Ruso](http://getjump.github.io/ru-php-the-right-way)
*   [Thai](https://apzentral.github.io/php-the-right-way/)
*   [Turco](http://hkulekci.github.io/php-the-right-way/)
*   [Ucraniano](http://iflista.github.com/php-the-right-way)

**¿Cómo Colaborar?**

¡Ayuda a que este sitio se convierta en el mejor recurso para nuevos programadores en PHP! [Colabora en GitHub](https://github.com/phpdevenezuela/php-the-right-way/tree/gh-pages)

**¡Corre la voz!**

_PHP: La Manera Correcta_ tiene disponibles _banners_ que puedes usar en tu sitio web. ¡Apoya la causa y hazles saber a nuevos desarrolladores en PHP donde es que pueden encontrar buena información!

**Primeros pasos**

**Use la versión estable actual (5.6)**

Si está dando sus primeros pasos con PHP, asegúrese de usar con la última versión estable (current stable) de [PHP 5.6](http://www.php.net/downloads.php). En los últimos años se ha progresado mucho añadiendo [nuevas y potentes características](http://phpdevenezuela.github.io/php-the-right-way/) a PHP. Aunque la diferencia entre las versiones 5.2 y 5.6 aparenta ser mínima, en realidad la nueva versión representa _grandes_ mejoras en el sistema. Si estás buscando alguna función en particular o su modo de uso, la documentación oficial en [php.net](http://www.php.net/manual/es/) tendrá la respuesta.

**Servidor Web Integrado**

Usted puede comenzar a aprender PHP sin tener que instalar y configurar un servidor web completo (se requiere la versión PHP 5.4). Para iniciar el servidor integrado se necesita correr el siguiente comando en la terminal desde el directorio raíz de su proyecto:

&gt; php -S localhost:8000

*   [Aprenda más acerca del servidor web integrado](http://www.php.net/manual/es/features.commandline.webserver.php)

**Configuración en Mac**

El sistema OSX viene previamente configurado con un PHP que normalmente no está actualizado a la versión corriente. El sistema “Lion” viene configurado con PHP 5.3.6, el sistema “Mountain Lion” con la versión 5.3.10 y el sistema “Mavericks” con al versión 5.4.17.

Para actualizar la versión de PHP en el sistema OSX se puede instalar por medio de diferentes [gestores de paquetes](http://www.php.net/manual/en/install.macosx.packages.php), sin embargo, recomendamos el paquete [php-osx by Liip](http://php-osx.liip.ch/).

La otra opción disponible es que [usted compile](http://www.php.net/manual/en/install.macosx.compile.php) el paquete de instalación. En tal caso debe asegurarse de tener la aplicación para desarrollo _Xcode_ o, como sustituto, las herramientas [“Command Line Tools for Xcode”](https://developer.apple.com/downloads) que se pueden descargar directamente del _Mac Developer Center_ de Apple.

También existen paquetes tipo “todo incluido” con un control gráfico de configuración bastante simple, [MAMP](http://www.mamp.info/en/downloads/index.html) o [XAMPP](http://www.apachefriends.org/es/xampp.html). Estos incluyen una configuración de PHP junto con el servidor web Apache y el gestor de base de datos MySQL.

**Configuración en Windows**

Hay un sinnúmero de maneras de configurar PHP en el sistema Windows. Usted puede [descargar los binarios](http://phpdevenezuela.github.io/php-the-right-way/php-downloads) y recientemente el paquete de instalación estaba disponible en el formato ‘.msi’. Este paquete de instalación ya no se actualiza y la última versión fue PHP 5.3.0.

Para aprender PHP o el desarrollo local, se puede utilizar el servidor web embebido que viene con la versión PHP 5.4, así no tendrá que preocuparse por configurar un servidor por separado. Ahora bien, si le gustaría disponer de una solución tipo “todo incluido”, que le ofrece un servidor web completo junto con el gestor de base de datos MySQL, entonces herramientas como el [Web Platform Installer](http://www.microsoft.com/web/downloads/platform.aspx), [XAMPP](http://www.apachefriends.org/en/xampp.html) y [WAMP](http://www.wampserver.com/) le ayudaran a configurar un entorno de desarrollo web en Windows más fácilmente y en menos tiempo. Tenga en consideración que estas herramientas son un poco diferentes a las que usara en su sistema de producción, así que tenga cuidado de las diferencias en el entorno de su aplicación si es que la desarrolla en Windows pero la despliega en Linux.

Si necesita correr un sistema de producción en Windows entonces el servidor IIS 7 le ofrecerá un entorno más estable y con el mejor rendimiento. Una herramienta como [phpmanager](http://phpmanager.codeplex.com/) (un complemento GUI para IIS 7) le simplificara la gestión y configuración de PHP en este servidor. IIS 7 viene configurado con FastCGI listo para su uso, solo necesita apuntar a PHP como controlador. Para más información y recursos adicionales refiérase a la [área dedicada en iis.net](http://php.iis.net/) para PHP.

**Guía de Estilo de Código**

La comunidad detrás de PHP es enorme y diversa, compuesta de innumerables librerías, armazones de desarrollo (_frameworks_) y componentes. Es común que desarrolladores en PHP escojan de entre estos y los combinen en un solo proyecto. Por eso es importante que el código PHP se adhiera (lo más cerca posible) a un estilo de código común para que se facilite el trabajo de los desarrolladores al combinar una variedad de librerías para sus proyectos.

El [Framework Interop Group](http://www.php-fig.org/) (antes conocido como el ‘PHP Standards Group’) ha propuesto y aprobado una serie de recomendaciones de estilo, conocidas como [PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md), [PSR-1](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md), [PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) y [PSR-4](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md). No deje que los títulos raros lo confundan, estas recomendaciones son simplemente un conjunto de normas que algunos proyectos como Drupal, Zend, CakePHP, phpBB, AWS SDK, FuelPHP, Lithium, y otros han comenzado a adoptar. Usted puede utilizar estas normas en sus propios proyectos o continuar usando su propio estilo.

Sería ideal que escribiera código PHP que se adhiere a uno o más de estos estándares. Puede ser cualquier combinación de PSR, o uno de los estándares de codificación hechos por PEAR o Zend. Esto significa que otros desarrolladores pueden fácilmente leer y trabajar con su código, y las aplicaciones que implementan los componentes puedan tener consistencia incluso cuando trabajen con una gran cantidad de código de terceros.

*   [Lea acerca de PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md)
*   [Lea acerca de PSR-1](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md)
*   [Lea acerca de PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md)
*   [Lea acerca de PSR-4](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md)
*   [Lea acerca de los Estandares de Codificación de PEAR](http://pear.php.net/manual/en/standards.php)
*   [Lea acerca de los Estandares de Codificación de Zend](http://framework.zend.com/wiki/display/ZFDEV2/Coding+Standards)
*   [Lea acerca de los Estandares de Codificación de Symfony](http://symfony.com/doc/current/contributing/code/standards.html)

Puede utilizar [PHP_CodeSniffer](http://pear.php.net/package/PHP_CodeSniffer/) para verificar que su código se apegue a estas recomendaciones, y plugins para editores de texto como [Sublime Text 2](https://github.com/benmatselby/sublime-phpcs) para obtener un análisis en tiempo real.

Utilice [PHP Coding Standards Fixer](http://cs.sensiolabs.org/) de Fabien Potencier para modificar la sintaxis de su código automáticamente y así quede conforme a estos estándares, ahorrándole tiempo y esfuerzo que requeriría arreglar cada problema a mano.

Se prefiere la utilización del idioma Inglés para todos los nombres de símbolos e infraestructura del código. Los comentarios pueden ser escritos e un lenguaje fácilmente legible para todos autores y futuros desarrolladores que trabajaran en la base del código.

**Aspectos Destacados del Lenguaje**

**Paradigmas de Programación**

PHP es un lenguaje flexible y dinámico que permite usar una variedad de técnicas de programación. El lenguaje ha evolucionado dramáticamente a través de los años. Se añadió un modelo de objetos (object-oriented) sólido en la versión 5.0 (2004), funciones anónimas y espacios de nombres (namespaces) en PHP 5.3, y rasgos (traits) en PHP 5.4 (2012).

**Programación Orientada a Objetos**

PHP tiene un conjunto muy completo de aspectos que facilitan la programación orientada a objetos (OOP) que incluye la habilidad de crear clases, clases abstractas, interfaces, herencia, constructores, clonación de objetos, excepciones y mucho más.

*   [Leer más acerca de PHP orientado a objetos](http://www.php.net/manual/es/language.oop5.php)
*   [Leer más acerca de Rasgos](http://www.php.net/manual/es/language.oop5.traits.php)

**Programación Funcional**

PHP tiene la capacidad de declarar funciones de primera clase, en otras palabras, una función puede ser asignada a un variable. Las funciones definidas por el usuario, así como las funciones internas (incluidas), tiene la habilidad de ser referenciadas por un variable e invocadas dinámicamente. Las funciones pueden ser pasadas como argumentos a otras funciones (un aspecto llamado funciones de orden superior) y funciones pueden devolver otras funciones.

La recursividad es un aspecto que le permite a una función a llamarse a sí misma. El lenguaje PHP habilita este tipo de algoritmos, sin embargo, la mayoría del código PHP se enfoca en iteración.

Las funciones anónimas (con soporte para closures) están presentes en PHP desde la versión 5.3 (2009).

En PHP 5.4 se añadió la habilidad para vincular closure al ámbito de un objeto y también se mejoró el soporte de funciones de tipo _callable_ para que puedan intercambiarse con funciones anónimas en casi todos los casos.

*   Continúe leyendo acerca de la [programación funcional en PHP](http://phpdevenezuela.github.io/php-the-right-way/pages/Functional-Programming.html)
*   [Leer acerca de las funciones anónimas](http://www.php.net/manual/es/functions.anonymous.php)
*   [Leer acerca de la clase Closure](http://php.net/manual/es/class.closure.php)
*   [Mas detalles definidos en el RFC de closures](https://wiki.php.net/rfc/closures)
*   [Leer acerca de funciones tipo Callable](http://php.net/manual/es/language.types.callable.php)
*   [Leer acerca de cómo invocar funciones con call_user_func_array](http://php.net/manual/es/function.call-user-func-array.php)

**Programación Meta**

PHP soporta varias formas de programación meta por medio de mecanismos como el API de Reflexión y los Métodos Mágicos. Hay muchos Métodos Mágicos disponibles como __get(), __set(), __clone(), __toString(), __invoke() y más, que permiten a los desarrolladores a conectarse con el funcionamiento de la clase. A menudo desarrolladores en Ruby dicen que a PHP le falta la función de method_missing, sin embargo los aspectos de esta función están disponibles en __call() y __callStatic().

*   [Leer acerca de los Métodos Mágicos](http://php.net/manual/es/language.oop5.magic.php)
*   [Leer acerca de Reflexion](http://www.php.net/manual/es/intro.reflection.php)

**Namespaces**

Como mencionamos anteriormente, la comunidad de PHP tiene muchos desarrolladores creando una gran cantidad de código fuente. Esto quiere decir que existe la posibilidad que dos librerías diferentes utilicen el mismo nombre para una clase en su código. Cuando las dos librerías se usan dentro del mismo namespace esto se denomina como una colisión y puede causar problemas.

Los _Namespaces_ resuelven este problema. Como se describe en el manual de referencia de PHP, los namespaces son similares a los directorios que separan los archivos en el sistema operativo. Dos archivos con el mismo nombre pueden coexistir en directorios separados. Igualmente, dos clases de PHP con el mismo nombre pueden coexistir en namespaces separados, es tan simple como eso.

Es importante que separe su código con un namespace para que pueda ser usado por otros desarrolladores sin la preocupación de que cause conflictos con otras librerías.

Uno de los métodos recomendados para el uso de espacios de nombres se indica en el [PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md), el cual se propone proveer una convención estándar para los archivos, clases y los namespaces, lo cual facilita el intercambio y uso del código en diferentes proyectos.

*   [Leer acerca de los Namespaces](http://php.net/manual/es/language.namespaces.php)
*   [Leer acerca del PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md)

**Librería Estándar de PHP**

La Librería Estándar de PHP (SPL) viene empaquetada con PHP y provee una colección de clases e interfaces compuesta principalmente de clases de estructura de datos (como stack, queue y heap) e iteradores que pueden atravesar estas estructuras de datos o sus propias clases que implementan las interfaces de la SPL.

*   [Leer acerca de la SPL](http://php.net/manual/es/book.spl.php)

**Interface de Línea de Comando (CLI)**

PHP fue creado principalmente para desarrollar aplicaciones web, pero también es muy útil para implementar programas que corren en la interface de línea de comando (CLI). Los programas de línea de comando en PHP pueden ayudarle a automatizar tareas comunes como pruebas, despliegues y la administración de aplicaciones.

Los programas CLI en PHP son muy potentes porque el código de la aplicación se puede utilizar directamente sin tener que crear o asegurar un GUI web para su uso. Por esta razón, ¡asegúrese de no colocar sus programas CLI en su directorio raíz público!

Intente correr PHP desde la línea de comando:

&gt; php -i

La opción -i imprimirá la configuración de PHP, como sucede con la función [phpinfo](http://php.net/manual/es/function.phpinfo.php). La opción -a habilita una consola interactiva muy similar al IRB de Ruby o a la consola interactiva de Python. Existen varias [opciones de línea de comando](http://www.php.net/manual/es/features.commandline.options.php) que resultan muy útiles. Vamos a escribir un programa simple que imprima “Hola, $nombre” a la línea de comando. Para empezar, vamos a crear un archive llamad hola.php como se muestra enseguida:

&lt;?php

if($argc != 2) {

echo &quot;Uso: php hola.php [nombre].\n&quot;;

exit(1);

}

$nombre = $argv[1];

echo &quot;Hola, $nombre\n&quot;;

PHP hace disponibles dos variables especiales basados en los argumentos que recibe el programa el ser ejecutado. El variable de tipo _entero_ [$argc](http://php.net/manual/es/reserved.variables.argc.php) contiene el _count_ o número de argumentos y el variable de tipo _array_ [$argv](http://php.net/manual/es/reserved.variables.argv.php) contiene el _value_ o valor de cada uno de los argumentos que se pasaron durante la ejecución. El primer argumento siempre es el nombre del archivo del programa PHP, que en este caso es hola.php.

La expresión exit() se puede usar con un número que no es cero para dejarle saber a la consola que el comando ha fallado. [Aquí](http://www.gsp.com/cgi-bin/man.cgi?section=3&topic=sysexits) puede encontrar los códigos de salida más comúnmente usados.

Para ejecutar el programa desde la línea de comando:

&gt; php hola.php

Uso: php hola.php [nombre]

&gt; php hola.php mundo

Hola, mundo

*   [Aprenda acerca de la ejecución de PHP desde la línea de comando](http://php.net/manual/es/features.commandline.php)
*   [Aprenda como configurar Windows para ejecutar PHP desde la línea de comando](http://www.php.net/manual/es/install.windows.commandline.php)

**XDebug**

Es una de las herramientas más útiles en el desarrollo de software, es un depurador o _debugger_. Permite el trazado de ejecución de tu código y monitorear el contenida de la pila de ejecución. XDebug, depurador para PHP, puede ser utilizado por varios IDEs para proveer _Breakpoints_ e inspeccionar la pila de ejecución. También permite que herramientas como PHPUnit y KCacheGrind realicen análisis de cobertura del código.

Si te encuentras en un aprieto, y recurres a _var_dump/print_r_, y sigues sin encontrar la solución - tal ves necesitas usar un depurador.

[Instalar XDebug](http://xdebug.org/docs/install) puede ser complicado, pero una de las características más importantes es la “Depuración Remota” - Si ésta desarrollando su código localmente y después lo prueba dentro de una VM (Máquina Virtual) u en otro servidor, la Depuración Remota es la característica que necesitaras habilitar desde un comienzo.

Tradicionalmente, tendrá que modificar su VHost Apache o el archivo .htaccess con los siguientes valores:

php_value xdebug.remote_host=192.168.?.?

php_value xdebug.remote_port=9000

El “remote host” y el “remote port” corresponderán a su computadora local y el puerto de escucha que usted configuró para su IDE. Ahora solo es cuestión de que ponga su IDE dentro del modo “escuchar conexiones”, y cargue la URL:

http://your-website.example.com/index.php?XDEBUG_SESSION_START=1

Su IDE ahora interceptará el estado actual de la ejecución de su script, permitiéndole establecer _breakpoints_ y verificar los valores en memoria.

Los depuradores gráficos hacen muy fácil el proceso de recorrer el código, inspeccionar variables, y evaluar el código en tiempo de ejecución. Varios IDE’s tienen integrado o pueden ser integrados vía plugin la depuración gráfica con XDebug. MacGDBp es un GUI de XDebug para Mac y también es gratuito, open-source y stand-alone.

*   [Leer más acerca XDebug](http://xdebug.org/docs/)
*   [Leer más acerca de MacGDBp](http://www.bluestatic.org/software/macgdbp/)

**Gestión de Dependencias**

Existen un sinnúmero de librerías, armazones de desarrollo (_frameworks_) y componentes de PHP de donde escoger y lo más probable es que su proyecto utilice varios de ellos. A estos se les llama dependencias de proyecto. Hasta muy recientemente, PHP no tenía una manera fácil de gestionar tales dependencias. Aun si usted se hacía cargo de estos manualmente, todavía tendría que mantenerse al tanto de los cargadores automáticos (autoloaders). Ahora ya no es así.

Actualmente hay dos sistemas principales de gestión de paquetes para PHP: Composer y PEAR. ¿Cuál es el adecuado para usted? La respuesta es, ambos.

*   Utilice **Composer** cuando maneje las dependencias de un solo proyecto.
*   Utilice **PEAR** cuando maneje las dependencias de todo el sistema de PHP en su plataforma.

Generalmente, los paquetes de Composer solo estarán disponibles en los proyectos que usted especifique explícitamente, mientras que un paquete de PEAR estaría disponible a todos los proyectos bajo el sistema PHP. Puede que PEAR parezca la propuesta más accesible a primera vista, sin embargo, también existen ventajas al manejar las dependencias con Composer en base al proyecto en que se está trabajando.

**Composer y Packagist**

Composer es un **excelente** gestor de dependencias para PHP. Solo tiene que añadir las dependencias de su proyecto a un archivo llamado composer.json, ejecutar algunos comandos y Composer descargará automáticamente las dependencias para su proyecto y configurará el cargador automático en cuestión de segundos.

Ya existen muchas librerías PHP compatibles con Composer y están listas para que las use en su proyecto. Hay una lista de estos “paquetes” en el sitio [Packagist](http://packagist.org/), que es el repositorio oficial de librerías compatibles con Composer.

**Como configurar Composer**

Se puede instalar Composer local (en el directorio de trabajo actual, aunque esto ya no es recomendable) o globalmente (por ejemplo, en /user/local/bin). Supongamos que usted quiere configurar Composer localmente. Desde el directorio raíz de su proyecto:

curl -s http://getcomposer.org/installer | php

Esto descargará el archivo binario composer.phar. Se puede ejecutar este archivo con php para manejar las dependencias de su proyecto. _Por favor, tenga en cuenta:_ Si ejecuta el código directamente en el intérprete de PHP al mismo tiempo que lo descarga, tenga cuidado de leer el código del programa con anterioridad y confirmar que es seguro.

**Como configurar Composer (manualmente)**

Configurar Composer manualmente requiere técnicas avanzadas. No obstante, hay varias razones por las cuales un desarrollador como usted prefiera configurarlo de esta manera en vez de utilizar la rutina de configuración interactiva. La configuración interactiva verifica su sistema de PHP para asegurar que:

*   Está utilizando una versión compatible de PHP
*   Los archivos .phar pueden ser ejecutados correctamente
*   Tiene suficientes permisos en los directorios
*   Algunas extensiones que pueden causar problemas no han sido cargadas
*   El archivo php.ini tiene los ajustes necesarios

Ya que la configuración manual no realiza ninguna de estas verificaciones, necesita tomar en consideración si tal funcionamiento es lo que usted desea. De todas maneras, usted puede obtener y configurar Composer manualmente de la siguiente manera:

curl -s http://getcomposer.org/composer.phar -o $HOME/local/bin/composer

chmod +x $HOME/local/bin/composer

La ruta $HOME/local/bin (o un directorio que usted escoja) necesita estar en el variable de entorno $PATH. De esta manera, el comando composer estará habilitado en cualquier directorio del sistema.

Cuando se encuentre con instrucciones que le sugieran ejecutar Composer con php composer.phar install, esto se puede sustituir con:

composer install

**Como Definir y Configurar Dependencias**

Primero, se crea un archivo composer.json en el mismo directorio donde se encuentra composer.phar. Enseguida, encontramos un ejemplo que define el paquete [Twig](http://twig.sensiolabs.org) como una dependencia del proyecto:

{

&quot;require&quot;: {

&quot;twig/twig&quot;: &quot;1.8.*&quot;

}

}

El siguiente paso es ejecutar Composer desde el directorio raíz de su proyecto:

php composer.phar install

Esto descargara y configurara la dependencia dentro de un directorio llamado vendors/. Una vez configurado, añada esta línea de código al archivo principal de su aplicación:

&lt;?php

require &#039;vendor/autoload.php&#039;;

Esta instrucción le dice a su programa que use el cargador automático de Composer para cargar cualquier dependencia que haya configurado. Ahora sus dependencias serán cargadas dinámicamente según su programa las requiera.

*   [Aprenda más acerca de Composer](http://getcomposer.org/doc/00-intro.md)

**PEAR**

Otra alternativa para la gestión de paquetes que muchos desarrolladores en PHP prefieren es [PEAR](http://pear.php.net/). Su funcionamiento es muy similar al de Composer y vale la pena investigar más sus aspectos sobresalientes.

[Aprenda acerca de PEAR](http://pear.php.net/).

**Buenas Prácticas**

**Fundamentos**

PHP es un gran lenguaje que permite a cualquier desarrollador producir código de forma rápida y de manera eficiente. Sin embargo, mientras que avanzamos con el lenguaje, a menudo olvidamos (o pasamos por alto) las prácticas básicas que aprendimos al inicio, tomando así atajos o malas prácticas. Para ayudar a combatir este problema común, esta sección tiene como objetivo recordar a los desarrolladores las buenas prácticas dentro de PHP.

*   Continua leyendo acerca de [Los Fundamentos](http://phpdevenezuela.github.io/php-the-right-way/pages/The-Basics.html)

**Fecha y Hora**

PHP dispone de una clase llamada **DateTIme** para asistir en la lectura, escritura, comparación y calculación de la fecha y hora. Existen muchas funciones en PHP relacionadas con la manipulación de la fecha y la hora, sin embargo, la clase **DateTime** provee una mejor interface orientada a objetos para los situaciones más comunes. También tiene la capacidad de utilizar los husos horarios; esta información no se considerará en esta corta introducción.

Para comenzar a trabajar con DateTime primero se convierte la cadena de texto que contiene la fecha y la hora a un objeto con el método de fabricación createFromFormat() o también se puede crear un objeto con new \DateTime que contendrá la fecha y hora actual. Después, puede utilizar el método format() para convertir el objeto DateTime de regreso a una cadena de texto e imprimirla:

&lt;?php

$fecha = &#039;22\. 11\. 1968&#039;;

$inicio = \DateTime::createFromFormat(&#039;d. m. Y&#039;, $fecha);

echo &quot;Fecha de Inicio: &quot; . $inicio-&gt;format(&#039;m/d/Y&#039;) . &quot;\n&quot;;

Se puede utilizar la clase DateInterval para realizar calculaciones con DateTime. La clase DateTime tiene métodos como add() y sub() que requieren que pase un DateInterval como argumento. Nunca escriba código que cuente con el mismo número de segundos en todos los días ya que los ajustes de los husos horarios y el horario de verano (daylight savings time) invalidaría esa suposición. En vez de eso, utilice los intervalos de fechas para hacer sus calculaciones. Para calcular la diferencia entre fechas utilice el método diff(). Este le devolverá un return new DateInterval, lo cual puede ser fácilmente impreso en la pantalla.

&lt;?php

// Crea una copia de $inicio y añade un mes y 6 días

$final = clone $inicio;

$final-&gt;add(new \DateInterval(&#039;P1M6D&#039;));

$diff = $final-&gt;diff($inicio);

echo &quot;Diferencia: &quot; . $diff-&gt;format(&#039;%m mes, %d días (total: %a días)&#039;) . &quot;\n&quot;;

// Diferencia: 1 mes, 6 días (total: 37 días)

Es posible comparar fácilmente los objetos DateTime:

&lt;?php

if($inicio &lt; $final) {

echo &quot;¡El inicio sucede antes que el final!\n&quot;;

}

Este último ejemplo demuestra cómo se utiliza la clase DatePeriod para iterar sobre eventos periódicos. El objeto toma dos objetos DateTime, uno para el inicio y el otro para el final, y el intervalo que define el número de eventos periódicos que se devuelven.

&lt;?php

// Imprimir todos los jueves entre $inicio y $final

$intervaloDePeriodo = \DateInterval::createFromDateString(&#039;first thursday&#039;);

$iteradorDePeriodo = new \DatePeriod($inicio, $intervaloDePeriodo, $final, \DatePeriod::EXCLUDE_START_DATE);

foreach($iteradorDePeriodo as $fecha)

{

// Imprimir cada fecha en el periodo

echo $fecha-&gt;format(&#039;m/d/Y&#039;) . &quot; &quot;;

}

*   [Leer acerca de la clase DateTime](http://php.net/manual/es/book.datetime.php)
*   [Como formatear la fecha](http://php.net/manual/es/function.date.php) (Opciones de los formatos aceptados para una fecha)

**Patrones de Diseño**

Cuando se desarrolla una aplicación es muy bueno utilizar patrones de uso común en su código y patrones para la estructura general de su proyecto. El usar estos patrones ayuda y facilita el manejo de su código y permite a otros desarrolladores a entender fácilmente como es que encajan todas las partes de su aplicación.

Si utiliza un armazón (_framework_) para el desarrollo de su proyecto, entonces la mayor parte del nivel superior de su código estará basado en este armazón, así que muchas de las decisiones ya han sido hechas por usted. Pero todavía depende de usted el escoger los mejores patrones a seguir en el código que desarrolla sobre este armazón. Si, por otro lado, no está utilizando un armazón para desarrollar su aplicación, entonces necesita encontrar los patrones que mejor se adapten al tipo y tamaño de su proyecto.

*   Continúe leyendo acerca de los [Patrones de Diseño](http://phpdevenezuela.github.io/php-the-right-way/pages/Design-Patterns.html)

**Working with UTF-8**

_This section was originally written by_ [_Alex Cabal_](https://alexcabal.com/) _over at_ [_PHP Best Practices_](https://phpbestpractices.org/) _and has been used as the basis for our own UTF-8 advice_.

**There’s no one-liner. Be careful, detailed, and consistent.**

Right now PHP does not support Unicode at a low level. There are ways to ensure that UTF-8 strings are processed OK, but it’s not easy, and it requires digging in to almost all levels of the web app, from HTML to SQL to PHP. We’ll aim for a brief, practical summary.

**UTF-8 at the PHP level**

The basic string operations, like concatenating two strings and assigning strings to variables, don’t need anything special for UTF-8\. However most string functions, like strpos() and strlen(), do need special consideration. These functions often have an mb_* counterpart: for example, mb_strpos() and mb_strlen(). These mb_* strings are made available to you via the [Multibyte String Extension](http://php.net/manual/en/book.mbstring.php), and are specifically designed to operate on Unicode strings.

You must use the mb_* functions whenever you operate on a Unicode string. For example, if you use substr() on a UTF-8 string, there’s a good chance the result will include some garbled half-characters. The correct function to use would be the multibyte counterpart, mb_substr().

The hard part is remembering to use the mb_* functions at all times. If you forget even just once, your Unicode string has a chance of being garbled during further processing.

Not all string functions have an mb_* counterpart. If there isn’t one for what you want to do, then you might be out of luck.

You should use the mb_internal_encoding() function at the top of every PHP script you write (or at the top of your global include script), and the mb_http_output() function right after it if your script is outputting to a browser. Explicitly defining the encoding of your strings in every script will save you a lot of headaches down the road.

Additionally, many PHP functions that operate on strings have an optional parameter letting you specify the character encoding. You should always explicitly indicate UTF-8 when given the option. For example, htmlentities() has an option for character encoding, and you should always specify UTF-8 if dealing with such strings. Note that as of PHP 5.4.0, UTF-8 is the default encoding for htmlentities() and htmlspecialchars().

Finally, If you are building an distributed application and cannot be certain that the mbstring extension will be enabled, then consider using the [patchwork/utf8](https://packagist.org/packages/patchwork/utf8) Composer package. This will use mbstring if it is available, and fall back to non UTF-8 functions if not.

**UTF-8 at the Database level**

If your PHP script accesses MySQL, there’s a chance your strings could be stored as non-UTF-8 strings in the database even if you follow all of the precautions above.

To make sure your strings go from PHP to MySQL as UTF-8, make sure your database and tables are all set to the utf8mb4 character set and collation, and that you use the utf8mb4 character set in the PDO connection string. See example code below. This is _critically important_.

Note that you must use the utf8mb4 character set for complete UTF-8 support, not the utf8 character set! See Further Reading for why.

**UTF-8 at the browser level**

Use the mb_http_output() function to ensure that your PHP script outputs UTF-8 strings to your browser.

The browser will then need to be told by the HTTP response that this page should be considered as UTF-8\. The historic approach to doing that was to include the [charset &lt;meta&gt; tag](http://htmlpurifier.org/docs/enduser-utf8.html) in your page’s &lt;head&gt; tag. This approach is perfectly valid, but setting the charset in the Content-Type header is actually [much faster](https://developers.google.com/speed/docs/best-practices/rendering).

&lt;?php

// Tell PHP that we&#039;re using UTF-8 strings until the end of the script

mb_internal_encoding(&#039;UTF-8&#039;);

// Tell PHP that we&#039;ll be outputting UTF-8 to the browser

mb_http_output(&#039;UTF-8&#039;);

// Our UTF-8 test string

$string = &#039;Êl síla erin lû e-govaned vîn.&#039;;

// Transform the string in some way with a multibyte function

// Note how we cut the string at a non-Ascii character for demonstration purposes

$string = mb_substr($string, 0, 15);

// Connect to a database to store the transformed string

// See the PDO example in this document for more information

// Note the `set names utf8mb4` commmand!

$link = new \PDO(

&#039;mysql:host=your-hostname;dbname=your-db;charset=utf8mb4&#039;,

&#039;your-username&#039;,

&#039;your-password&#039;,

array(

\PDO::ATTR_ERRMODE =&gt; \PDO::ERRMODE_EXCEPTION,

\PDO::ATTR_PERSISTENT =&gt; false

)

);

// Store our transformed string as UTF-8 in our database

// Your DB and tables are in the utf8mb4 character set and collation, right?

$handle = $link-&gt;prepare(&#039;insert into ElvishSentences (Id, Body) values (?, ?)&#039;);

$handle-&gt;bindValue(1, 1, PDO::PARAM_INT);

$handle-&gt;bindValue(2, $string);

$handle-&gt;execute();

// Retrieve the string we just stored to prove it was stored correctly

$handle = $link-&gt;prepare(&#039;select * from ElvishSentences where Id = ?&#039;);

$handle-&gt;bindValue(1, 1, PDO::PARAM_INT);

$handle-&gt;execute();

// Store the result into an object that we&#039;ll output later in our HTML

$result = $handle-&gt;fetchAll(\PDO::FETCH_OBJ);

header(&#039;Content-Type: text/html; charset=UTF-8&#039;);

?&gt;&lt;!doctype html&gt;

&lt;html&gt;

&lt;head&gt;

&lt;meta charset=&quot;UTF-8&quot;&gt;

&lt;title&gt;UTF-8 test page&lt;/title&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;?php

foreach($result as $row){

print($row-&gt;Body); // This should correctly output our transformed UTF-8 string to the browser

}

?&gt;

&lt;/body&gt;

&lt;/html&gt;

**Further reading**

*   [PHP Manual: String Operations](http://php.net/manual/en/language.operators.string.php)
*   [PHP Manual: String Functions](http://php.net/manual/en/ref.strings.php)
    *   [strpos()](http://php.net/manual/en/function.strpos.php)
    *   [strlen()](http://php.net/manual/en/function.strlen.php)
    *   [substr()](http://php.net/manual/en/function.substr.php)
*   [PHP Manual: Multibyte String Functions](http://php.net/manual/en/ref.mbstring.php)
    *   [mb_strpos()](http://php.net/manual/en/function.mb-strpos.php)
    *   [mb_strlen()](http://php.net/manual/en/function.mb-strlen.php)
    *   [mb_substr()](http://php.net/manual/en/function.mb-substr.php)
    *   [mb_internal_encoding()](http://php.net/manual/en/function.mb-internal-encoding.php)
    *   [mb_http_output()](http://php.net/manual/en/function.mb-http-output.php)
    *   [htmlentities()](http://php.net/manual/en/function.htmlentities.php)
    *   [htmlspecialchars()](http://www.php.net/manual/en/function.htmlspecialchars.php)
*   [PHP UTF-8 Cheatsheet](http://blog.loftdigital.com/blog/php-utf-8-cheatsheet)
*   [Stack Overflow: What factors make PHP Unicode-incompatible?](http://stackoverflow.com/questions/571694/what-factors-make-php-unicode-incompatible)
*   [Stack Overflow: Best practices in PHP and MySQL with international strings](http://stackoverflow.com/questions/140728/best-practices-in-php-and-mysql-with-international-strings)
*   [How to support full Unicode in MySQL databases](http://mathiasbynens.be/notes/mysql-utf8mb4)
*   [Brining Unicode to PHP with Portable UTF-8](http://www.sitepoint.com/bringing-unicode-to-php-with-portable-utf8/)

**Dependency Injection**

From [Wikipedia](http://en.wikipedia.org/wiki/Dependency_injection):

Dependency injection is a software design pattern that allows the removal of hard-coded dependencies and makes it possible to change them, whether at run-time or compile-time.

This quote makes the concept sound much more complicated than it actually is. Dependency Injection is providing a component with it’s dependencies either through constructor injection, method calls or the setting of properties. It is that simple.

**Basic Concept**

We can demonstrate the concept with a simple, yet naive example.

Here we have a Database class that requires an adapter to speak to the database. We instantiate the adapter in the constructor and create a hard dependency. This makes testing difficult and means the Database class is very tightly coupled to the adapter.

&lt;?php

namespace Database;

class Database

{

protected $adapter;

public function __construct()

{

$this-&gt;adapter = new MySqlAdapter;

}

}

class MysqlAdapter {}

This code can be refactored to use Dependency Injection and therefore loosen the dependency.

&lt;?php

namespace Database;

class Database

{

protected $adapter;

public function __construct(MySqlAdapter $adapter)

{

$this-&gt;adapter = $adapter;

}

}

class MysqlAdapter {}

Now we are giving the Database class its dependency rather than it creating it itself. We could even create a method that would accept an argument of the dependency and set it that way, or if the $adapter property was public we could set it directly.

**Complex Problem**

If you have ever read about Dependency Injection then you have probably seen the terms _“Inversion of Control”_ or _“Dependency Inversion Principle”_. These are the complex problems that Dependency Injection solves.

**Inversion of Control**

Inversion of Control is as it says, “inverting the control” of a system by keeping organisational control entirely separate from our objects. In terms of Dependency Injection, this means loosening our dependencies by controlling and instantiating them elsewhere in the system.

For years, PHP frameworks have been achieving Inversion of Control, however, the question became, which part of control are you inverting, and where to? For example, MVC frameworks would generally provide a super object or base controller that other controllers must extend to gain access to its dependencies. This **is** Inversion of Control, however, instead of loosening dependencies, this method simply moved them.

Dependency Injection allows us to more elegantly solve this problem by only injecting the dependencies we need, when we need them, without the need for any hard coded dependencies at all.

**Dependency Inversion Principle**

Dependency Inversion Principle is the “D” in the S.O.L.I.D set of object oriented design principles that states one should _“Depend on Abstractions. Do not depend on concretions.”_. Put simply, this means our dependencies should be interfaces/contracts or abstract classes rather than concrete implementations. We can easily refactor the above example to follow this principle.

&lt;?php

namespace Database;

class Database

{

protected $adapter;

public function __construct(AdapterInterface $adapter)

{

$this-&gt;adapter = $adapter;

}

}

interface AdapterInterface {}

class MysqlAdapter implements AdapterInterface {}

There are several benefits to the Database class now depending on an interface rather than a concretion.

Consider that you are working in a team and the adapter is being worked on by a colleague. In our first example, we would have to wait for said colleague to finish the adapter before we could properly mock it for our unit tests. Now that the dependency is an interface/contract we can happily mock that interface knowing that our colleague will build the adapter based on that contract.

An even bigger benefit to this method is that our code is now much more scalable. If a year down the line we decide that we want to migrate to a different type of database, we can write an adapter that implements the original interface and inject that instead, no more refactoring would be required as we can ensure that the adapter follows the contract set by the interface.

**Containers**

The first thing you should understand about Dependency Injection Containers is that they are not the same thing as Dependency Injection. A container is a convenience utility that helps us implement Dependency Injection, however, they can be and often are misused to implement an anti-pattern, Service Location. Injecting a DI container as a Service Locator in to your classes arguably creates a harder dependency on the container than the dependency you are replacing. It also makes your code much less transparent and ultimately harder to test.

Most modern frameworks have their own Dependency Injection Container that allows you to wire your dependencies together through configuration. What this means in practice is that you can write application code that is as clean and de-coupled as the framework it is built on.

**Further Reading**

*   [Learning about Dependency Injection and PHP](http://ralphschindler.com/2011/05/18/learning-about-dependency-injection-and-php)
*   [What is Dependency Injection?](http://fabien.potencier.org/article/11/what-is-dependency-injection)
*   [Dependency Injection: An analogy](http://mwop.net/blog/260-Dependency-Injection-An-analogy.html)
*   [Dependency Injection: Huh?](http://net.tutsplus.com/tutorials/php/dependency-injection-huh/)
*   [Dependency Injection as a tool for testing](http://www.happyaccidents.me/dependency-injection-as-a-tool-for-testing/)

**Databases**

Many times your PHP code will use a database to persist information. You have a few options to connect and interact with your database. The recommended option **until PHP 5.1.0** was to use native drivers such as [mysqli](http://php.net/mysqli), [pgsql](http://php.net/pgsql), [mssql](http://php.net/mssql), etc.

Native drivers are great if you are only using _one_ database in your application, but if, for example, you are using MySQL and a little bit of MSSQL, or you need to connect to an Oracle database, then you will not be able to use the same drivers. You’ll need to learn a brand new API for each database — and that can get silly.

**MySQL Extension**

The [mysql](http://php.net/mysql) extension for PHP is no longer in active development, and is [officially deprecated as of PHP 5.5.0](http://php.net/manual/en/migration55.deprecated.php), meaning that it will be removed within the next few releases. If you are using any functions that start with mysql_* such as mysql_connect() and mysql_query() in your applications then these will simply not be available in later versions of PHP. This means you will be faced with a rewrite at some point down the line, so the best option is to replace mysql usage with [mysqli](http://php.net/mysqli) or [PDO](http://php.net/pdo) in your applications within your own development schedules so you won’t be rushed later on.

**If you are starting from scratch then absolutely do not use the** [**mysql**](http://php.net/mysql) **extension: use the** [**MySQLi extension**](http://php.net/mysqli)**, or use** [**PDO**](http://php.net/pdo)**.**

*   [PHP: Choosing an API for MySQL](http://php.net/manual/en/mysqlinfo.api.choosing.php)
*   [PDO Tutorial for MySQL Developers](http://wiki.hashphp.org/PDO_Tutorial_for_MySQL_Developers)

**PDO Extension**

[PDO](http://php.net/pdo) is a database connection abstraction library — built into PHP since 5.1.0 — that provides a common interface to talk with many different databases. For example, you can use basically identical code to interface with MySQL or SQLite:

// PDO + MySQL

$pdo = new PDO(&#039;mysql:host=example.com;dbname=database&#039;, &#039;user&#039;, &#039;password&#039;);

$statement = $pdo-&gt;query(&quot;SELECT some\_field FROM some\_table&quot;);

$row = $statement-&gt;fetch(PDO::FETCH_ASSOC);

echo htmlentities($row[&#039;some_field&#039;]);

// PDO + SQLite

$pdo = new PDO(&#039;sqlite:/path/db/foo.sqlite&#039;);

$statement = $pdo-&gt;query(&quot;SELECT some\_field FROM some\_table&quot;);

$row = $statement-&gt;fetch(PDO::FETCH_ASSOC);

echo htmlentities($row[&#039;some_field&#039;]);

PDO will not translate your SQL queries or emulate missing features; it is purely for connecting to multiple types of database with the same API.

More importantly, PDO allows you to safely inject foreign input (e.g. IDs) into your SQL queries without worrying about database SQL injection attacks. This is possible using PDO statements and bound parameters.

Let’s assume a PHP script receives a numeric ID as a query parameter. This ID should be used to fetch a user record from a database. This is the wrong way to do this:

&lt;?php

$pdo = new PDO(&#039;sqlite:/path/db/users.db&#039;);

$pdo-&gt;query(&quot;SELECT name FROM users WHERE id = &quot; . $_GET[&#039;id&#039;]); // &lt;-- NO!

This is terrible code. You are inserting a raw query parameter into a SQL query. This will get you hacked in a heartbeat, using a practice called [SQL Injection](http://wiki.hashphp.org/Validation). Just imagine if a hacker passes in an inventive id parameter by calling a URL like http://domain.com/?id=1%3BDELETE+FROM+users. This will set the $_GET[&#039;id&#039;] variable to 1;DELETE FROM users which will delete all of your users! Instead, you should sanitize the ID input using PDO bound parameters.

&lt;?php

$pdo = new PDO(&#039;sqlite:/path/db/users.db&#039;);

$stmt = $pdo-&gt;prepare(&#039;SELECT name FROM users WHERE id = :id&#039;);

$stmt-&gt;bindParam(&#039;:id&#039;, $_GET[&#039;id&#039;], PDO::PARAM_INT); // &lt;-- Automatically sanitized by PDO

$stmt-&gt;execute();

This is correct code. It uses a bound parameter on a PDO statement. This escapes the foreign input ID before it is introduced to the database preventing potential SQL injection attacks.

*   [Learn about PDO](http://www.php.net/manual/en/book.pdo.php)

You should also be aware that database connections use up resources and it was not unheard-of to have resources exhausted if connections were not implicitly closed, however this was more common in other languages. Using PDO you can implicitly close the connection by destroying the object by ensuring all remaining references to it are deleted, i.e. set to NULL. If you don’t do this explicitly, PHP will automatically close the connection when your script ends - unless of course you are using persistent connections.

*   [Learn about PDO connections](http://php.net/manual/en/pdo.connections.php)

**Interacting with Databases**

When developers first start to learn PHP, they often end up mixing their database interaction up with their presentation logic, using code that might look like this:

&lt;ul&gt;

&lt;?php

foreach ($db-&gt;query(&#039;SELECT * FROM table&#039;) as $row) {

echo &quot;&lt;li&gt;&quot;.$row[&#039;field1&#039;].&quot; - &quot;.$row[&#039;field1&#039;].&quot;&lt;/li&gt;&quot;;

}

?&gt;

&lt;/ul&gt;

This is bad practice for all sorts of reasons, mainly that its hard to debug, hard to test, hard to read and it is going to output a lot of fields if you don’t put a limit on there.

While there are many other solutions to doing this - depending on if you prefer [OOP](http://phpdevenezuela.github.io/) or [functional programming](http://phpdevenezuela.github.io/) - there must be some element of separation.

Consider the most basic step:

&lt;?php

function getAllFoos($db) {

return $db-&gt;query(&#039;SELECT * FROM table&#039;);

}

foreach (getAllFoos($db) as $row) {

echo &quot;&lt;li&gt;&quot;.$row[&#039;field1&#039;].&quot; - &quot;.$row[&#039;field1&#039;].&quot;&lt;/li&gt;&quot;; // BAD!!

}

That is a good start. Put those two items in two different files and you’ve got some clean separation.

Create a class to place that method in and you have a “Model”. Create a simple .php file to put the presentation logic in and you have a “View”, which is very nearly [MVC](http://code.tutsplus.com/tutorials/mvc-for-noobs--net-10488) - a common OOP architecture for most [frameworks](http://phpdevenezuela.github.io/).

**foo.php**

&lt;?php

$db = new PDO(&#039;mysql:host=localhost;dbname=testdb;charset=utf8mb4&#039;, &#039;username&#039;, &#039;password&#039;);

// Make your model available

include &#039;models/FooModel.php&#039;;

// Create an instance

$fooList = new FooModel($db);

// Show the view

include &#039;views/foo-list.php&#039;;

**models/FooModel.php**

&lt;?php

class Foo()

{

protected $db;

public function __construct(PDO $db)

{

$this-&gt;db = $db;

}

public function getAllFoos() {

return $this-&gt;db-&gt;query(&#039;SELECT * FROM table&#039;);

}

}

**views/foo-list.php**

&lt;? foreach ($fooList as $row): ?&gt;

&lt;?= $row[&#039;field1&#039;] ?&gt; - &lt;?= $row[&#039;field1&#039;] ?&gt;

&lt;? endforeach ?&gt;

This is essentially the same as what most modern frameworks are doing, all be it a little more manual. You might not need to do all of that every time, but mixing together too much presentation logic and database interaction can be a real problem if you ever want to [unit-test](http://phpdevenezuela.github.io/) your application.

[PHPBridge](http://phpbridge.org/) have a great resource called [Creating a Data Class](http://phpbridge.org/intro-to-php/creating_a_data_class) which covers a very similar topic, and is great for developers just getting used to the concept of interacting with databases.

**Abstraction Layers**

Many frameworks provide their own abstraction layer which may or may not sit on top of PDO. These will often emulate features for one database system that is missing from another by wrapping your queries in PHP methods, giving you actual database abstraction instead of just the connection abstraction that PDO provides. This will of course add a little overhead, but if you are building a portable application that needs to work with MySQL, PostgreSQL and SQLite then a little overhead will be worth it the sake of code cleanliness.

Some abstraction layers have been built using the [PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md) or [PSR-4](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md) namespace standards so can be installed in any application you like:

*   [Aura SQL](https://github.com/auraphp/Aura.Sql)
*   [Doctrine2 DBAL](http://www.doctrine-project.org/projects/dbal.html)
*   [Propel](http://propelorm.org/)
*   [ZF2 Db](http://packages.zendframework.com/docs/latest/manual/en/index.html)

**Plantillas**

Las plantillas proporcionan una manera conveniente de separar el controlador y la lógica de dominio de su lógica de presentación. Las plantillas normalmente contienen el HTML de tu aplicación, pero pueden ser usadas también para otros formatos, como XML. A las plantillas también se les llaman ‘vistas’, que constituyen parte del segundo componente del patrón de arquitectura de software [modelo-vista-controlador](http://phpdevenezuela.github.io/php-the-right-way/pages/Design-Patterns.html) (MVC).

**Benefits**

The main benefit to using templates is the clear separation they create between the presentation logic and the rest of your application. Templates have the sole responsibility of displaying formatted content. They are not responsible for data lookup, persistence or other more complex tasks. This leads to cleaner, more readable code which is especially helpful in a team environment where developers work on the server-side code (controllers, models) and designers work on the client-side code (markup).

Templates also improve the organization of presentation code. Templates are typically placed in a “views” folder, each defined within a single file. This approach encourages code reuse where larger blocks of code are broken into smaller, reusable pieces, often called partials. For example, your site header and footer can each be defined as templates, which are then included before and after each page template.

Finally, depending on the library you use, templates can offer more security by automatically escaping user-generated content. Some libraries even offer sand-boxing, where template designers are only given access to white-listed variables and functions.

**Plain PHP Templates**

Plain PHP templates are simply templates that use native PHP code. They are a natural choice since PHP is actually a template language itself. That simply means that you can combine PHP code within other code, like HTML. This is beneficial to PHP developers as there is no new syntax to learn, they know the functions available to them, and their code editors already have PHP syntax highlighting and auto-completion built-in. Further, plain PHP templates tend to be very fast as no compiling stage is required.

Every modern PHP framework employs some kind of template system, most of which use plain PHP by default. Outside of frameworks, libraries like [Plates](http://platesphp.com/) or [Aura.View](https://github.com/auraphp/Aura.View) make working with plain PHP templates easier by offering modern template functionality such as inheritance, layouts and extensions.

**Simple example of a plain PHP template**

Using the [Plates](http://platesphp.com/) library.

&lt;?php // user_profile.php ?&gt;

&lt;?php $this-&gt;insert(&#039;header&#039;, [&#039;title&#039; =&gt; &#039;User Profile&#039;]) ?&gt;

&lt;h1&gt;User Profile&lt;/h1&gt;

&lt;p&gt;Hello, &lt;?=$this-&gt;escape($name)?&gt;&lt;/p&gt;

&lt;?php $this-&gt;insert(&#039;footer&#039;) ?&gt;

**Example of plain PHP templates using inheritance**

Using the [Plates](http://platesphp.com/) library.

&lt;?php // template.php ?&gt;

&lt;html&gt;

&lt;head&gt;

&lt;title&gt;&lt;?=$title?&gt;&lt;/title&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;main&gt;

&lt;?=$this-&gt;section(&#039;content&#039;)?&gt;

&lt;/main&gt;

&lt;/body&gt;

&lt;/html&gt;

&lt;?php // user_profile.php ?&gt;

&lt;?php $this-&gt;layout(&#039;template&#039;, [&#039;title&#039; =&gt; &#039;User Profile&#039;]) ?&gt;

&lt;h1&gt;User Profile&lt;/h1&gt;

&lt;p&gt;Hello, &lt;?=$this-&gt;escape($name)?&gt;&lt;/p&gt;

**Compiled Templates**

While PHP has evolved into a mature, object oriented language, it [hasn’t improved much](http://fabien.potencier.org/article/34/templating-engines-in-php) as a templating language. Compiled templates, like [Twig](http://twig.sensiolabs.org/) or [Smarty](http://www.smarty.net/)*, fill this void by offering a new syntax that has been geared specifically to templating. From automatic escaping, to inheritance and simplified control structures, compiled templates are designed to be easier to write, cleaner to read and safer to use. Compiled templates can even be shared across different languages, [Mustache](http://mustache.github.io/) being a good example of this. Since these templates must be compiled there is a slight performance hit, however this is very minimal when proper caching is used.

_*While Smarty offers automatic escaping, this feature is NOT enabled by default._

**Simple example of a compiled template**

Using the [Twig](http://twig.sensiolabs.org/) library.

{% include &#039;header.html&#039; with {&#039;title&#039;: &#039;User Profile&#039;} %}

&lt;h1&gt;User Profile&lt;/h1&gt;

&lt;p&gt;Hello, {{ name }}&lt;/p&gt;

{% include &#039;footer.html&#039; %}

**Example of compiled templates using inheritance**

Using the [Twig](http://twig.sensiolabs.org/) library.

// template.html

&lt;html&gt;

&lt;head&gt;

&lt;title&gt;{% block title %}{% endblock %}&lt;/title&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;main&gt;

{% block content %}{% endblock %}

&lt;/main&gt;

&lt;/body&gt;

&lt;/html&gt;

// user_profile.html

{% extends &quot;template.html&quot; %}

{% block title %}User Profile{% endblock %}

{% block content %}

&lt;h1&gt;User Profile&lt;/h1&gt;

&lt;p&gt;Hello, {{ name }}&lt;/p&gt;

{% endblock %}

**Further Reading**

**Articles &amp; Tutorials**

*   [Templating Engines in PHP](http://fabien.potencier.org/article/34/templating-engines-in-php)
*   [An Introduction to Views &amp; Templating in CodeIgniter](http://code.tutsplus.com/tutorials/an-introduction-to-views-templating-in-codeigniter--net-25648)
*   [Getting Started With PHP Templating](http://www.smashingmagazine.com/2011/10/17/getting-started-with-php-templating/)
*   [Roll Your Own Templating System in PHP](http://code.tutsplus.com/tutorials/roll-your-own-templating-system-in-php--net-16596)
*   [Master Pages](https://laracasts.com/series/laravel-from-scratch/episodes/7)
*   [Working With Templates in Symfony 2](http://code.tutsplus.com/tutorials/working-with-templates-in-symfony-2--cms-21172)

**Libraries**

*   [Aura.View](https://github.com/auraphp/Aura.View) _(native)_
*   [Blade](http://laravel.com/docs/templates) _(compiled, framework specific)_
*   [Dwoo](http://dwoo.org/) _(compiled)_
*   [Latte](https://github.com/nette/latte) _(compiled)_
*   [Mustache](https://github.com/bobthecow/mustache.php) _(compiled)_
*   [PHPTAL](http://phptal.org/) _(compiled)_
*   [Plates](http://platesphp.com/) _(native)_
*   [Smarty](http://www.smarty.net/) _(compiled)_
*   [Twig](http://twig.sensiolabs.org/) _(compiled)_
*   [Zend\View](http://framework.zend.com/manual/2.3/en/modules/zend.view.quick-start.html) _(native, framework specific)_

**Errors and Exceptions**

**Errors**

In many “exception-heavy” programming languages, whenever anything goes wrong an exception will be thrown. This is certainly a viable way to do things, but PHP is an “exception-light” programming language. While it does have exceptions and more of the core is starting to use them when working with objects, most of PHP itself will try to keep processing regardless of what happens, unless a fatal error occurs.

For example:

$ php -a

php &gt; echo $foo;

Notice: Undefined variable: foo in php shell code on line 1

This is only a notice error, and PHP will happily carry on. This can be confusing for those coming from “exception-heavy” languages, because referencing a missing variable in Python for example will throw an exception:

$ python

&gt;&gt;&gt; print foo

Traceback (most recent call last):

File &quot;&lt;stdin&gt;&quot;, line 1, in &lt;module&gt;

NameError: name &#039;foo&#039; is not defined

The only real difference is that Python will freak out over any small thing, so that developers can be super sure any potential issue or edge-case is caught, whereas PHP will keep on processing unless something extreme happens, at which point it will throw an error and report it.

**Error Severity**

PHP has several levels of error severity. The three most common types of messages are errors, notices and warnings. These have different levels of severity; E_ERROR, E_NOTICE, and E_WARNING. Errors are fatal run-time errors and are usually caused by faults in your code and need to be fixed as they’ll cause PHP to stop executing. Warnings are non-fatal errors, execution of the script will not be halted. Notices are advisory messages caused by code that may or may not cause problems during the execution of the script, execution is not halted.

Another type of error message reported at compile time are E_STRICT messages. These messages are used to suggest changes to your code to help ensure best interoperability and forward compatibility with upcoming versions of PHP.

**Changing PHP’s Error Reporting Behaviour**

Error Reporting can be changed by using PHP settings and/or PHP function calls. Using the built in PHP function error_reporting() you can set the level of errors for the duration of the script execution by passing one of the predefined error level constants, meaning if you only want to see Warnings and Errors - but not Notices - then you can configure that:

error_reporting(E_ERROR | E_WARNING);

You can also control whether or not errors are displayed to the screen (good for development) or hidden, and logged (good for production). For more information on this check out the [Error Reporting](http://phpdevenezuela.github.io/) section.

**Inline Error Suppression**

You can also suppress specific errors from being displayed using the Error Control Operator @. You simply put this operator at the beginning an expression, and any error that would be caused as a direct result of the specific expression will be silenced.

echo @$foo[&#039;bar&#039;];

This will output $foo[&#039;bar&#039;] if it exists, but will simply return a null and print nothing if the variable $foo or &#039;bar&#039; key does not exist.

This might seem like a good idea, but due to the way PHP actually handles @ it is incredibly unperformant, and has the unexpected effect of still actually logging the error anyway. If you have this code in a loop that runs 100 times in an instance, and you run that 1 million times, then you’ve got 100 million lines in your logs.

Instead, use the following:

echo isset($foo[&#039;bar&#039;]) ? $foo[&#039;bar&#039;] : &#039;&#039;;

This will be much quicker, and save filling up your logs with junk. [SitePoint](http://www.sitepoint.com/) go a step further and say you should [never suppress notices](http://www.sitepoint.com/why-suppressing-notices-is-wrong/) with @.

One instance where error suppression might make sense is where fopen() fails to find a file to load. You could check for existence of the file before you try to load it, but if the file is deleted after the check and before the fopen() (which might sound impossible, but it can happen) then fopen() will return false _and_ throw an error. This is potentially something PHP should resolve, but is one case where error suppression might seem like the only valid solution.

In a stock PHP system, the behavior of the error control operator is irreversible. There are no configuration settings which allow a suppressed error to be temporarily un-suppressed.

However, [xDebug](http://xdebug.org/docs/basic) has an xdebug.scream ini setting which will disable the error control operator. You can set this via your php.ini file with the following.

xdebug.scream = On

You can also set this value at runtime with the ini_set function

ini_set(&#039;xdebug.scream&#039;, &#039;1&#039;)

The “[Scream](http://www.php.net/manual/es/book.scream.php)” PHP extension offers similar functionality to xDebug’s, although Scream’s ini setting is named scream.enabled.

This is most useful when you’re debugging code and suspect an informative error is suppressed. Use scream with care, and as a temporary debugging tool. There’s lots of PHP library code that may not work with the error control operator disabled.

*   [Error Control Operators](http://php.net/manual/es/language.operators.errorcontrol.php)
*   [SitePoint](http://www.sitepoint.com/)
*   [never suppress notices](http://www.sitepoint.com/why-suppressing-notices-is-wrong/)
*   [xDebug](http://xdebug.org/docs/basic)
*   [Scream](http://www.php.net/manual/es/book.scream.php)

**ErrorException**

PHP is perfectly capable of being an “exception-heavy” programming language, and only requires a few lines of code to make the switch. Basically you can throw your “errors” as “exceptions” using the ErrorException class, which extends the Exception class.

This is a common practice implemented by a large number of modern frameworks such as Symfony and Laravel. By default Laravel will display all errors as exceptions using the [Whoops!](http://filp.github.io/whoops/) package if the app.debug switch is turned on, then hide them if the switch is turned off.

By throwing errors as exceptions in development you can handle them better than the usual result, and if you see an exception during development you can wrap it in a catch statement with specific instructions on how to handle the situation. Each exception you catch instantly makes your application that little bit more robust.

More information on this and details on how to use ErrorException with error handling can be found at [ErrorException Class](http://php.net/manual/es/class.errorexception.php).

*   [Error Control Operators](http://php.net/manual/es/language.operators.errorcontrol.php)
*   [Predefined Constants for Error Handling](http://www.php.net/manual/es/errorfunc.constants.php)
*   [error_reporting](http://www.php.net/manual/es/function.error-reporting.php)
*   [Reporting](http://phpdevenezuela.github.io/)

**Exceptions**

Exceptions are a standard part of most popular programming languages, but they are often overlooked by PHP programmers. Languages like Ruby are extremely Exception heavy, so whenever something goes wrong such as a HTTP request failing, or a DB query goes wrong, or even if an image asset could not be found, Ruby (or the gems being used) will throw an exception to the screen meaning you instantly know there is a mistake.

PHP itself is fairly lax with this, and a call to file_get_contents() will usually just get you a FALSE and a warning. Many older PHP frameworks like CodeIgniter will just return a false, log a message to their proprietary logs and maybe let you use a method like $this-&gt;upload-&gt;get_error() to see what went wrong. The problem here is that you have to go looking for a mistake and check the docs to see what the error method is for this class, instead of having it made extremely obvious.

Another problem is when classes automatically throw an error to the screen and exit the process. When you do this you stop another developer from being able to dynamically handle that error. Exceptions should be thrown to make a developer aware of an error; they then can choose how to handle this. E.g.:

&lt;?php

$email = new Fuel\Email;

$email-&gt;subject(&#039;My Subject&#039;);

$email-&gt;body(&#039;How the heck are you?&#039;);

$email-&gt;to(&#039;guy@example.com&#039;, &#039;Some Guy&#039;);

try

{

$email-&gt;send();

}

catch(Fuel\Email\ValidationFailedException $e)

{

// The validation failed

}

catch(Fuel\Email\SendingFailedException $e)

{

// The driver could not send the email

}

finally

{

// Executed regardless of whether an exception has been thrown, and before normal execution resumes

}

**SPL Exceptions**

The generic Exception class provides very little debugging context for the developer; however, to remedy this, it is possible to create a specialized Exception type by sub-classing the generic Exception class:

&lt;?php

class ValidationException extends Exception {}

This means you can add multiple catch blocks and handle different Exceptions differently. This can lead to the creation of a _lot_ of custom Exceptions, some of which could have been avoided using the SPL Exceptions provided in the [SPL extension](http://phpdevenezuela.github.io/).

If for example you use the __call() Magic Method and an invalid method is requested then instead of throwing a standard Exception which is vague, or creating a custom Exception just for that, you could just throw new BadFunctionCallException;.

*   [Read about Exceptions](http://php.net/manual/en/language.exceptions.php)
*   [Read about SPL Exceptions](http://php.net/manual/en/spl.exceptions.php)
*   [Nesting Exceptions In PHP](http://www.brandonsavage.net/exceptional-php-nesting-exceptions-in-php/)
*   [Exception Best Practices in PHP 5.3](http://ralphschindler.com/2010/09/15/exception-best-practices-in-php-5-3)

**Seguridad**

**Seguridad en Aplicaciones Web**

Es importante reconocer que existen individuos sin escrúpulos que buscan explotar e inhabilitar su aplicación web. Por esta razón es imperativo que tome las precauciones necesarias y trabaje en mejorar la seguridad de su proyecto. Afortunadamente, la comunidad del [The Open Web Application Security Project](https://www.owasp.org/index.php?title=Main_Page&setlang=es) (OWASP) han compilado una lista completa de problemas de seguridad conocidos y los métodos que puede seguir para protegerse contra ellos. Esta guía es lectura obligada para cualquier desarrollador consciente de la seguridad en su aplicación.

*   [Leer la Guía de seguridad de OWASP](https://www.owasp.org/index.php?title=Guide_Table_of_Contents&setlang=es) (Disponible solo en inglés)

**Hash de contraseñas**

Con el tiempo todo el mundo desarrolla una aplicación PHP que se apoya en la conexión del usuario. Los nombres de usuario y las contraseñas se almacenan en una base de datos y posteriormente son utilizados para autenticar a los usuarios en el login.

Es importante que usted [realice hash](https://es.wikipedia.org/wiki/Funci%C3%B3n_hash_criptogr%C3%A1fica) de las contraseñas correctamente antes de almacenarlos. Una vez realizado el hash a la contraseña con una función aplicada contra la contraseña del usuario, el paso es irreversible. Esto produce una cadena de longitud fija que no puede ser revertida factiblemente. Esto significa que puede comparar un hash contra otro para determinar si ambos proceden de la misma cadena de origen, pero no se puede determinar la cadena original. Si las contraseñas no están hasheadas y se accede a la base de datos por un tercero no autorizado, todas las cuentas de usuario están comprometidas. Algunos usuarios pueden (por desgracia) utilizar la misma contraseña para otros servicios. Por lo tanto, es importante tomar en serio la seguridad.

**Hash de contraseñas con password_hash**

En PHP 5.5 fue introducido password_hash. En este momento está usando BCrypt, el algoritmo más fuerte actualmente soportado por PHP. Se actualizará en el futuro para apoyar a más algoritmos, según sea necesario. La librería password_compat fue creada para proveer compatibilidad a las versiones PHP &gt;= 5.3.7.

Más abajo hacemos hash a una cadena de texto, y seguidamente comprobamos el hash con una nueva cadena. Debido a que las fuentes de nuestras dos cadenas son distintas (‘contraseña-secreta’ vs ‘mala-contraseña’) el login fallará.

&lt;?php

require &#039;password.php&#039;;

$passwordHash = password_hash(&#039;contraseña-secreta&#039;, PASSWORD_DEFAULT);

if (password_verify(&#039;mala-contraseña&#039;, $passwordHash)) {

// Contraseña correcta

} else {

// Contraseña incorrecta

}

*   [Aprende más acerca de password_hash](http://es.php.net/manual/es/function.password-hash.php)
*   [password_compat para PHP &gt;= 5.3.7 &amp;&amp; &lt; 5.5](https://github.com/ircmaxell/password_compat)
*   [Obtener información acerca de hashing en cuanto a la criptografía](https://es.wikipedia.org/wiki/Funci%C3%B3n_hash_criptogr%C3%A1fica)
*   [PHP password_hash RFC](https://wiki.php.net/rfc/password_hash)

**Filtrado de Datos**

Nunca, jamás, se confíe de los datos que provienen del exterior de su aplicación PHP. Siempre sanee y verifique los datos de entrada antes de usarlos en su código. Las funciones filter_var() y filter_input() proporcionan saneamiento de los datos y verifican la validez del formato del texto (por ejemplo, las direcciones de correo electrónico).

Los datos de entrada exteriores pueden contener cualquier cosa: los datos provenientes de formularios en $_GET y $_POST, algunos valores provenientes del súper global $_SERVER, el cuerpo de la solicitud HTTP vía la función fopen(&#039;php://input&#039;, &#039;r&#039;). Recuerde que la entrada exterior de datos no está limitada a los datos que provienen de un usuario a través de un formulario, también provienen de la subida y descarga de archivos, valores de sesión, datos de cookies, y los servicios web exteriores.

Aunque los datos que provienen del exterior pueden ser guardados, combinados y se puede acceder a ellos posteriormente, todavía siguen siendo datos exteriores. Cada vez que procesa, imprime, concatena, o los incluye con otros datos en su código, pregúntese si los datos han sido filtrados apropiadamente y si es confiable.

Los datos pueden ser _filtrados_ de diferente manera dependiendo de su proposito. Por ejemplo, cuando se pasan datos sin filtrar a la salida de HTML de su página, corre el riesgo de ejecutar código sin verificar de HTML o JavaScript en su sitio. Esto es conocido (en inglés) como Cross-Site Scripting (XSS), y puede causar mucho daño a su aplicación. Una manera de prevenir estos ataques es sanear todas las etiquetas de HTML en sus datos de entrada al remover etiquetas o convirtiéndolas en entidades de HTML.

Otro ejemplo es cuando se pasan opciones que van a ser ejecutadas en la línea de comando. Esto puede ser extremadamente peligroso y en general no es una buena idea. Sin embargo, puede usar la función escapeshellarg que viene incluida en PHP para sanear los argumentos de ejecución de un comando.

Un último ejemplo es el de aceptar la entrada de datos para determinar que archivo se necesita cargar del sistema de archivos. Esto puede ser explotado al cambiar el nombre del archivo a una ruta de archivo diferente. En este caso es necesario remover los caracteres “/”, “../”, [bytes nulos](http://php.net/manual/es/security.filesystem.nullbytes.php) y otros de la ruta de archivo para que no permita cargar archivos escondidos, no públicos, o de otra manera sensitivos.

*   [Aprenda acerca del filtrado de datos](http://www.php.net/manual/es/book.filter.php)
*   [Aprenda acerca de la función filter_var](http://php.net/manual/es/function.filter-var.php)
*   [Aprenda acerca de la función filter_input](http://www.php.net/manual/es/function.filter-input.php)
*   [Aprenda como manipular los bytes nulos](http://php.net/manual/es/security.filesystem.nullbytes.php)

**Saneamiento**

El saneamiento remueve (o evita) los caracteres ilegales o inseguros que provienen de la entrada de datos externa.

Por ejemplo, debería sanear la entrada de datos antes de incluirla en el código HTML o insertarla a una consulta de SQL. Cuando utiliza parámetros consolidados con [PDO](http://phpdevenezuela.github.io/), este saneara la entrada de datos automáticamente.

En veces es requerido que permita que algunas etiquetas de HTML que se consideren inofensivas puedan ser incluidas en la entrada de datos para una página de su sitio. Esto es algo muy difícil de realizar de una manera segura y muchos lo evitan al usar otros estándares de formato de texto más restrictivos como Markdown o BBCode, aunque librerías que proveen una lista blanca de etiquetas como el [HTML Purifier](http://htmlpurifier.org/) se concibieron para este propósito.

[Vea los filtros de saneamiento](http://www.php.net/manual/es/filter.filters.sanitize.php)

**Validación**

La validación asegura que lo que contiene la entrada de datos es lo que usted esperaba. Por ejemplo, quizás desee validar una dirección de correo electrónico, un número telefónico, o la edad de un usuario al procesar una solicitud de registro.

[Vea los filtros de validación](http://www.php.net/manual/es/filter.filters.validate.php)

**Archivos de Configuración**

Cuando esté trabajando con archivos de configuración para su aplicación, las mejores prácticas dictan que utilice uno de los métodos siguientes:

*   Es recomendable que almacene sus archivos de configuración donde no se pueda acceder a ellos directamente por medio del sistema de archivos.
*   Si no tiene otra alternativa más que almacenar sus archivos de configuración en la raíz de documentos de su aplicación, debe adjuntar la extensión.php al nombre de sus archivos. De esta manera, aun si alguien accede a ellos directamente, la información no será impresa en forma de texto a la pantalla.
*   La información en los archivos de configuración debe ser protegida ya sea por medio de codificación o con los permisos de grupo/usuario pertinentes en el sistema de archivos.

**Register Globals**

**NOTA:** Desde el lanzamiento de PHP 5.4, la opción register_globals ha sido eliminada y ya no puede ser utilizada.

Cuando se habilita la opción register_globals en la configuración de PHP, varios tipos de variables (incluidos los de $_POST, $_GET y $_REQUEST) se hacen disponibles en el ámbito global de su aplicación. Esto puede muy fácilmente conducirlo a problemas de seguridad ya que su aplicación no tiene una manera efectiva de verificar de dónde provienen esos datos.

Si está usando una versión de PHP anterior a 4.2.0, tenga en cuenta que corre el riesgo de que esta opción le cause problemas. Desde la versión 4.2.0 en adelante, la opción register_globals viene desactivada. Para garantizar la seguridad de su aplicación, asegúrese de que esta opción **siempre** este desactivada, con el valor “off”, si es que está disponible.

*   [Register_globals en el manual de PHP](http://www.php.net/manual/es/security.globals.php)

**Reporte de Errores**

El registro de errores puede ser muy útil para encontrar los lugares donde existen problemas en su aplicación, pero también puede exponer información acerca de la estructura de su aplicación al exterior. Para proteger efectivamente su aplicación de problemas que pudieran ser causados por la salida de mensajes de error, necesita configurar su servidor de desarrollo de diferente manera que su servidor de producción.

**Desarrollo**

Para mostrar los errores durante el **desarrollo** de su aplicación, configure las siguientes opciones en su archivo php.ini:

*   display_errors: On
*   error_reporting: E_ALL
*   log_errors: On

**Producción**

Para esconder los errores en su entorno de **producción**, configure su archivo php.ini de la siguiente manera:

*   display_errors: Off
*   error_reporting: E_ALL
*   log_errors: On

Con estas opciones en su entorno de producción, los errores seguirán siendo registrados en los registros de errores de su servidor web, pero no serán mostrados al usuario. Para más información en cuanto a estas opciones, vea el manual de PHP:

*   [Error_reporting](http://www.php.net/manual/es/errorfunc.configuration.php)
*   [Display_errors](http://www.php.net/manual/es/errorfunc.configuration.php)
*   [Log_errors](http://www.php.net/manual/es/errorfunc.configuration.php)

**Pruebas**

La creación de pruebas automatizadas para su código PHP es considerada una buena práctica y conduce a aplicaciones sólidamente construidas. Las pruebas automatizadas son una gran herramienta que asegura que su aplicación no sea afectada negativamente al hacer cambios o al añadir nuevas características a su código; estas son ventajas que no se puede ignorar.

Existen diferentes tipos de herramientas (o armazones) para pruebas disponibles en PHP, las cuales tiene enfoques diferentes, pero todas intentan eliminar las pruebas manuales y la necesidad de disponer grandes equipos de Control de Calidad que se encarguen de asegurar que la aplicación sigue trabajando bien cuando introduce nuevos cambios al código.

**Test Driven Development**

From [Wikipedia](http://en.wikipedia.org/wiki/Test-driven_development):

Test-driven development (TDD) is a software development process that relies on the repetition of a very short development cycle: first the developer writes a failing automated test case that defines a desired improvement or new function, then produces code to pass that test and finally refactors the new code to acceptable standards. Kent Beck, who is credited with having developed or ‘rediscovered’ the technique, stated in 2003 that TDD encourages simple designs and inspires confidence

There are several different types of testing that you can do for your application

**Unit Testing**

Unit Testing is a programming approach to ensure functions, classes and methods are working as expected, from the point you build them all the way through the development cycle. By checking values going in and out of various functions and methods, you can make sure the internal logic is working correctly. By using Dependency Injection and building “mock” classes and stubs you can verify that dependencies are correctly used for even better test coverage.

When you create a class or function you should create a unit test for each behavior it must have. At a very basic level you should make sure it errors if you send it bad arguments and make sure it works if you send it valid arguments. This will help ensure that when you make changes to this class or function later on in the development cycle that the old functionality continues to work as expected. The only alternative to this would be var_dump() in a test.php, which is no way to build an application - large or small.

The other use for unit tests is contributing to open source. If you can write a test that shows broken functionality (i.e. fails), then fix it, and show the test passing, patches are much more likely to be accepted. If you run a project which accepts pull requests then you should suggest this as a requirement.

[PHPUnit](http://phpunit.de) is the de-facto testing framework for writing unit tests for PHP applications, but there are several alternatives

*   [atoum](https://github.com/atoum/atoum)
*   [Enhance PHP](https://github.com/Enhance-PHP/Enhance-PHP)
*   [PUnit](http://punit.smf.me.uk/)
*   [SimpleTest](http://simpletest.org)

**Integration Testing**

From [Wikipedia](http://en.wikipedia.org/wiki/Integration_testing):

Integration testing (sometimes called Integration and Testing, abbreviated “I&amp;T”) is the phase in software testing in which individual software modules are combined and tested as a group. It occurs after unit testing and before validation testing. Integration testing takes as its input modules that have been unit tested, groups them in larger aggregates, applies tests defined in an integration test plan to those aggregates, and delivers as its output the integrated system ready for system testing.

Many of the same tools that can be used for unit testing can be used for integration testing as many of the same principles are used.

**Functional Testing**

Sometimes also known as acceptance testing, functional testing consists of using tools to create automated tests that actually use your application instead of just verifying that individual units of code are behaving correctly and that individual units can speak to each other correctly. These tools typically work using real data and simulating actual users of the application.

**Functional Testing Tools**

*   [Selenium](http://seleniumhq.com)
*   [Mink](http://mink.behat.org)
*   [Codeception](http://codeception.com) is a full-stack testing framework that includes acceptance testing tools
*   [Storyplayer](http://datasift.github.io/storyplayer) is a full-stack testing framework that includes support for creating and destroying test environments on demand

**Desarrollo Guiado por Comportamiento**

Existen dos tipos diferentes de Desarrollo Guiado por Comportamiento (BDD, por sus siglas en inglés): SpecBDD y StoryBDD. SpecBDD se enfoca en el comportamiento o funcionamiento técnico o de parte del código, mientras que StoryBDD se enfoca en el funcionamiento de negocios, el comportamiento de las características o las interacciones. PHP proporciona armazones para estos dos tipos de BDD.

Con el StoryBDD, se escriben historias legibles que describen el comportamiento de su aplicación. Estas historias pueden ser ejecutadas como pruebas en contra de su aplicación. El armazón que se utiliza en PHP para StoryBDD se llama Behat, el cual fue inspirado por el proyecto [Cucumber](http://cukes.info/) de Ruby e implementa el Gherking DSL para describir el comportamiento de características.

Con el SpecBDD, se escriben las especificaciones que describen como su código debe de funcionar. En vez de probar una función o método, solo se describe como la función o método se tiene que comportar. PHP ofrece el armazón [PHPSpec](http://www.phpspec.net/) para este propósito. Este armazon fue inspirado por el proyecto [RSpec](http://rspec.info/) de Ruby.

**Enlaces de BDD**

*   [Behat](http://behat.org/) el armazón de StoryBDD para PHP
*   [PHPSpec](http://www.phpspec.net/) el armazón deSpecBDD paraPHP
*   [Codeception](http://www.codeception.com) es un armazón completo para pruebas que utiliza los principios de BDD

**Herramientas Complementarias de Pruebas**

Además de armazones para pruebas individuales y guiados por comportamiento, también existen varios armazones genéricos y librerías auxiliares que son útiles para cualquier enfoque que se tome.

**Enlaces de herramientas**

*   [Selenium](http://seleniumhq.org/) es una herramienta de automatización del navegador que puede ser [integrada a PHPUnit](http://www.phpunit.de/manual/3.1/en/selenium.html)
*   [Mockery](https://github.com/padraic/mockery) es un armazón para objetos de maqueta que puede ser integrado con [PHPUnit](http://phpunit.de/) o [PHPSpec](http://www.phpspec.net/)

**Servidores y Despliegue**

Las aplicaciones PHP se pueden desplegar y ejecutar en servidores web de producción de varias maneras.

**Plataforma como Servicio (PaaS)**

Las aplicaciones PHP se pueden desplegar y ejecutar en servidores web de producción de varias maneras.

PaaS provee la arquitectura adecuada del sistema y la red que se necesitan para ejecutar aplicaciones PHP en la web. Esto significa que no es necesaria una configuración extensa del servidor para lanzar aplicaciones o armazones de PHP.

Recientemente, PaaS se ha convertido en un método muy popular de desplegar, alojar, y ampliar aplicaciones PHP de todos los tamaños. Encontrará una lista de **Proveedores de PHP PaaS** en la [sección de recursos](http://phpdevenezuela.github.io/php-the-right-way/).

**Servidores Virtuales o Dedicados**

Si se siente cómodo trabajando en la administración de sistemas, o está interesado en aprender a hacerlo, entonces los servidores virtuales o dedicados le proporcionaran el control completo del entorno de producción de su aplicación.

**nginx y PHP-FPM**

PHP, via el Gestor de Procesos FastCGI de PHP (FPM, con sus siglas en inglés), hace buen par con el servidor [nginx](http://nginx.org), que es un servidor ligero de alto rendimiento. Utiliza menos memoria que Apache y puede manejar más solicitudes simultáneas. Esto es de especial importancia en servidores que no disponen de mucha memoria.

*   [Leer más sobre nginx](http://nginx.org)
*   [Leer más sobre PHP-FPM](http://php.net/manual/es/install.fpm.php)
*   [Leer más sobre configurar, y asegurar, nginx y PHP-FPM](https://nealpoole.com/blog/2011/04/setting-up-php-fastcgi-and-nginx-dont-trust-the-tutorials-check-your-configuration/)

**Apache y PHP**

PHP y Apache gozan de una larga historia juntos. Apache es muy configurable y tiene muchos [módulos](http://httpd.apache.org/docs/2.4/mod/) disponibles que extienden las características del servidor. Es una elección popular para servidores compartidos y es fácil de configurar armazones de desarrollo y aplicaciones como WordPress para que trabajen en el servidor. Desafortunadamente, Apache utiliza más recursos que nginx y por defecto no está configurado para manejar un alto número de visitantes al mismo tiempo.

Es posible configurar Apache para ejecutar PHP de diferentes maneras. La más común y más fácil de configurar es usando el módulo mod_php5 con el [prefork MPM](http://httpd.apache.org/docs/2.4/mod/prefork.html). Aunque no es el modulo más eficiente en cuanto al uso de la memoria, es el mas fácil de utilizar. Esta opción es la más viable si no está interesado en adentrarse en los aspectos de administrar un servidor. Cabe notar que si usa el módulo mod_php5, tiene que usar el _prefork MPM_.

Alternativamente, si desea sacar más rendimiento y estabilidad de Apache, entones puede tomar ventaja del mismo sistema de FPM que usa nginx y utilizar el [worker MPM](http://httpd.apache.org/docs/2.4/mod/worker.html) o el [event MPM](http://httpd.apache.org/docs/2.4/mod/event.html) con mod_fastcgi o mod_fcgid. Esto le proporcionara una configuración más eficiente en memoria y mucho más rápida, aunque es más difícil de configurar.

*   [Leer más sobre](http://httpd.apache.org/)
*   [Leer más sobre los módulos para Multi-Processing](http://httpd.apache.org/docs/2.4/mod/mpm_common.html)
*   [Leer más sobre mod_fastcgi](http://www.fastcgi.com/mod_fastcgi/docs/mod_fastcgi.html)
*   [Leer más sobre mod_fcgid](http://httpd.apache.org/mod_fcgid/)

**Servidores Compartidos**

PHP es un lenguaje popular gracias a su proliferación en servidores compartidos. Es difícil encontrarse con un servicio de alojamiento que no incluya PHP en sus opciones, sin embargo es importante que sea la versión más nueva. Los servidores compartidos le permiten a varios desarrolladores desplegar sitios web en un solo sistema. La ventaja de esto es que se ha convertido en una mercancía barata. La desventaja es que nunca sabe qué tipo de alboroto crearan sus inquilinos vecinos; La sobrecarga del servidor y los huecos abiertos de seguridad serían sus preocupaciones principales. Por esta razón, es recomendable evitar este tipo de servicios si el presupuesto de su proyecto lo permite.

**Building and Deploying your Application**

If you find yourself doing manual database schema changes or running your tests manually before updating your files (manually), think twice! With every additional manual task needed to deploy a new version of your app, the chances for potentially fatal mistakes increase. Whether you’re dealing with a simple update, a comprehensive build process or even a continuous integration strategy, [build automation](http://en.wikipedia.org/wiki/Build_automation) is your friend.

Among the tasks you might want to automate are:

*   Dependency management
*   Compilation, minification of your assets
*   Running tests
*   Creation of documentation
*   Packaging
*   Deployment

**Build Automation Tools**

Build tools can be described as a collection of scripts that handle common tasks of software deployment. The build tool is not a part of your software, it acts on your software from ‘outside’.

There are many open source tools available to help you with build automation, some are written in PHP others aren’t. This shouldn’t hold you back from using them, if they’re better suited for the specific job. Here are a few examples:

[Phing](http://www.phing.info/) is the easiest way to get started with automated deployment in the PHP world. With Phing you can control your packaging, deployment or testing process from within a simple XML build file. Phing (which is based on [Apache Ant](http://ant.apache.org/)) provides a rich set of tasks usually needed to install or update a web app and can be extended with additional custom tasks, written in PHP.

[Capistrano](https://github.com/capistrano/capistrano/wiki) is a system for _intermediate-to-advanced programmers_ to execute commands in a structured, repeatable way on one or more remote machines. It is pre-configured for deploying Ruby on Rails applications, however people are **successfully deploying PHP systems** with it. Successful use of Capistrano depends on a working knowledge of Ruby and Rake.

Dave Gardner’s blog post [PHP Deployment with Capistrano](http://www.davegardner.me.uk/blog/2012/02/13/php-deployment-with-capistrano/) is a good starting point for PHP developers interested in Capistrano.

[Chef](http://www.opscode.com/chef/) is more than a deployment framework, it is a very powerful Ruby based system integration framework that doesn’t just deploy your app but can build your whole server environment or virtual boxes.

Chef resources for PHP developers:

*   [Three part blog series about deploying a LAMP application with Chef, Vagrant, and EC2](http://www.jasongrimes.org/2012/06/managing-lamp-environments-with-chef-vagrant-and-ec2-1-of-3/)
*   [Chef Cookbook which installs and configures PHP 5.3 and the PEAR package management system](https://github.com/opscode-cookbooks/php)

Further reading:

*   [Automate your project with Apache Ant](http://net.tutsplus.com/tutorials/other/automate-your-projects-with-apache-ant/)
*   [Maven](http://maven.apache.org/), a build framework based on Ant and [how to use it with PHP](http://www.php-maven.org/)

**Continuous Integration**

Continuous Integration is a software development practice where members of a team integrate their work frequently, usually each person integrates at least daily — leading to multiple integrations per day. Many teams find that this approach leads to significantly reduced integration problems and allows a team to develop cohesive software more rapidly.

_– Martin Fowler_

There are different ways to implement continuous integration for PHP. Recently [Travis CI](https://travis-ci.org/) has done a great job of making continuous integration a reality even for small projects. Travis CI is a hosted continuous integration service for the open source community. It is integrated with GitHub and offers first class support for many languages including PHP.

Further reading:

*   [Continuous Integration with Jenkins](http://jenkins-ci.org/)
*   [Continuous Integration with PHPCI](http://www.phptesting.org/)

**Virtualization**

Running your application on different environments in development and production can lead to strange bugs popping up when you go live. It’s also tricky to keep different development environments up to date with the same version for all libraries used when working with a team of developers.

If you are developing on Windows and deploying to Linux (or anything non-Windows) or are developing in a team, you should consider using a virtual machine. This sounds tricky, but besides the widely known virtualization environments like VMware or VirtualBox, there are additional tools that may help you setting up a virtual environment in a few easy steps.

**Vagrant**

[Vagrant](http://vagrantup.com/) helps you building your virtual boxes on top of the known virtual environments and will configure these environments based on a single configuration file. These boxes can be set up manually, or you can use “provisioning” software such as [Puppet](http://www.puppetlabs.com/) or [Chef](http://www.opscode.com/) to do this for you. Provisioning the base box is a great way to ensure that multiple boxes are set up in an identical fashion and removes the need for you to maintain complicated “set up” command lists. You can also “destroy” your base box and recreate it without many manual steps, making it easy to create a “fresh” installation.

Vagrant creates folders for sharing your code between your host and your virtual machine, which means that you can create and edit your files on your host machine and then run the code inside your virtual machine.

**A little help**

If you need a little help to start using Vagrant there are some services that might be useful:

*   [Rove](http://rove.io/): service that allows you to pre-generate typical Vagrant builds, PHP among the options. The provisioning is made with Chef.
*   [Puphpet](https://puphpet.com/): simple GUI to set up virtual machines for PHP development. **Heavily focused in PHP**. Besides local VMs, it can be used to deploy to cloud services as well. The provisioning is made with Puppet.
*   [Protobox](http://getprotobox.com/): is a layer on top of vagrant and a web GUI to setup virtual machines for web development. A single YAML document controls everything that is installed on the virtual machine.
*   [Phansible](http://phansible.com/): provides an easy to use interface that helps you generate Ansible Playbooks for PHP based projects.

**Docker**

Beside using Vagrant, another easy way to get a virtual development or production environment up and running is [Docker](http://docker.com/). Docker helps you to provide Linux containers for all kind of applications. There are many helpful docker images which could provide you with other great services without the need to install these services on your local machine, e.g. MySQL or PostgreSQL and a lot more. Have a look at the [Docker Hub Registry](https://registry.hub.docker.com/) to search a list of available pre-built containers, which you can then run and use in very few steps.

**Example: Runnning your PHP Applications in Docker**

After you [installed docker](https://docs.docker.com/installation/) on your machine, you can start an Apache with PHP support in one step. The following command will download a fully functional Apache installation with the latest PHP version and provide the directory /path/to/your/php/files at http://localhost:8080:

docker run -d --name my-php-webserver -p 8080:80 -v /path/to/your/php/files:/var/www/html/ php:apache

After running docker run your container is initialized and running. If you would like to stop or start your container again, you can use the provided name attribute and simply run docker stop my-php-webserver and docker start my-php-webserver without providing the above mentioned parameters again.

**Learn more about Docker**

The commands mentioned above only show a quick way to run an Apache web server with PHP support but there are a lot more things that you can do with Docker. One of the most important things for PHP developers will be linking your web server to a database instance, for example. How this could be done is well described within the [Docker User Guide](https://docs.docker.com/userguide/).

*   [Docker Website](http://docker.com/)
*   [Docker Installation](https://docs.docker.com/installation/)
*   [Docker Images at the Docker Hub Registry](https://registry.hub.docker.com/)
*   [Docker User Guide](https://docs.docker.com/userguide/)

**Caché**

En sí, PHP es muy rápido, pero pueden surgir embotellamientos cuando realiza conexiones remotas, carga archivos y así por el estilo. Afortunadamente, existen varias herramientas disponibles para acelerar ciertas partes de su aplicación o reducir el número de veces que se ejecutan estas tareas que consumen tanto tiempo.

**Opcode Cache**

When a PHP file is executed, under the hood it is first compiled to opcodes and, only then, the opcodes are executed. If a PHP file is not modified, the opcodes will always be the same. This means that the compilation step is a waste of CPU resources.

This is where opcode caches come in. They prevent redundant compilation by storing opcodes in memory and reusing it on successive calls. Setting up an opcode cache takes a matter of minutes, and your application will speed up significantly. There’s really no reason not to use it.

As of PHP 5.5, there is a built-in opcode cache called [OPcache](http://php.net/manual/en/book.opcache.php). It is also available for earlier versions.

Read more about opcode caches:

*   [OPcache](http://php.net/manual/en/book.opcache.php) (built-in since PHP 5.5)
*   [APC](http://php.net/manual/en/book.apc.php) (PHP 5.4 and earlier)
*   [XCache](http://xcache.lighttpd.net/)
*   [Zend Optimizer+](http://www.zend.com/products/server/) (part of Zend Server package)
*   [WinCache](http://www.iis.net/download/wincacheforphp) (extension for MS Windows Server)
*   [list of PHP accelerators on Wikipedia](http://en.wikipedia.org/wiki/List_of_PHP_accelerators)

**Object Caching**

There are times when it can be beneficial to cache individual objects in your code, such as with data that is expensive to get or database calls where the result is unlikely to change. You can use object caching software to hold these pieces of data in memory for extremely fast access later on. If you save these items to a data store after you retrieve them, then pull them directly from the cache for following requests, you can gain a significant improvement in performance as well as reduce the load on your database servers.

Many of the popular bytecode caching solutions let you cache custom data as well, so there’s even more reason to take advantage of them. APCu, XCache, and WinCache all provide APIs to save data from your PHP code to their memory cache.

The most commonly used memory object caching systems are APCu and memcached. APCu is an excellent choice for object caching, it includes a simple API for adding your own data to its memory cache and is very easy to setup and use. The one real limitation of APCu is that it is tied to the server it’s installed on. Memcached on the other hand is installed as a separate service and can be accessed across the network, meaning that you can store objects in a hyper-fast data store in a central location and many different systems can pull from it.

Note that when running PHP as a (Fast-)CGI application inside your webserver, every PHP process will have its own cache, i.e. APCu data is not shared between your worker processes. In these cases, you might want to consider using memcached instead, as it’s not tied to the PHP processes.

In a networked configuration APCu will usually outperform memcached in terms of access speed, but memcached will be able to scale up faster and further. If you do not expect to have multiple servers running your application, or do not need the extra features that memcached offers then APCu is probably your best choice for object caching.

Example logic using APCu:

&lt;?php

// check if there is data saved as &#039;expensive_data&#039; in cache

$data = apc_fetch(&#039;expensive_data&#039;);

if ($data === false) {

// data is not in cache; save result of expensive call for later use

apc_add(&#039;expensive_data&#039;, $data = get_expensive_data());

}

print_r($data);

Note that prior to PHP 5.5, APC provides both an object cache and a bytecode cache. APCu is a project to bring APC’s object cache to PHP 5.5+, since PHP now has a built-in bytecode cache (OPcache).

Learn more about popular object caching systems:

*   [APCu](https://github.com/krakjoe/apcu)
*   [APC Functions](http://php.net/manual/en/ref.apc.php)
*   [Memcached](http://memcached.org/)
*   [Redis](http://redis.io/)
*   [XCache APIs](http://xcache.lighttpd.net/wiki/XcacheApi)
*   [WinCache Functions](http://www.php.net/manual/en/ref.wincache.php)

**Recursos**

**Directamente de la fuente**

*   [Sitio web de PHP](http://php.net/)
*   [Documentación de PHP](http://www.php.net/manual/es/)

**Gente a seguir**

*   [Rasmus Lerdorf](http://twitter.com/rasmus)
*   [Fabien Potencier](http://twitter.com/fabpot)
*   [Derick Rethans](http://twitter.com/derickr)
*   [Chris Shiflett](http://twitter.com/shiflett)
*   [Sebastian Bergmann](http://twitter.com/s_bergmann)
*   [Matthew Weier O’Phinney](http://twitter.com/weierophinney)
*   [Nikita Popov](http://twitter.com/nikita_ppv)

**Mentores**

*   [phpmentoring.org](http://phpmentoring.org/) - Asesoramiento formal y directo para la comunidad de PHP.

**Proveedores de PHP PaaS**

*   [PagodaBox](https://pagodabox.com/)
*   [PHP Fog](https://phpfog.com/)
*   [Engine Yard Orchestra PHP Platform](http://www.engineyard.com/products/orchestra/)
*   [Red Hat OpenShift Platform](http://www.redhat.com/products/cloud-computing/openshift/)
*   [dotCloud](http://docs.dotcloud.com/services/php/)
*   [AWS Elastic Beanstalk](http://aws.amazon.com/elasticbeanstalk/)
*   [cloudControl](https://www.cloudcontrol.com/)
*   [Windows Azure](http://www.windowsazure.com/)

**Frameworks**

En lugar de reinventar la rueda, muchos desarrolladores de PHP usan **Frameworks** para desarrollar nuevas aplicaciones web. Los Frameworks abstraen mucho del funcionamiento fundamental de la aplicación y proveen interfaces útiles y fáciles de usar para desempeñar tareas comunes.

No es necesario usar un framework en todos sus proyectos. A veces la mejor alternativa es utilizar PHP puro, pero si cree que necesitas un framework hay tres tipos disponibles:

*   Micro Frameworks
*   Frameworks Full-Stack (Completos)
*   Frameworks de Componentes

Los **micro frameworks** son, en esencia, una envoltura para dirigir las solicitudes de HTTP a un controlador o método lo más rápido posible, y en veces incluyen otras librerías para asistir en el desarrollo, tal como envolturas básicas para bases de datos y así por el estilo. Estos frameworks son utilizados en su mayoría para desarrollar servicios remotos de HTTP.

Muchos frameworks añaden un número considerable de funciones y características sobre la base disponible en un micro framework. A estos se les conoce como **frameworks full-stack (completos)**. A menudo, estos frameworks incluyen paquetes ORM para bases de datos, paquetes de autenticación, y otros.

Los **frameworks de componentes** son colecciones de librerías especializadas para un propósito en particular. Los componentes de estos frameworks pueden utilizarse con otras librerías para construir micro frameworks o frameworks full-stack (completos).

*   [Frameworks populares de PHP](https://github.com/codeguy/php-the-right-way/wiki/Frameworks)

**Components**

As mentioned above “Components” are another approach to the common goal of creating, distributing and implementing shared code. Various component repositories exist, the main two of which are:

*   [Packagist](http://phpdevenezuela.github.io/)
*   [PEAR](http://phpdevenezuela.github.io/)

Both of these repositories have command line tools associated with them to help the installation and upgrade processes, and have been explained in more detail in the [Dependency Management](http://phpdevenezuela.github.io/) section.

There are also component-based frameworks, which allow you to use their components with minimal (or no) requirements. For example, you can use the [FuelPHP Validation package](https://github.com/fuelphp/validation), without needing to use the FuelPHP framework itself. These projects are essentially just another repository for reusable components:

*   [Aura](http://auraphp.github.com/)
*   [FuelPHP](https://github.com/fuelphp)
*   [Symfony Components](http://symfony.com/doc/current/components/index.html)
*   [The League of Extraordinary Packages](http://thephpleague.com/)
*   Laravel’s Illuminate Components
    *   [Eloquent ORM](https://github.com/illuminate/database)
    *   [Queue](https://github.com/illuminate/queue)

_Laravel’s_ [_Illuminate components_](https://github.com/illuminate) _will become better decoupled from the Laravel framework. For now, only the components best decoupled from the Laravel framework are listed above._

**Comunidad**

La comunidad de PHP es una comunidad grande y con mucha diversidad. Sus miembros están listos y dispuestos para apoyar a los nuevos programadores en PHP. Usted debería considerar la posibilidad de unirse a un grupo local de usuarios de PHP (PUG, con sus siglas en inglés) o atender una de las conferencias enfocadas en PHP para aprender más acerca de las mejores prácticas expuestas en esta página. También puede asociarse en el canal de IRC, #phpc, disponible en irc.freenode.com y seguir la cuenta de twitter [@phpc](https://twitter.com/phpc). Le exhortamos a que conozca a otros desarrolladores, aprenda más acerca de otros tópicos y, sobre todo, entable nuevas amistades.

[Lea el calendario oficial de eventos de PHP](http://www.php.net/cal.php)

**Grupos de Usuarios de PHP**

Si usted vive en una ciudad grande, es muy probable que exista un grupo de usuarios de PHP cerca. Aunque no existe todavía una lista oficial de estos grupos, si puede encontrar fácilmente un grupo local usando [Google](https://www.google.com/search?q=php+user+group+near+me) o [Meetup.com](http://www.meetup.com/find/). Si usted vive en una ciudad más pequeña, quizás no haya grupos de usuarios locales. Si esa es su situación, ¡lo invitamos a que inicie su propio grupo!

[Lea más acerca de los grupos de usuarios en el wiki de PHP](https://wiki.php.net/usergroups)

**Conferencias de PHP**

La comunidad de PHP también organiza conferencias de ámbito regional y nacional en muchos países alrededor del mundo. Miembros bien conocidos de la comunidad de PHP usualmente tienen intervenciones en estos eventos así que es una buena oportunidad para aprender directamente de estos líderes de la industria.

[Encuentre una conferencia de PHP](http://php.net/conferences/index.php)

**PHPDoc**

PHPDoc is an informal standard for commenting PHP code. There are a _lot_ of different [tags](http://www.phpdoc.org/docs/latest/references/phpdoc/tags/index.html) available. The full list of tags and examples can be found at the [PHPDoc manual](http://www.phpdoc.org/docs/latest/index.html).

Below is an example of how you might document a class with a few methods;

&lt;?php

/**

* @author A Name &lt;a.name@example.com&gt;

* @link http://www.phpdoc.org/docs/latest/index.html

* @package helper

*/

class DateTimeHelper

{

/**

* @param mixed $anything Anything that we can convert to a \DateTime object

*

* @return \DateTime

* @throws \InvalidArgumentException

*/

public function dateTimeFromAnything($anything)

{

$type = gettype($anything);

switch ($type) {

// Some code that tries to return a \DateTime object

}

throw new \InvalidArgumentException(

&quot;Failed Converting param of type &#039;{$type}&#039; to DateTime object&quot;

);

}

/**

* @param mixed $date Anything that we can convert to a \DateTime object

*

* @return void

*/

public function printISO8601Date($date)

{

echo $this-&gt;dateTimeFromAnything($date)-&gt;format(&#039;c&#039;);

}

/**

* @param mixed $date Anything that we can convert to a \DateTime object

*/

public function printRFC2822Date($date)

{

echo $this-&gt;dateTimeFromAnything($date)-&gt;format(&#039;r&#039;);

}

}

The documentation for the class as a whole firstly has the [@author](http://www.phpdoc.org/docs/latest/references/phpdoc/tags/author.html) tag, this tag is used to document the author of the code and can be repeated for documenting several authors. Secondly is the [@link](http://www.phpdoc.org/docs/latest/references/phpdoc/tags/link.html) tag, used to link to a website indicating a relationship between the website and the code. Thirdly it has the [@package](http://www.phpdoc.org/docs/latest/references/phpdoc/tags/package.html) tag, used to categorize the code.

Inside the class, the first method has an [@param](http://www.phpdoc.org/docs/latest/references/phpdoc/tags/param.html) tag documenting the type, name and description of the parameter being passed to the method. Additionally it has the [@return](http://www.phpdoc.org/docs/latest/references/phpdoc/tags/return.html) and [@throws](http://www.phpdoc.org/docs/latest/references/phpdoc/tags/throws.html) tags for documenting the return type, and any exceptions that could be throw respectively.

The second and third methods are very similar and have a single [@param](http://www.phpdoc.org/docs/latest/references/phpdoc/tags/param.html) tag as did the first method. The import difference between the second and third method is doc block is the inclusion/exclusion of the [@return](http://www.phpdoc.org/docs/latest/references/phpdoc/tags/return.html) tag. @return void explicitly informs us that there is no return, historically omitting the @return void statement also results in the same (no return) action.

**Créditos**

**Creado y mantenido por**

*   [Josh Lockhart](http://twitter.com/codeguy)

**Colaboradores del proyecto**

*   [Kris Jordan](http://krisjordan.com/)
*   [Phil Sturgeon](http://philsturgeon.co.uk/)

**Contribuyentes al proyecto**

Este proyecto no ser�a posible sin la ayuda de [nuestros valiosos contribuidores](https://github.com/phpdevenezuela/php-the-right-way/graphs/contributors) en GitHub.

**Patrocinadores del proyecto**

*   [New Media Campaigns](http://www.newmediacampaigns.com)

![Creative Commons License](assets/creative_commons_license.png)PHP: The Right Way by [Josh Lockhart](http://www.twitter.com/codeguy) is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-nc-sa/3.0/).Based on a work at [www.phptherightway.com](http://www.phptherightway.com).