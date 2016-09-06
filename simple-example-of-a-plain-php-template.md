_**Simple example of a plain PHP template**_

Using the [Plates](http://platesphp.com/) library.

`<?php // user_profile.php ?>`



`<?php $this->insert('header', ['title' => 'User Profile']) ?>`



`<h1>User Profile</h1>`

`<p>Hello, <?=$this->escape($name)?></p>`



`<?php $this->insert('footer') ?> `

