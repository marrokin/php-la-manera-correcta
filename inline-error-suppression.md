### Inline Error Suppression

You can also suppress specific errors from being displayed using the Error Control Operator @. You simply put this operator at the beginning an expression, and any error that would be caused as a direct result of the specific expression will be silenced.

`echo @$foo['bar'];`

This will output $foo\['bar'\] if it exists, but will simply return a null and print nothing if the variable $foo or 'bar' key does not exist.

This might seem like a good idea, but due to the way PHP actually handles @ it is incredibly unperformant, and has the unexpected effect of still actually logging the error anyway. If you have this code in a loop that runs 100 times in an instance, and you run that 1 million times, then you’ve got 100 million lines in your logs.

Instead, use the following:

`echo isset($foo['bar']) ? $foo['bar'] : '';`

This will be much quicker, and save filling up your logs with junk. [SitePoint](http://www.sitepoint.com/) go a step further and say you should [never suppress notices](http://www.sitepoint.com/why-suppressing-notices-is-wrong/) with @.

One instance where error suppression might make sense is where fopen\(\) fails to find a file to load. You could check for existence of the file before you try to load it, but if the file is deleted after the check and before the fopen\(\) \(which might sound impossible, but it can happen\) then fopen\(\) will return false _and_ throw an error. This is potentially something PHP should resolve, but is one case where error suppression might seem like the only valid solution.

In a stock PHP system, the behavior of the error control operator is irreversible. There are no configuration settings which allow a suppressed error to be temporarily un-suppressed.

However, [xDebug](http://xdebug.org/docs/basic) has an xdebug.scream ini setting which will disable the error control operator. You can set this via your php.ini file with the following.

`xdebug.scream = On`

`You can also set this value at runtime with the ini_set function`

`ini_set('xdebug.scream', '1')`

The “[Scream](http://www.php.net/manual/es/book.scream.php)” PHP extension offers similar functionality to xDebug’s, although Scream’s ini setting is named scream.enabled.

This is most useful when you’re debugging code and suspect an informative error is suppressed. Use scream with care, and as a temporary debugging tool. There’s lots of PHP library code that may not work with the error control operator disabled.

* [Error Control Operators](http://php.net/manual/es/language.operators.errorcontrol.php)
* [SitePoint](http://www.sitepoint.com/)
* [never suppress notices](http://www.sitepoint.com/why-suppressing-notices-is-wrong/)
* [xDebug](http://xdebug.org/docs/basic)
* [Scream](http://www.php.net/manual/es/book.scream.php)

