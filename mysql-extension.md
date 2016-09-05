## MySQL Extension

The [mysql](http://php.net/mysql) extension for PHP is no longer in active development, and is [officially deprecated as of PHP 5.5.0](http://php.net/manual/en/migration55.deprecated.php), meaning that it will be removed within the next few releases. If you are using any functions that start with mysql\_\* such as mysql\_connect\(\) and mysql\_query\(\) in your applications then these will simply not be available in later versions of PHP. This means you will be faced with a rewrite at some point down the line, so the best option is to replace mysql usage with [mysqli](http://php.net/mysqli) or [PDO](http://php.net/pdo) in your applications within your own development schedules so you won’t be rushed later on.

**If you are starting from scratch then absolutely do not use the **[**mysql**](http://php.net/mysql)** extension: use the **[**MySQLi extension**](http://php.net/mysqli)**, or use **[**PDO**](http://php.net/pdo)**.**

* [PHP: Choosing an API for MySQL](http://php.net/manual/en/mysqlinfo.api.choosing.php)
* [PDO Tutorial for MySQL Developers](http://wiki.hashphp.org/PDO_Tutorial_for_MySQL_Developers)

