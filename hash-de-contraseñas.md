## Hash de contraseñas

Con el tiempo todo el mundo desarrolla una aplicación PHP que se apoya en la conexión del usuario. Los nombres de usuario y las contraseñas se almacenan en una base de datos y posteriormente son utilizados para autenticar a los usuarios en el login.

Es importante que usted [realice hash](https://es.wikipedia.org/wiki/Funci%C3%B3n_hash_criptogr%C3%A1fica) de las contraseñas correctamente antes de almacenarlos. Una vez realizado el hash a la contraseña con una función aplicada contra la contraseña del usuario, el paso es irreversible. Esto produce una cadena de longitud fija que no puede ser revertida factiblemente. Esto significa que puede comparar un hash contra otro para determinar si ambos proceden de la misma cadena de origen, pero no se puede determinar la cadena original. Si las contraseñas no están hasheadas y se accede a la base de datos por un tercero no autorizado, todas las cuentas de usuario están comprometidas. Algunos usuarios pueden \(por desgracia\) utilizar la misma contraseña para otros servicios. Por lo tanto, es importante tomar en serio la seguridad.

* ### Hash de contraseñas con password\_hash


