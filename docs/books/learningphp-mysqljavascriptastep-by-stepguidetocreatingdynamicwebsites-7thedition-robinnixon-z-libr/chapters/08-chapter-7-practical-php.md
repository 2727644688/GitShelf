## Chapter 7 Answers

1. The conversion specifier you would use to display a floating-point number is %f.  
2. To take the input string "Happy Birthday" and output the string "\*\*Happy", you could use a printf statement such as this:  
3. To send the output from printf to a variable instead of to a browser, you would use sprintf instead.  
4. To create a Unix timestamp for 7:11 a.m. on May 2, 2025, you could use this command:  
5. You would use the w+ file access mode with fopen to open a file in write and read mode, with the file truncated and the file pointer at the start.  
6. The PHP command for deleting the file file.txt is:

```txt
printf("%'*7.5s", "Happy Birthday");
```

```txt
$timestamp = mktime(7, 11, 0, 5, 2, 2025);
```

```javascript
unlink('file.txt');
```

7. The PHP function file\_get\_contents is used to read in an entire file in one go. It will also read a file from across the internet if provided with a URL.  
8. The PHP superglobal associative array \$\_FILES contains the details about uploaded files.  
9. The PHP exec function enables running system commands.  
10. To turn any special characters returned by the system into ones that HTML can understand and properly display, use the htmlspecialchars function.

## Chapter 8 Answers

1. The semicolon in MySQL separates or ends commands. If you forget to enter it, MySQL will issue a prompt and wait for you to enter the semicolon.  
2. To see the available databases, type SHOW databases. To see tables within a database that you are using, type SHOW tables. (These commands are case-insensitive.)  
3. To create this new user, use the GRANT command like this:

GRANT PRIVILEGES ON newdatabase.\* TO 'newuser'@'localhost' IDENTIFIED BY 'newpassword';

4. To view the structure of a table, type DESCRIBE tablename.

5. The purpose of a MySQL index is to substantially decrease database access times by adding metadata to the table about one or more key columns, which can then be quickly searched to locate rows within a table.

6. A FULLTEXT index enables natural-language queries to find keywords, wherever they are in the FULLTEXT column(s), in much the same way as using a search engine.

7. A stopword is a word that is so common that it is considered not worth including in a FULLTEXT index or using in searches. However, it is included in searches when it is part of a larger string bounded by double quotes.

8. SELECT DISTINCT essentially affects only the display, choosing a single row and eliminating all the duplicates. GROUP BY does not eliminate rows but combines all the rows that have the same value in the column. Therefore, GROUP BY is useful for performing an operation such as COUNT on groups of rows. SELECT DISTINCT is not useful for that purpose.

9. To return only those rows containing the word Langhorne somewhere in the column author of the table classics, use a command such as this:

SELECT \* FROM classics WHERE author LIKE "%Langhorne%";

10. When you’re joining two tables together, they must share at least one common column, such as an ID number or, as in the case of the classics and customers tables, the isbn column.

## Chapter 9 Answers

1. The term relationship refers to the connection between two pieces of data that have some association, such as a book and its author or a book and the customer who bought the book. A relational database such as MySQL specializes in storing and retrieving such relationships.  
2. The process of removing duplicate data and optimizing tables is called normalization.  
3. The three rules of First Normal Form are:

• There should be no repeating columns containing the same kind of data.  
• All columns should contain a single value.  
• There should be a primary key to uniquely identify each row.

4. To satisfy Second Normal Form, columns whose data repeats across multiple rows should be removed to their own tables.  
5. In a one-to-many relationship, the primary key from the table on the “one” side must be added as a separate column (a foreign key) to the table on the “many” side.  
6. To create a database with a many-to-many relationship, you create an intermediary table containing keys from two other tables. The other tables can then reference one another via the third.  
7. To initiate a MySQL transaction, use the BEGIN or START TRANSACTION command. To terminate a transaction and cancel all actions, issue a ROLLBACK command. To terminate a transaction and commit all actions, issue a COMMIT command.  
8. To examine how a query will work in detail, you can use the EXPLAIN command.  
9. To back up the database publications to a file called publications.sql, you would use a command such as:

mysqldump -u user -ppassword publications > publications.sql