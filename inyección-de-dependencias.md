# Dependency Injection

From [Wikipedia](http://en.wikipedia.org/wiki/Dependency_injection):

Dependency injection is a software design pattern that allows the removal of hard-coded dependencies and makes it possible to change them, whether at run-time or compile-time.

This quote makes the concept sound much more complicated than it actually is. Dependency Injection is providing a component with it’s dependencies either through constructor injection, method calls or the setting of properties. It is that simple.

## Basic Concept

We can demonstrate the concept with a simple, yet naive example.

Here we have a Database class that requires an adapter to speak to the database. We instantiate the adapter in the constructor and create a hard dependency. This makes testing difficult and means the Database class is very tightly coupled to the adapter.

`<?php`

`namespace Database;`



`class Database`

`{`

`  protected $adapter;`



`  public function __construct()`

`  {`

`    $this->adapter = new MySqlAdapter;`

`   }`

`}`



`class MysqlAdapter {}`

This code can be refactored to use Dependency Injection and therefore loosen the dependency.

`<?php`

`namespace Database;`



`class Database`

`{`

`  protected $adapter;`



`  public function __construct(MySqlAdapter $adapter)`

`  {`

`    $this->adapter = $adapter;`

`  }`

`}`



`class MysqlAdapter {}`

Now we are giving the Database class its dependency rather than it creating it itself. We could even create a method that would accept an argument of the dependency and set it that way, or if the $adapter property was public we could set it directly.

## Complex Problem

If you have ever read about Dependency Injection then you have probably seen the terms _“Inversion of Control”_ or _“Dependency Inversion Principle”_. These are the complex problems that Dependency Injection solves.

### Inversion of Control

Inversion of Control is as it says, “inverting the control” of a system by keeping organisational control entirely separate from our objects. In terms of Dependency Injection, this means loosening our dependencies by controlling and instantiating them elsewhere in the system.

For years, PHP frameworks have been achieving Inversion of Control, however, the question became, which part of control are you inverting, and where to? For example, MVC frameworks would generally provide a super object or base controller that other controllers must extend to gain access to its dependencies. This **is** Inversion of Control, however, instead of loosening dependencies, this method simply moved them.

Dependency Injection allows us to more elegantly solve this problem by only injecting the dependencies we need, when we need them, without the need for any hard coded dependencies at all.

### Dependency Inversion Principle

Dependency Inversion Principle is the “D” in the S.O.L.I.D set of object oriented design principles that states one should _“Depend on Abstractions. Do not depend on concretions.”_. Put simply, this means our dependencies should be interfaces\/contracts or abstract classes rather than concrete implementations. We can easily refactor the above example to follow this principle.

`<?php`

`namespace Database;`



`class Database`

`{`

`  protected $adapter;`



`  public function __construct(AdapterInterface $adapter)`

`  {`

`    $this->adapter = $adapter;`

`  }`

`}`



`interface AdapterInterface {}`



`class MysqlAdapter implements AdapterInterface {}`

There are several benefits to the Database class now depending on an interface rather than a concretion.

Consider that you are working in a team and the adapter is being worked on by a colleague. In our first example, we would have to wait for said colleague to finish the adapter before we could properly mock it for our unit tests. Now that the dependency is an interface\/contract we can happily mock that interface knowing that our colleague will build the adapter based on that contract.

An even bigger benefit to this method is that our code is now much more scalable. If a year down the line we decide that we want to migrate to a different type of database, we can write an adapter that implements the original interface and inject that instead, no more refactoring would be required as we can ensure that the adapter follows the contract set by the interface.

## Containers

The first thing you should understand about Dependency Injection Containers is that they are not the same thing as Dependency Injection. A container is a convenience utility that helps us implement Dependency Injection, however, they can be and often are misused to implement an anti-pattern, Service Location. Injecting a DI container as a Service Locator in to your classes arguably creates a harder dependency on the container than the dependency you are replacing. It also makes your code much less transparent and ultimately harder to test.

Most modern frameworks have their own Dependency Injection Container that allows you to wire your dependencies together through configuration. What this means in practice is that you can write application code that is as clean and de-coupled as the framework it is built on.

## Further Reading

* [Learning about Dependency Injection and PHP](http://ralphschindler.com/2011/05/18/learning-about-dependency-injection-and-php)
* [What is Dependency Injection?](http://fabien.potencier.org/article/11/what-is-dependency-injection)
* [Dependency Injection: An analogy](http://mwop.net/blog/260-Dependency-Injection-An-analogy.html)
* [Dependency Injection: Huh?](http://net.tutsplus.com/tutorials/php/dependency-injection-huh/)
* [Dependency Injection as a tool for testing](http://www.happyaccidents.me/dependency-injection-as-a-tool-for-testing/)

