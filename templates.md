# Plantillas

Las plantillas proporcionan una manera conveniente de separar el controlador y la lógica de dominio de su lógica de presentación. Las plantillas normalmente contienen el HTML de tu aplicación, pero pueden ser usadas también para otros formatos, como XML. A las plantillas también se les llaman ‘vistas’, que constituyen parte del segundo componente del patrón de arquitectura de software [modelo-vista-controlador](http://phpdevenezuela.github.io/php-the-right-way/pages/Design-Patterns.html#model-view-controller) \(MVC\).

## Benefits

The main benefit to using templates is the clear separation they create between the presentation logic and the rest of your application. Templates have the sole responsibility of displaying formatted content. They are not responsible for data lookup, persistence or other more complex tasks. This leads to cleaner, more readable code which is especially helpful in a team environment where developers work on the server-side code \(controllers, models\) and designers work on the client-side code \(markup\).

Templates also improve the organization of presentation code. Templates are typically placed in a “views” folder, each defined within a single file. This approach encourages code reuse where larger blocks of code are broken into smaller, reusable pieces, often called partials. For example, your site header and footer can each be defined as templates, which are then included before and after each page template.

Finally, depending on the library you use, templates can offer more security by automatically escaping user-generated content. Some libraries even offer sand-boxing, where template designers are only given access to white-listed variables and functions.

## Plain PHP Templates

Plain PHP templates are simply templates that use native PHP code. They are a natural choice since PHP is actually a template language itself. That simply means that you can combine PHP code within other code, like HTML. This is beneficial to PHP developers as there is no new syntax to learn, they know the functions available to them, and their code editors already have PHP syntax highlighting and auto-completion built-in. Further, plain PHP templates tend to be very fast as no compiling stage is required.

Every modern PHP framework employs some kind of template system, most of which use plain PHP by default. Outside of frameworks, libraries like [Plates](http://platesphp.com/) or [Aura.View](https://github.com/auraphp/Aura.View) make working with plain PHP templates easier by offering modern template functionality such as inheritance, layouts and extensions.

### Simple example of a plain PHP template

Using the [Plates](http://platesphp.com/) library.

`<?php // user_profile.php ?>`

`<?php $this->insert('header', ['title' => 'User Profile']) ?>`

`<h1>User Profile</h1>`

`<p>Hello, <?=$this->escape($name)?></p>`

`<?php $this->insert('footer') ?>`

## Example of plain PHP templates using inheritance

Using the [Plates](http://platesphp.com/) library.

`<?php // template.php ?>`

`<html>`

`  <head>`

`    <title><?=$title?></title>`

`  </head>`

`  <body>`

`    <main>`

`      <?=$this->section('content')?>`

`    </main>`

`  </body>`

`</html>`



`<?php // user_profile.php ?>`

`<?php $this->layout('template', ['title' => 'User Profile']) ?>`

`<h1>User Profile</h1>`

`<p>Hello, <?=$this->escape($name)?></p>`

## Compiled Templates

While PHP has evolved into a mature, object oriented language, it [hasn’t improved much](http://fabien.potencier.org/article/34/templating-engines-in-php) as a templating language. Compiled templates, like [Twig](http://twig.sensiolabs.org/) or [Smarty](http://www.smarty.net/)\*, fill this void by offering a new syntax that has been geared specifically to templating. From automatic escaping, to inheritance and simplified control structures, compiled templates are designed to be easier to write, cleaner to read and safer to use. Compiled templates can even be shared across different languages, [Mustache](http://mustache.github.io/) being a good example of this. Since these templates must be compiled there is a slight performance hit, however this is very minimal when proper caching is used.

_\*While Smarty offers automatic escaping, this feature is NOT enabled by default._

### Simple example of a compiled template

Using the [Twig](http://twig.sensiolabs.org/) library.

`{% include 'header.html' with {'title': 'User Profile'} %}`

`<h1>User Profile</h1>`

`<p>Hello, {{ name }}</p>`

`{% include 'footer.html' %}`

### Example of compiled templates using inheritance

Using the [Twig](http://twig.sensiolabs.org/) library.

`// template.html`

`<html>`

`  <head>`

`    <title>{% block title %}{% endblock %}</title>`

`  </head>`

`  <body>`

`    <main>`

`      {% block content %}{% endblock %}`

`    </main>`

`  </body>`

`</html>`



`// user_profile.html`

`{% extends "template.html" %}`

`{% block title %}User Profile{% endblock %}`

`{% block content %}`

` <h1>User Profile</h1>`

` <p>Hello, {{ name }}</p>`

`{% endblock %}`

## Further Reading

### Articles & Tutorials

* [Templating Engines in PHP](http://fabien.potencier.org/article/34/templating-engines-in-php)
* [An Introduction to Views & Templating in CodeIgniter](http://code.tutsplus.com/tutorials/an-introduction-to-views-templating-in-codeigniter--net-25648)
* [Getting Started With PHP Templating](http://www.smashingmagazine.com/2011/10/17/getting-started-with-php-templating/)
* [Roll Your Own Templating System in PHP](http://code.tutsplus.com/tutorials/roll-your-own-templating-system-in-php--net-16596)
* [Master Pages](https://laracasts.com/series/laravel-from-scratch/episodes/7)
* [Working With Templates in Symfony 2](http://code.tutsplus.com/tutorials/working-with-templates-in-symfony-2--cms-21172)

### Libraries

* [Aura.View](https://github.com/auraphp/Aura.View) _\(native\)_
* [Blade](http://laravel.com/docs/templates) _\(compiled, framework specific\)_
* [Dwoo](http://dwoo.org/) _\(compiled\)_
* [Latte](https://github.com/nette/latte) _\(compiled\)_
* [Mustache](https://github.com/bobthecow/mustache.php) _\(compiled\)_
* [PHPTAL](http://phptal.org/) _\(compiled\)_
* [Plates](http://platesphp.com/) _\(native\)_
* [Smarty](http://www.smarty.net/) _\(compiled\)_
* [Twig](http://twig.sensiolabs.org/) _\(compiled\)_
* [Zend\View](http://framework.zend.com/manual/2.3/en/modules/zend.view.quick-start.html) _\(native, framework specific\)_

