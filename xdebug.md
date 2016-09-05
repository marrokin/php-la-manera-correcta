## XDebug

Es una de las herramientas más útiles en el desarrollo de software, es un depurador o _debugger_. Permite el trazado de ejecución de tu código y monitorear el contenida de la pila de ejecución. XDebug, depurador para PHP, puede ser utilizado por varios IDEs para proveer _Breakpoints_ e inspeccionar la pila de ejecución. También permite que herramientas como PHPUnit y KCacheGrind realicen análisis de cobertura del código.

Si te encuentras en un aprieto, y recurres a _var\_dump\/print\_r_, y sigues sin encontrar la solución - tal ves necesitas usar un depurador.

[Instalar XDebug](http://xdebug.org/docs/install) puede ser complicado, pero una de las características más importantes es la “Depuración Remota” - Si ésta desarrollando su código localmente y después lo prueba dentro de una VM \(Máquina Virtual\) u en otro servidor, la Depuración Remota es la característica que necesitaras habilitar desde un comienzo.

Tradicionalmente, tendrá que modificar su VHost Apache o el archivo .htaccess con los siguientes valores:

`php_value xdebug.remote_host=192.168.?.?`

`php_value xdebug.remote_port=9000`

El “remote host” y el “remote port” corresponderán a su computadora local y el puerto de escucha que usted configuró para su IDE. Ahora solo es cuestión de que ponga su IDE dentro del modo “escuchar conexiones”, y cargue la URL:

http:\/\/your-website.example.com\/index.php?XDEBUG\_SESSION\_START=1

Su IDE ahora interceptará el estado actual de la ejecución de su script, permitiéndole establecer _breakpoints_ y verificar los valores en memoria.

Los depuradores gráficos hacen muy fácil el proceso de recorrer el código, inspeccionar variables, y evaluar el código en tiempo de ejecución. Varios IDE’s tienen integrado o pueden ser integrados vía plugin la depuración gráfica con XDebug. MacGDBp es un GUI de XDebug para Mac y también es gratuito, open-source y stand-alone.

* [Leer más acerca XDebug](http://xdebug.org/docs/)
* [Leer más acerca de MacGDBp](http://www.bluestatic.org/software/macgdbp/) 

