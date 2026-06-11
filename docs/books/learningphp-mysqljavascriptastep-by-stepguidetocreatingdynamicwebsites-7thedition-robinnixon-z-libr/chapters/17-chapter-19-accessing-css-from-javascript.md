## Chapter 19 Answers

1. The function to abbreviate DOM access uses the getElementById method, like this:

```javascript
function getById(id)
{
    return document.getElementById(id)
}
```

Or it can use the querySelector method, for example like this:

```javascript
function getBy(selector)
{
    return document.querySelector(selector)
}
```

Given an element with an ID box, you’d then call the functions as follows:

```javascript
getById('box')
getBy('#box') // note the # prefix
```

2. You can modify a CSS attribute of an object using the setAttribute function, like this:

```txt
myobject.setAttribute('font-size', '16pt')
```

You can also (usually) modify an attribute directly (using slightly modified property names where required), like this:

```txt
myobject.fontSize = '16pt'
```

3. The properties that provide the width and height available in a browser window are window.innerHeight and window.innerWidth.  
4. To make something happen when the mouse passes over and out of an object, attach the mouseover and mouseout events.  
5. To create a new element, use code such as:

```javascript
elem = document.createElement('span')
```

To add the new element to the DOM, use code such as:

```javascript
document.body.appendChild(elem)
```

6. To make an element invisible, set its visibility property to hidden (set it to visible to restore it again). To collapse an element’s dimensions to zero, set its display property to none (setting this property to block is one way to restore it to its original dimensions).  
7. To set up a single event at a future time, call the setTimeout function, passing it the code or function name to execute and the time delay in milliseconds.  
8. To set up repeating events at regular intervals, use the setInterval function, passing it the code or function name to execute and the time delay between repeats in milliseconds.  
9. To release an element from its location in a web page to enable it to be moved around, set its position property to relative, absolute, or fixed. To restore it to its original place, set the property to static.  
10. To achieve an animation rate of 50 frames per second, you should set a delay between interrupts of 20 milliseconds. To calculate this value, divide 1,000 milliseconds by the desired frame rate.

## Chapter 20 Answers

1. You can incorporate the React scripts in your web page by downloading the files and serving them from your own web server, or by using a CDN such as unpkg.com. Then load the scripts using script tags in your HTML document.  
2. To incorporate XML into your React JavaScript, you first need to load the Babel extension, either locally or from a CDN, using a script tag.  
3. JSX JavaScript <script> sections of code require type="text/babel" to work.  
4. You can extend React to your code either as a class using class Name extends React.Component or simply by returning code to be rendered by a function’s return statement. In both cases, ReactDOM.render must be called to initiate the rendering.  
5. In React, pure code doesn’t change its inputs, whereas code that does change inputs is considered impure.  
6. React keeps track of state with the props object and its attributes.  
7. To embed an expression within JSX code, you place it within curly braces, like this: Hello {props.name}.  
8. Once a class has been constructed, you can change the state of a value only by using the setState function.

9. To enable referring to props using the this keyword within a constructor, you must first call the super method, passing it props, like this: super(props).  
10. You can create a conditional statement in JSX using the && operator after the expression. For an if...then...else statement, you can use the ternary ?: operator.

## Chapter 21 Answers

1. After receiving a request for a file from a web browser and passing the request to the filesystem, Node.js returns to listening for new browser requests. Only when the filesystem sends an event to indicate the requested file is ready does it send the file contents back to the browser.  
2. To include a prewritten module in Node.js, load it using the import method.  
3. Node.js uses the http module to manage HTTP communications, the url module for URL parsing, and the fs module for accessing the local filesystem.  
4. The default HTTP port a server listens to is port 80. To avoid port clashes multiple servers may use different port numbers, such as port 8000, which is often used for proxies. Note that the default port for HTTPS is 443.  
5. The createServer method of an http module is called to create a new server object.  
6. Headers, if any, must be sent before returning data to a web browser. One way to do this is by calling the writeHead method of the server object  
7. To terminate a Node.js connection with a web browser, call the end method of the response object passed as a parameter to the createServer function of the http module.  
8. To start a Node.js server, from the command line type node server.js, where server.js is the filename of the server to run. Use the .mjs file extension to run a module.  
9. To manually terminate a Node.js server, press Ctrl-C at the command line.  
10. To write from Node.js to the terminal window command line, pass a string to the console.log or console.error functions.  
11. To add external Node.js modules to a project, use the npm program, like this: npm install packagename.

12. To access a MySQL database with Node.js, first install the mysql2 package using npm with the command npm install mysql2, then import it into a project using the import method:

```txt
import mysql from 'mysql2/promise'
```

13. To create a connection to MySQL (once you have installed and imported the module) call the createConnection method of the mysql object, like this:

```javascript
const connection = await mysql.createConnection({
    host: 'localhost',
    user: 'node',
    password: 'letmein',
    database: 'publications'
})
```

14. To use Node.js to query a MySQL database, call the execute method of an already created connection object, passing it the query string with placeholders.

15. To terminate a connection to a MySQL database, call the end method of its connection object.