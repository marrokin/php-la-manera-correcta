### Inversion of Control

Inversion of Control is as it says, “inverting the control” of a system by keeping organisational control entirely separate from our objects. In terms of Dependency Injection, this means loosening our dependencies by controlling and instantiating them elsewhere in the system.

For years, PHP frameworks have been achieving Inversion of Control, however, the question became, which part of control are you inverting, and where to? For example, MVC frameworks would generally provide a super object or base controller that other controllers must extend to gain access to its dependencies. This **is** Inversion of Control, however, instead of loosening dependencies, this method simply moved them.

Dependency Injection allows us to more elegantly solve this problem by only injecting the dependencies we need, when we need them, without the need for any hard coded dependencies at all.

