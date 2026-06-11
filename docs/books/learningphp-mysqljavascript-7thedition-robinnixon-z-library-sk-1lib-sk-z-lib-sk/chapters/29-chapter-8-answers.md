# Chapter 8 Answers

**1.**

The semicolon in MySQL separates or ends commands. If you forget to enter it, MySQL will issue a prompt and wait for you to enter the semicolon.

**2.**

To see the available databases, type SHOW databases. To see tables within a database that you are using, type SHOW tables. (These commands are case-insensitive.)

**3.**

To create this new user, use the GRANT command like this:

GRANT PRIVILEGES ON newdatabase.\* TO 'newuser'@'localhost'
IDENTIFIED BY 'newpassword';

**4.**

To view the structure of a table, type DESCRIBE tablename.

**5.**

The purpose of a MySQL index is to substantially decrease database access times by adding metadata to the table about one or more key columns, which can then be quickly searched to locate rows within a table.

**6.**

A FULLTEXT index enables natural-language queries to find keywords, wherever they are in the FULLTEXT column(s), in much the same way as

using a search engine.

7.

A stopword is a word that is so common that it is considered not worth including in a FULLTEXT index or using in searches. However, it is included in searches when it is part of a larger string bounded by double quotes.

8.

SELECT DISTINCT essentially affects only the display, choosing a single row and eliminating all the duplicates. GROUP BY does not eliminate rows but combines all the rows that have the same value in the column. Therefore, GROUP BY is useful for performing an operation such as COUNT on groups of rows. SELECT DISTINCT is not useful for that purpose.

9.

To return only those rows containing the word Langhorne somewhere in the column author of the table classics, use a command such as this:

SELECT \* FROM classics WHERE author LIKE "%Langhorne%";

10.

When you're joining two tables together, they must share at least one common column, such as an ID number or, as in the case of the classics and customers tables, the isbn column.