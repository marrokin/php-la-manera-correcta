## Compiled Templates

While PHP has evolved into a mature, object oriented language, it [hasn’t improved much](http://fabien.potencier.org/article/34/templating-engines-in-php) as a templating language. Compiled templates, like [Twig](http://twig.sensiolabs.org/) or [Smarty](http://www.smarty.net/)\*, fill this void by offering a new syntax that has been geared specifically to templating. From automatic escaping, to inheritance and simplified control structures, compiled templates are designed to be easier to write, cleaner to read and safer to use. Compiled templates can even be shared across different languages, [Mustache](http://mustache.github.io/) being a good example of this. Since these templates must be compiled there is a slight performance hit, however this is very minimal when proper caching is used.

_\*While Smarty offers automatic escaping, this feature is NOT enabled by default._

