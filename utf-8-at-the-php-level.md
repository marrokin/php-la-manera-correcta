### UTF-8 at the PHP level

The basic string operations, like concatenating two strings and assigning strings to variables, don’t need anything special for UTF-8. However most string functions, like strpos\(\) and strlen\(\), do need special consideration. These functions often have an mb\_\* counterpart: for example, mb\_strpos\(\) and mb\_strlen\(\). These mb\_\* strings are made available to you via the [Multibyte String Extension](http://php.net/manual/en/book.mbstring.php), and are specifically designed to operate on Unicode strings.

You must use the mb\_\* functions whenever you operate on a Unicode string. For example, if you use substr\(\) on a UTF-8 string, there’s a good chance the result will include some garbled half-characters. The correct function to use would be the multibyte counterpart, mb\_substr\(\).

The hard part is remembering to use the mb\_\* functions at all times. If you forget even just once, your Unicode string has a chance of being garbled during further processing.

Not all string functions have an mb\_\* counterpart. If there isn’t one for what you want to do, then you might be out of luck.

You should use the mb\_internal\_encoding\(\) function at the top of every PHP script you write \(or at the top of your global include script\), and the mb\_http\_output\(\) function right after it if your script is outputting to a browser. Explicitly defining the encoding of your strings in every script will save you a lot of headaches down the road.

Additionally, many PHP functions that operate on strings have an optional parameter letting you specify the character encoding. You should always explicitly indicate UTF-8 when given the option. For example, htmlentities\(\) has an option for character encoding, and you should always specify UTF-8 if dealing with such strings. Note that as of PHP 5.4.0, UTF-8 is the default encoding for htmlentities\(\) and htmlspecialchars\(\).

Finally, If you are building an distributed application and cannot be certain that the mbstring extension will be enabled, then consider using the [patchwork\/utf8](https://packagist.org/packages/patchwork/utf8) Composer package. This will use mbstring if it is available, and fall back to non UTF-8 functions if not.

