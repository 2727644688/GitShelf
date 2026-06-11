## Chapter 2 Answers

1. WAMP stands for Windows, Apache, MySQL, PHP. The M in MAMP stands for Mac instead of Windows, and the L in LAMP stands for Linux. They all refer to a complete solution for hosting dynamic web pages.  
2. SFTP stands for SSH File Transfer Protocol (sometimes Secure File Transfer Protocol). An SFTP program, similar to an FTP program, is used to transfer files back and forth between a client and a server but unlike FTP, SFTP is secure.  
3. Transferring files to a remote server to update them can substantially increase development time if this action is carried out many times and the internet connection is slow.  
4. Dedicated code editors are smart and can highlight problems in your code before you run it.

## Chapter 3 Answers

1. The tag used is <?php...?>. It can be shortened to <?...?>, but that is not recommended practice.  
2. You can use // for a single-line comment or /\*...\*/ to span multiple lines.  
3. All PHP statements must end with a semicolon (;).  
4. With the exception of constants, all PHP variables must begin with \$.  
5. A variable holds a value that can be a string, a number, or other data.  
6. \$variable = 1 is an assignment statement, whereas the == in \$variable == 1 and the === in \$variable === 1 is a comparison operator. Use \$variable = 1 to set the value of \$variable. Use \$variable === 1 to find out later in the program whether \$variable equals the number 1. If you use \$variable == 1,

it returns true even if \$variable is a string "1", which can cause unexpected bugs. If you mistakenly use \$variable = 1 where you meant to do a comparison, it will do two things you probably don’t want: set \$variable to 1 and return a true value all the time, no matter its previous value.

7. In PHP, the hyphen is reserved for the subtraction, decrement, and negation operators. A construct like \$current-user would be harder to interpret if hyphens were also allowed in variable names, and in any case would lead programs to be ambiguous.  
8. Yes, variable names are case-sensitive. \$This\_Variable is not the same as \$this\_variable.  
9. You cannot use spaces in variable names, as this would confuse the PHP parser. Instead, try using the \_ (underscore), or use camelCase notation.  
10. You can use type casting to convert the type, for example like \$number = (int)\$string. However, if type declarations are not used and you want to convert one variable type to another, reference it and PHP will automatically convert it for you.  
11. There is no difference between ++\$j and \$j++ unless the value of \$j is being tested, assigned to another variable, or passed as a parameter to a function. In such cases, ++\$j increments \$j before the test or other operation is performed, whereas \$j++ performs the operation and then increments \$j.  
12. Generally, the operators && and and are interchangeable except where precedence is important, in which case && has a high precedence, while and has a low one.  
13. You can use multiple lines within quotation marks or the <<<\_END...\_END; construct to create a multiline echo or assignment. In the latter case, the closing tag must be on a line by itself with nothing before or after it.  
14. You cannot redefine constants because, by definition, once defined they retain their value until the program terminates.  
15. You can use \' or \" to escape either a single or double quote.  
16. The echo and print commands are similar in that they are both constructs, except that print behaves like a PHP function and takes a single argument, while echo can take multiple arguments.  
17. The purpose of functions is to separate discrete sections of code into their own self-contained sections that can be referenced by a single function name.

18. You can make a variable accessible to all parts of a PHP program by declaring it as global. However this is not a recommended approach in production code.  
19. If you generate data within a function, you can convey the data to the rest of the program by returning a value or modifying a global variable.  
20. When you combine a string with a number, the result is another string.