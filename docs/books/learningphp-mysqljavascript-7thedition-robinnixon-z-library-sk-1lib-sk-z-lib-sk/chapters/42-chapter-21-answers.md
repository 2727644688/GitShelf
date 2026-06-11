# Chapter 21 Answers

**1.**

After receiving a request for a file from a web browser and passing the request to the filesystem, Node.js returns to listening for new browser requests. Only when the filesystem sends an event to indicate the requested file is ready does it send the file contents back to the browser.

**2.**

To include a prewritten module in Node.js, load it using the import method.

**3.**

Node.js uses the http module to manage HTTP communications, the url module for URL parsing, and the fs module for accessing the local filesystem.

**4.**

The default HTTP port a server listens to is port 80. To avoid port clashes multiple servers may use different port numbers, such as port 8000, which is often used for proxies. Note that the default port for HTTPS is 443.

**5.**

The createServer method of an http module is called to create a new server object.

**6.**

Headers, if any, must be sent before returning data to a web browser. One way to do this is by calling the writeHead method of the server object

7.

To terminate a Node.js connection with a web browser, call the end method of the response object passed as a parameter to the createServer function of the http module.

8.

To start a Node.js server, from the command line type node server.js, where server.js is the filename of the server to run. Use the .mjs file extension to run a module.

9.

To manually terminate a Node.js server, press Ctrl-C at the command line.

10.

To write from Node.js to the terminal window command line, pass a string to the console.log or console.error functions.

11.

To add external Node.js modules to a project, use the npm program, like this: npm install packagename.

12.

To access a MySQL database with Node.js, first install the mysql2 package using npm with the command npm install mysql2, then import it into a project using the import method:

13.

To create a connection to MySQL (once you have installed and imported the module) call the createConnection method of the mysql object, like this:

```javascript
const connection = await mysql.createConnection({
    host: 'localhost',
    user: 'node',
    password: 'letmein',
    database: 'publications'
})
```

14.

To use Node.js to query a MySQL database, call the execute method of an already created connection object, passing it the query string with placeholders.

15.

To terminate a connection to a MySQL database, call the end method of its connection object.