_**Example of compiled templates using inheritance**_

Using the [Twig](http://twig.sensiolabs.org/) library.

`// template.html`



`<html>`

`<head>`

` <title>{% block title %}{% endblock %}</title>`

`</head>`

`<body>`



`<main>`

` {% block content %}{% endblock %}`

`</main>`



`</body>`

`</html>`

`// user_profile.html`



`{% extends "template.html" %}`



`{% block title %}User Profile{% endblock %}`

`{% block content %}`

` <h1>User Profile</h1>`

` <p>Hello, {{ name }}</p>`

`{% endblock %} `

