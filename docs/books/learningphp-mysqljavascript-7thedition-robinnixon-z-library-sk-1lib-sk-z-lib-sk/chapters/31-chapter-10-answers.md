# Chapter 10 Answers

**1.**

To connect to a MySQL database with PDO, create a new object of the PDO class, passing the attributes, username, password, and options. A connection object will be returned on success.

**2.**

To submit a query to MySQL using PDO, ensure you have first created a connection object to a database, and then call its query method, passing the query string.

**3.**

The PDO::FETCH\_NUM style of the fetch method can be used to return a row as an array indexed by column number.

**4.**

You can manually close a PDO connection by assigning the value null to the PDO object used to connect to the database.

**5.**

When adding a row to a table with an AUTO\_INCREMENT column, you should pass the value null to that column.

**6.**

To escape special characters in strings, you can call the quote method of a PDO connection object, passing it the string to be escaped. Of course, for security, using prepared statements will serve you best.

**7.**

The best way to ensure database security when accessing it is to use placeholders and prepared statements.