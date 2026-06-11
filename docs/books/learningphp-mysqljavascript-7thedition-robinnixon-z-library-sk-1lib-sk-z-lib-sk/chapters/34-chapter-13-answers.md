# Chapter 13 Answers

**1.**

To enclose JavaScript code, you use <script> and </script> tags.

**2.**

You can include JavaScript code from other files in your documents by either copying and pasting them or, more commonly, including them as part of a <script src='filename.js'> tag.

**3.**

The equivalent of the echo and print commands used in PHP for quick output are the JavaScript functions console.log, alert, document.write, or writing directly into elements.

**4.**

To create a comment in JavaScript, preface it with // for a single-line comment or surround it with /\* and \*/ for a multiline comment.

**5.**

The JavaScript string concatenation operator is the + symbol.

**6.**

Within a JavaScript function, you can define a variable that has local scope by preceding it with the let or var keywords upon first assignment.

**7.**

To display the URL assigned to the link with an id of thislink in all main browsers, you can use either of these commands:

```javascript
console.log(document.getElementById('thislink').href)
console.log(thislink.href)
```

8.

The commands to change to the previous page in the browser’s history array are:

```txt
history.back()
history.go(-1)
```

9.

To replace the current document with the main page at the O’Reilly website, you could use this command:

```javascript
document.location.href = 'http://oreilly.com'
```