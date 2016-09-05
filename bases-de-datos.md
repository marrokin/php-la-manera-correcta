# Databases

Many times your PHP code will use a database to persist information. You have a few options to connect and interact with your database. The recommended option **until PHP 5.1.0** was to use native drivers such as [mysqli](http://php.net/mysqli), [pgsql](http://php.net/pgsql), [mssql](http://php.net/mssql), etc.

Native drivers are great if you are only using _one_ database in your application, but if, for example, you are using MySQL and a little bit of MSSQL, or you need to connect to an Oracle database, then you will not be able to use the same drivers. You’ll need to learn a brand new API for each database — and that can get silly.

## MySQL Extension

The [mysql](http://php.net/mysql) extension for PHP is no longer in active development, and is [officially deprecated as of PHP 5.5.0](http://php.net/manual/en/migration55.deprecated.php), meaning that it will be removed within the next few releases. If you are using any functions that start with mysql\_\* such as mysql\_connect\(\) and mysql\_query\(\) in your applications then these will simply not be available in later versions of PHP. This means you will be faced with a rewrite at some point down the line, so the best option is to replace mysql usage with [mysqli](http://php.net/mysqli) or [PDO](http://php.net/pdo) in your applications within your own development schedules so you won’t be rushed later on.

**If you are starting from scratch then absolutely do not use the **[**mysql**](http://php.net/mysql)** extension: use the **[**MySQLi extension**](http://php.net/mysqli)**, or use **[**PDO**](http://php.net/pdo)**.**

* [PHP: Choosing an API for MySQL](http://php.net/manual/en/mysqlinfo.api.choosing.php)
* [PDO Tutorial for MySQL Developers](http://wiki.hashphp.org/PDO_Tutorial_for_MySQL_Developers)

## PDO Extension

[PDO](http://php.net/pdo) is a database connection abstraction library — built into PHP since 5.1.0 — that provides a common interface to talk with many different databases. For example, you can use basically identical code to interface with MySQL or SQLite:

`// PDO + MySQL`

`$pdo = new PDO('mysql:host=example.com;dbname=database', 'user', 'password');`

`$statement = $pdo->query("SELECT some\_field FROM some\_table");`

`$row = $statement->fetch(PDO::FETCH_ASSOC);`

`echo htmlentities($row['some_field']);`



`// PDO + SQLite`

`$pdo = new PDO('sqlite:/path/db/foo.sqlite');`

`$statement = $pdo->query("SELECT some\_field FROM some\_table");`

`$row = $statement->fetch(PDO::FETCH_ASSOC);`

`echo htmlentities($row['some_field']);`

PDO will not translate your SQL queries or emulate missing features; it is purely for connecting to multiple types of database with the same API.

More importantly, PDO allows you to safely inject foreign input \(e.g. IDs\) into your SQL queries without worrying about database SQL injection attacks. This is possible using PDO statements and bound parameters.

Let’s assume a PHP script receives a numeric ID as a query parameter. This ID should be used to fetch a user record from a database. This is the wrong way to do this:

`<?php`

`  $pdo = new PDO('sqlite:/path/db/users.db');`

`  $pdo->query("SELECT name FROM users WHERE id = " . $_GET['id']); // <-- NO!`

This is terrible code. You are inserting a raw query parameter into a SQL query. This will get you hacked in a heartbeat, using a practice called [SQL Injection](http://wiki.hashphp.org/Validation). Just imagine if a hacker passes in an inventive id parameter by calling a URL like http:\/\/domain.com\/?id=1%3BDELETE+FROM+users. This will set the $\_GET\['id'\] variable to 1;DELETE FROM users which will delete all of your users! Instead, you should sanitize the ID input using PDO bound parameters.

`<?php`

`  $pdo = new PDO('sqlite:/path/db/users.db');`

`  $stmt = $pdo->prepare('SELECT name FROM users WHERE id = :id');`

`  $stmt->bindParam(':id', $_GET['id'], PDO::PARAM_INT); // <-- Automatically sanitized by PDO`

`  $stmt->execute();`

This is correct code. It uses a bound parameter on a PDO statement. This escapes the foreign input ID before it is introduced to the database preventing potential SQL injection attacks.

* [Learn about PDO](http://www.php.net/manual/en/book.pdo.php)

You should also be aware that database connections use up resources and it was not unheard-of to have resources exhausted if connections were not implicitly closed, however this was more common in other languages. Using PDO you can implicitly close the connection by destroying the object by ensuring all remaining references to it are deleted, i.e. set to NULL. If you don’t do this explicitly, PHP will automatically close the connection when your script ends - unless of course you are using persistent connections.

* [Learn about PDO connections](http://php.net/manual/en/pdo.connections.php)

## Interacting with Databases

When developers first start to learn PHP, they often end up mixing their database interaction up with their presentation logic, using code that might look like this:

`<ul>`

`  <?php`

`    foreach ($db->query('SELECT * FROM table') as $row) {`

`      echo "<li>".$row['field1']." - ".$row['field1']."</li>";`

`    }`

`  ?>`

`</ul>`

This is bad practice for all sorts of reasons, mainly that its hard to debug, hard to test, hard to read and it is going to output a lot of fields if you don’t put a limit on there.

While there are many other solutions to doing this - depending on if you prefer [OOP](http://phpdevenezuela.github.io/#object-oriented-programming) or [functional programming](http://phpdevenezuela.github.io/#functional-programming) - there must be some element of separation.

Consider the most basic step:

`<?php`

`  function getAllFoos($db) {`

`    return $db->query('SELECT * FROM table');`

`  }`



`  foreach (getAllFoos($db) as $row) {`

`    echo "<li>".$row['field1']." - ".$row['field1']."</li>"; // BAD!!`

`  }`

That is a good start. Put those two items in two different files and you’ve got some clean separation.

Create a class to place that method in and you have a “Model”. Create a simple .php file to put the presentation logic in and you have a “View”, which is very nearly [MVC](http://code.tutsplus.com/tutorials/mvc-for-noobs--net-10488) - a common OOP architecture for most [frameworks](http://phpdevenezuela.github.io/#frameworks_title).

_**foo.php**_

`<?php`



`  $db = new PDO('mysql:host=localhost;dbname=testdb;charset=utf8mb4', 'username', 'password');`



`  // Make your model available`

`  include 'models/FooModel.php';`



`  // Create an instance`

`  $fooList = new FooModel($db);`



`  // Show the view`

`  include 'views/foo-list.php';`

_**models\/FooModel.php**_

`<?php`

`  class Foo()`

`  {`

`    protected $db;`



`    public function __construct(PDO $db)`

`    {`

`      $this->db = $db;`

`    }`



`    public function getAllFoos() {`

`      return $this->db->query('SELECT * FROM table');`

`    }`

`  }`

_**views\/foo-list.php**_

`<? foreach ($fooList as $row): ?>`

`  <?= $row['field1'] ?> - <?= $row['field1'] ?>`

`<? endforeach ?>`

This is essentially the same as what most modern frameworks are doing, all be it a little more manual. You might not need to do all of that every time, but mixing together too much presentation logic and database interaction can be a real problem if you ever want to [unit-test](http://phpdevenezuela.github.io/#unit-testing) your application.

[PHPBridge](http://phpbridge.org/) have a great resource called [Creating a Data Class](http://phpbridge.org/intro-to-php/creating_a_data_class) which covers a very similar topic, and is great for developers just getting used to the concept of interacting with databases.

### Abstraction Layers

Many frameworks provide their own abstraction layer which may or may not sit on top of PDO. These will often emulate features for one database system that is missing from another by wrapping your queries in PHP methods, giving you actual database abstraction instead of just the connection abstraction that PDO provides. This will of course add a little overhead, but if you are building a portable application that needs to work with MySQL, PostgreSQL and SQLite then a little overhead will be worth it the sake of code cleanliness.

Some abstraction layers have been built using the [PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md) or [PSR-4](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md) namespace standards so can be installed in any application you like:

* [Aura SQL](https://github.com/auraphp/Aura.Sql)
* [Doctrine2 DBAL](http://www.doctrine-project.org/projects/dbal.html)
* [Propel](http://propelorm.org/)
* [ZF2 Db](http://packages.zendframework.com/docs/latest/manual/en/index.html#zend-db)


