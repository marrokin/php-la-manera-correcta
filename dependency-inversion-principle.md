### Dependency Inversion Principle

Dependency Inversion Principle is the “D” in the S.O.L.I.D set of object oriented design principles that states one should _“Depend on Abstractions. Do not depend on concretions.”_. Put simply, this means our dependencies should be interfaces\/contracts or abstract classes rather than concrete implementations. We can easily refactor the above example to follow this principle.

`<?php`

`namespace Database;`

`class Database`

`{`

`protected $adapter;`

`public function __construct(AdapterInterface $adapter)`

`{`

`$this->adapter = $adapter;`

`}`

`}`

`interface AdapterInterface {}`

`class MysqlAdapter implements AdapterInterface {}`

There are several benefits to the Database class now depending on an interface rather than a concretion.

Consider that you are working in a team and the adapter is being worked on by a colleague. In our first example, we would have to wait for said colleague to finish the adapter before we could properly mock it for our unit tests. Now that the dependency is an interface\/contract we can happily mock that interface knowing that our colleague will build the adapter based on that contract.

An even bigger benefit to this method is that our code is now much more scalable. If a year down the line we decide that we want to migrate to a different type of database, we can write an adapter that implements the original interface and inject that instead, no more refactoring would be required as we can ensure that the adapter follows the contract set by the interface.

