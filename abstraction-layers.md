### Abstraction Layers

Many frameworks provide their own abstraction layer which may or may not sit on top of PDO. These will often emulate features for one database system that is missing from another by wrapping your queries in PHP methods, giving you actual database abstraction instead of just the connection abstraction that PDO provides. This will of course add a little overhead, but if you are building a portable application that needs to work with MySQL, PostgreSQL and SQLite then a little overhead will be worth it the sake of code cleanliness.

Some abstraction layers have been built using the [PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md) or [PSR-4](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md) namespace standards so can be installed in any application you like:

* [Aura SQL](https://github.com/auraphp/Aura.Sql)
* [Doctrine2 DBAL](http://www.doctrine-project.org/projects/dbal.html)
* [Propel](http://propelorm.org/)
* [ZF2 Db](http://packages.zendframework.com/docs/latest/manual/en/index.html#zend-db)

