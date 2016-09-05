## Interacting with Databases

When developers first start to learn PHP, they often end up mixing their database interaction up with their presentation logic, using code that might look like this:

`<ul>`

`<?php`

`foreach ($db->query('SELECT * FROM table') as $row) {`

`echo "<li>".$row['field1']." - ".$row['field1']."</li>";`

`}`

`?>`

`</ul>`

This is bad practice for all sorts of reasons, mainly that its hard to debug, hard to test, hard to read and it is going to output a lot of fields if you don’t put a limit on there.

While there are many other solutions to doing this - depending on if you prefer [OOP](http://phpdevenezuela.github.io/#object-oriented-programming) or [functional programming](http://phpdevenezuela.github.io/#functional-programming) - there must be some element of separation.

Consider the most basic step:

`<?php`

`function getAllFoos($db) {`

`return $db->query('SELECT * FROM table');`

`}`

`foreach (getAllFoos($db) as $row) {`

`echo "<li>".$row['field1']." - ".$row['field1']."</li>"; // BAD!!`

`}`

That is a good start. Put those two items in two different files and you’ve got some clean separation.

Create a class to place that method in and you have a “Model”. Create a simple .php file to put the presentation logic in and you have a “View”, which is very nearly [MVC](http://code.tutsplus.com/tutorials/mvc-for-noobs--net-10488) - a common OOP architecture for most [frameworks](http://phpdevenezuela.github.io/#frameworks_title).

_**foo.php**_

`<?php`

`$db = new PDO('mysql:host=localhost;dbname=testdb;charset=utf8mb4', 'username', 'password');`

`// Make your model available`

`include 'models/FooModel.php';`

`// Create an instance`

`$fooList = new FooModel($db);`

`// Show the view`

`include 'views/foo-list.php';`

_**models\/FooModel.php**_

`<?php`

`class Foo()`

`{`

`protected $db;`

`public function __construct(PDO $db)`

`{`

`$this->db = $db;`

`}`

`public function getAllFoos() {`

`return $this->db->query('SELECT * FROM table');`

`}`

`}`

_**views\/foo-list.php**_

`<? foreach ($fooList as $row): ?>`

`<?= $row['field1'] ?> - <?= $row['field1'] ?>`

`<? endforeach ?>`

This is essentially the same as what most modern frameworks are doing, all be it a little more manual. You might not need to do all of that every time, but mixing together too much presentation logic and database interaction can be a real problem if you ever want to [unit-test](http://phpdevenezuela.github.io/#unit-testing) your application.

[PHPBridge](http://phpbridge.org/) have a great resource called [Creating a Data Class](http://phpbridge.org/intro-to-php/creating_a_data_class) which covers a very similar topic, and is great for developers just getting used to the concept of interacting with databases.

