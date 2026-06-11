# Chapter 7 Answers

1.

The conversion specifier you would use to display a floating-point number is \%f.

2.

To take the input string "Happy Birthday" and output the string "\*\*Happy", you could use a printf statement such as this:

printf("%'\*7.5s", "Happy Birthday");

3.

To send the output from printf to a variable instead of to a browser, you would use sprintf instead.

4.

To create a Unix timestamp for 7:11 a.m. on May 2, 2025, you could use this command:

\$timestamp = mktime(7, 11, 0, 5, 2, 2025);

5.

You would use the w+ file access mode with fopen to open a file in write and read mode, with the file truncated and the file pointer at the start.

6.

The PHP command for deleting the file file.txt is:

unlink('file.txt');

7.

The PHP function file\_get\_contents is used to read in an entire file in one go. It will also read a file from across the internet if provided with a URL.

8.

The PHP superglobal associative array \$\_FILES contains the details about uploaded files.

9.

The PHP exec function enables running system commands.

10.

To turn any special characters returned by the system into ones that HTML can understand and properly display, use the htmlspecialchars function.