# Chapter 9 Answers

**1.**

The term relationship refers to the connection between two pieces of data that have some association, such as a book and its author or a book and the customer who bought the book. A relational database such as MySQL specializes in storing and retrieving such relationships.

**2.**

The process of removing duplicate data and optimizing tables is called normalization.

**3.**

The three rules of First Normal Form are:

- There should be no repeating columns containing the same kind of data.  
- All columns should contain a single value.  
- There should be a primary key to uniquely identify each row.

**4.**

To satisfy Second Normal Form, columns whose data repeats across multiple rows should be removed to their own tables.

**5.**

In a one-to-many relationship, the primary key from the table on the “one” side must be added as a separate column (a foreign key) to the

table on the “many” side.

6.

To create a database with a many-to-many relationship, you create an intermediary table containing keys from two other tables. The other tables can then reference one another via the third.

7.

To initiate a MySQL transaction, use the BEGIN or START TRANSACTION command. To terminate a transaction and cancel all actions, issue a ROLLBACK command. To terminate a transaction and commit all actions, issue a COMMIT command.

8.

To examine how a query will work in detail, you can use the EXPLAIN command.

9.

To back up the database publications to a file called publications.sql, you would use a command such as:

mysqldump -u user -ppassword publications > publications.sql