### SPL Exceptions

The generic Exception class provides very little debugging context for the developer; however, to remedy this, it is possible to create a specialized Exception type by sub-classing the generic Exception class:

`<?php`

`class ValidationException extends Exception {}`

This means you can add multiple catch blocks and handle different Exceptions differently. This can lead to the creation of a _lot_ of custom Exceptions, some of which could have been avoided using the SPL Exceptions provided in the [SPL extension](http://phpdevenezuela.github.io/#standard_php_library).

If for example you use the \_\_call\(\) Magic Method and an invalid method is requested then instead of throwing a standard Exception which is vague, or creating a custom Exception just for that, you could just throw new BadFunctionCallException;.

* [Read about Exceptions](http://php.net/manual/en/language.exceptions.php)
* [Read about SPL Exceptions](http://php.net/manual/en/spl.exceptions.php)
* [Nesting Exceptions In PHP](http://www.brandonsavage.net/exceptional-php-nesting-exceptions-in-php/)
* [Exception Best Practices in PHP 5.3](http://ralphschindler.com/2010/09/15/exception-best-practices-in-php-5-3)

