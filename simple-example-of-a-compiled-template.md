### Simple example of a compiled template

Using the [Twig](http://twig.sensiolabs.org/) library.

`{% include 'header.html' with {'title': 'User Profile'} %}`

`<h1>User Profile</h1>`

`<p>Hello, {{ name }}</p>`

`{% include 'footer.html' %}`

