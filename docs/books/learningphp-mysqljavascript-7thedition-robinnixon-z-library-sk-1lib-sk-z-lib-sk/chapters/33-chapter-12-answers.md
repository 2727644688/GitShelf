# Chapter 12 Answers

1.

Cookies should be transferred before a web page’s HTML because they are sent as part of the headers.

2.

To store a cookie in a web browser, use the setcookie function.

3.

To destroy a cookie, reissue it with setcookie, but set its expiration date in the past.

4.

Using HTTP authentication, the username and password are stored in \$\_SERVER['PHP\_AUTH\_USER'] and \$\_SERVER['PHP\_AUTH\_PW'].

5.

The password\_hash function is a powerful security measure because it is a one-way function that converts a string to a long hexadecimal string of numbers that cannot be converted back quickly, and is therefore very hard to crack as long as strong passwords are required from users (for example, at least eight characters in length, including randomly placed numbers and punctuation marks).

6.

When a string is salted, extra characters known only by the web server (or by the programmer if they are self-salting the code) are added to it before hash conversion (this should normally be left up to PHP to handle for you, though, don’t add any extra salt when you’re using the password\_hash function for example). This ensures that users with the same password will not have the same hash and prevents the use of precomputed hash tables.

7.

A PHP session is a group of variables unique to the current user, stored on the server, passed along with successive requests so that the variables remain available as the user visits different pages.

8.

To initiate a PHP session, use the session\_start function.

9.

Session hijacking is where a hacker somehow discovers an existing session ID and attempts to take it over.

10.

Session fixation is when an attacker attempts to force a user to log in using a valid session ID the attacker has obtained earlier, thus compromising the connection’s security.