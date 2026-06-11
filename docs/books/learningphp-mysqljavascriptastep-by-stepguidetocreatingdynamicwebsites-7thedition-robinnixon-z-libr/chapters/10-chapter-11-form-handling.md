## Chapter 11 Answers

1. The associative arrays used to pass submitted form data to PHP are \$\_GET for the GET method and \$\_POST for the POST method.  
2. The difference between a text box and a text area is that although they both accept text for form input, a text box is a single line, whereas a text area can be multiple lines and include word wrapping.  
3. To offer three mutually exclusive choices in a web form, you should use radio buttons, because checkboxes allow multiple selections.  
4. You can submit a group of selections from a web form using a single field name by using an array name with square brackets, such as choices[], instead of a regular field name. Each value is then placed into the array, whose length will be the number of elements submitted.  
5. To submit a form field without the user seeing it, place it in a hidden field using the attribute type="hidden".

6. You can encapsulate a form element and supporting text or graphics, making the entire unit selectable with a mouse click, by using the <label> and </label> tags.  
7. To prevent XSS attacks, that is, to convert HTML into a format that can be displayed but will not be interpreted as HTML by a browser, use the PHP htmlentities or htmlspecialchars function.  
8. You can help users complete fields with data they may have submitted elsewhere by using the autocomplete attribute, which prompts the user with possible values.  
9. To ensure that a form is not submitted with missing data, you can apply the required attribute to essential inputs.

## Chapter 12 Answers

1. Cookies should be transferred before a web page’s HTML because they are sent as part of the headers.  
2. To store a cookie in a web browser, use the setcookie function.  
3. To destroy a cookie, reissue it with setcookie, but set its expiration date in the past.  
4. Using HTTP authentication, the username and password are stored in \$\_SERVER['PHP\_AUTH\_USER'] and \$\_SERVER['PHP\_AUTH\_PW'].  
5. The password\_hash function is a powerful security measure because it is a one-way function that converts a string to a long hexadecimal string of numbers that cannot be converted back quickly, and is therefore very hard to crack as long as strong passwords are required from users (for example, at least eight characters in length, including randomly placed numbers and punctuation marks).  
6. When a string is salted, extra characters known only by the web server (or by the programmer if they are self-salting the code) are added to it before hash conversion (this should normally be left up to PHP to handle for you, though, don’t add any extra salt when you’re using the password\_hash function for example). This ensures that users with the same password will not have the same hash and prevents the use of precomputed hash tables.  
7. A PHP session is a group of variables unique to the current user, stored on the server, passed along with successive requests so that the variables remain available as the user visits different pages.

8. To initiate a PHP session, use the session\_start function.  
9. Session hijacking is where a hacker somehow discovers an existing session ID and attempts to take it over.  
10. Session fixation is when an attacker attempts to force a user to log in using a valid session ID the attacker has obtained earlier, thus compromising the connection’s security.