## Chapter 16 Answers

1. You can send a form for validation prior to submitting it by attaching the submit event handler to the form using the addEventListener method. To prevent the form values being submitted on any validation error, use event.preventDefault().

2. To match a string against a regular expression in JavaScript, use the test method.

3. Regular expressions to match characters not in a word could be any of /[^\w]/, /[\W]/, /^\w/, /\W/ /[^a-zA-Z0-9\_]/, and so on.  
4. A regular expression to match either of the words fox or fix could be /f[oi]x/.  
5. A regular expression to match any single word followed by any nonword character could be /\w+\W/g.  
6. A JavaScript function using regular expressions to test whether the word fox exists in the string The quick brown fox could be:  
7. A PHP function using a regular expression to replace all occurrences of the word the in The cow jumps over the moon with the word my could be as follows:  
8. The HTML attribute used to precomplete form fields with a value is value, which is placed within an <input> tag and takes the form value="value".

```javascript
console.log(/fox/.test("The quick brown fox"))
```

```javascript
$s = preg_replace("/the/i", "my", "The cow jumps over the moon");
```