### Hash de contraseñas con password\_hash

En PHP 5.5 fue introducido password\_hash. En este momento está usando BCrypt, el algoritmo más fuerte actualmente soportado por PHP. Se actualizará en el futuro para apoyar a más algoritmos, según sea necesario. La librería password\_compat fue creada para proveer compatibilidad a las versiones PHP &gt;= 5.3.7.

Más abajo hacemos hash a una cadena de texto, y seguidamente comprobamos el hash con una nueva cadena. Debido a que las fuentes de nuestras dos cadenas son distintas \(‘contraseña-secreta’ vs ‘mala-contraseña’\) el login fallará.

`<?php`



`require 'password.php';`



`$passwordHash = password_hash('contraseña-secreta', PASSWORD_DEFAULT);`



`if (password_verify('mala-contraseña', $passwordHash)) {`

` // Contraseña correcta`

`} else {`

` // Contraseña incorrecta`

`}`

* [Aprende más acerca de password\_hash](http://es.php.net/manual/es/function.password-hash.php)
* [password\_compat para PHP &gt;= 5.3.7 && &lt; 5.5](https://github.com/ircmaxell/password_compat)
* [Obtener información acerca de hashing en cuanto a la criptografía](https://es.wikipedia.org/wiki/Funci%C3%B3n_hash_criptogr%C3%A1fica)
* [PHP password\_hash RFC](https://wiki.php.net/rfc/password_hash)

