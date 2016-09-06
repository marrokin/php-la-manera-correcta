## Errors

In many “exception-heavy” programming languages, whenever anything goes wrong an exception will be thrown. This is certainly a viable way to do things, but PHP is an “exception-light” programming language. While it does have exceptions and more of the core is starting to use them when working with objects, most of PHP itself will try to keep processing regardless of what happens, unless a fatal error occurs.

For example:

`$ php -a`

`php > echo $foo;`

`Notice: Undefined variable: foo in php shell code on line 1`

This is only a notice error, and PHP will happily carry on. This can be confusing for those coming from “exception-heavy” languages, because referencing a missing variable in Python for example will throw an exception:

`$ python`

`>>> print foo`

`Traceback (most recent call last):`

` File "<stdin>", line 1, in <module>`

`NameError: name 'foo' is not defined`

The only real difference is that Python will freak out over any small thing, so that developers can be super sure any potential issue or edge-case is caught, whereas PHP will keep on processing unless something extreme happens, at which point it will throw an error and report it.

* ### Error Severity

* ### Changing PHP’s Error Reporting Behaviour

* ### Inline Error Suppression

* ### ErrorException


