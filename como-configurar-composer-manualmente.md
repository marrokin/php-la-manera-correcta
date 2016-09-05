### Como configurar Composer \(manualmente\)

Configurar Composer manualmente requiere técnicas avanzadas. No obstante, hay varias razones por las cuales un desarrollador como usted prefiera configurarlo de esta manera en vez de utilizar la rutina de configuración interactiva. La configuración interactiva verifica su sistema de PHP para asegurar que:

* Está utilizando una versión compatible de PHP
* Los archivos .phar pueden ser ejecutados correctamente
* Tiene suficientes permisos en los directorios
* Algunas extensiones que pueden causar problemas no han sido cargadas
* El archivo php.ini tiene los ajustes necesarios

Ya que la configuración manual no realiza ninguna de estas verificaciones, necesita tomar en consideración si tal funcionamiento es lo que usted desea. De todas maneras, usted puede obtener y configurar Composer manualmente de la siguiente manera:

`curl -s http://getcomposer.org/composer.phar -o $HOME/local/bin/composer`

`chmod +x $HOME/local/bin/composer`

La ruta $HOME\/local\/bin \(o un directorio que usted escoja\) necesita estar en el variable de entorno $PATH. De esta manera, el comando composer estará habilitado en cualquier directorio del sistema.

Cuando se encuentre con instrucciones que le sugieran ejecutar Composer con php composer.phar install, esto se puede sustituir con:

`composer install`

