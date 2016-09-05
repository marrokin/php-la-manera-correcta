### UTF-8 at the Database level

If your PHP script accesses MySQL, there’s a chance your strings could be stored as non-UTF-8 strings in the database even if you follow all of the precautions above.

To make sure your strings go from PHP to MySQL as UTF-8, make sure your database and tables are all set to the utf8mb4 character set and collation, and that you use the utf8mb4 character set in the PDO connection string. See example code below. This is _critically important_.

Note that you must use the utf8mb4 character set for complete UTF-8 support, not the utf8 character set! See Further Reading for why.

