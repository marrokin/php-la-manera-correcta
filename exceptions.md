## Exceptions

Exceptions are a standard part of most popular programming languages, but they are often overlooked by PHP programmers. Languages like Ruby are extremely Exception heavy, so whenever something goes wrong such as a HTTP request failing, or a DB query goes wrong, or even if an image asset could not be found, Ruby \(or the gems being used\) will throw an exception to the screen meaning you instantly know there is a mistake.

PHP itself is fairly lax with this, and a call to file\_get\_contents\(\) will usually just get you a FALSE and a warning. Many older PHP frameworks like CodeIgniter will just return a false, log a message to their proprietary logs and maybe let you use a method like $this-&gt;upload-&gt;get\_error\(\) to see what went wrong. The problem here is that you have to go looking for a mistake and check the docs to see what the error method is for this class, instead of having it made extremely obvious.

Another problem is when classes automatically throw an error to the screen and exit the process. When you do this you stop another developer from being able to dynamically handle that error. Exceptions should be thrown to make a developer aware of an error; they then can choose how to handle this. E.g.:

`<?php`

`$email = new Fuel\Email;`

`$email->subject('My Subject');`

`$email->body('How the heck are you?');`

`$email->to('guy@example.com', 'Some Guy');`

`try`

`{`

`$email->send();`

`}`

`catch(Fuel\Email\ValidationFailedException $e)`

`{`

`// The validation failed`

`}`

`catch(Fuel\Email\SendingFailedException $e)`

`{`

`// The driver could not send the email`

`}`

`finally`

`{`

`// Executed regardless of whether an exception has been thrown, and before normal execution resumes`

`}`



* ### SPL Exceptions


