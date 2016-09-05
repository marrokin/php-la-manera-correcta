### UTF-8 at the browser level

Use the mb\_http\_output\(\) function to ensure that your PHP script outputs UTF-8 strings to your browser.

The browser will then need to be told by the HTTP response that this page should be considered as UTF-8. The historic approach to doing that was to include the [charset &lt;meta&gt; tag](http://htmlpurifier.org/docs/enduser-utf8.html) in your page’s &lt;head&gt; tag. This approach is perfectly valid, but setting the charset in the Content-Type header is actually [much faster](https://developers.google.com/speed/docs/best-practices/rendering#SpecifyCharsetEarly).

`<?php`

`// Tell PHP that we're using UTF-8 strings until the end of the script`

`mb_internal_encoding('UTF-8');`

`// Tell PHP that we'll be outputting UTF-8 to the browser`

`mb_http_output('UTF-8');`

`// Our UTF-8 test string`

`$string = 'Êl síla erin lû e-govaned vîn.';`

`// Transform the string in some way with a multibyte function`

`// Note how we cut the string at a non-Ascii character for demonstration purposes`

`$string = mb_substr($string, 0, 15);`

`// Connect to a database to store the transformed string`

`// See the PDO example in this document for more information`

``// Note the `set names utf8mb4` commmand!``

`$link = new \PDO(`

`'mysql:host=your-hostname;dbname=your-db;charset=utf8mb4',`

`'your-username',`

`'your-password',`

`array(`

`\PDO::ATTR_ERRMODE => \PDO::ERRMODE_EXCEPTION,`

`\PDO::ATTR_PERSISTENT => false`

`)`

`);`

`// Store our transformed string as UTF-8 in our database`

`// Your DB and tables are in the utf8mb4 character set and collation, right?`

`$handle = $link->prepare('insert into ElvishSentences (Id, Body) values (?, ?)');`

`$handle->bindValue(1, 1, PDO::PARAM_INT);`

`$handle->bindValue(2, $string);`

`$handle->execute();`

`// Retrieve the string we just stored to prove it was stored correctly`

`$handle = $link->prepare('select * from ElvishSentences where Id = ?');`

`$handle->bindValue(1, 1, PDO::PARAM_INT);`

`$handle->execute();`

`// Store the result into an object that we'll output later in our HTML`

`$result = $handle->fetchAll(\PDO::FETCH_OBJ);`

`header('Content-Type: text/html; charset=UTF-8');`

`?>`

`<!doctype html>`

`<html>`

`<head>`

`<meta charset="UTF-8">`

`<title>UTF-8 test page</title>`

`</head>`

`<body>`

`<?php`

`foreach($result as $row){`

`print($row->Body); // This should correctly output our transformed UTF-8 string to the browser`

`}`

`?>`

`</body>`

`</html>`

