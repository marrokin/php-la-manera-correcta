### Example of plain PHP templates using inheritance

Using the [Plates](http://platesphp.com/) library.

`<?php // template.php ?>`

`<html>`

`<head>`

`<title><?=$title?></title>`

`</head>`

`<body>`

`<main>`

`<?=$this->section('content')?>`

`</main>`

`</body>`

`</html>`

`<?php // user_profile.php ?>`

`<?php $this->layout('template', ['title' => 'User Profile']) ?>`

`<h1>User Profile</h1>`

`<p>Hello, <?=$this->escape($name)?></p>`

