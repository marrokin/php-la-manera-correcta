### ErrorException

PHP is perfectly capable of being an “exception-heavy” programming language, and only requires a few lines of code to make the switch. Basically you can throw your “errors” as “exceptions” using the ErrorException class, which extends the Exception class.

This is a common practice implemented by a large number of modern frameworks such as Symfony and Laravel. By default Laravel will display all errors as exceptions using the [Whoops!](http://filp.github.io/whoops/) package if the app.debug switch is turned on, then hide them if the switch is turned off.

By throwing errors as exceptions in development you can handle them better than the usual result, and if you see an exception during development you can wrap it in a catch statement with specific instructions on how to handle the situation. Each exception you catch instantly makes your application that little bit more robust.

More information on this and details on how to use ErrorException with error handling can be found at [ErrorException Class](http://php.net/manual/es/class.errorexception.php).

* [Error Control Operators](http://php.net/manual/es/language.operators.errorcontrol.php)
* [Predefined Constants for Error Handling](http://www.php.net/manual/es/errorfunc.constants.php)
* [error\_reporting](http://www.php.net/manual/es/function.error-reporting.php)
* [Reporting](http://phpdevenezuela.github.io/#error_reporting)

