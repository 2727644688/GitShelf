## Chapter 17 Answers

1. The fetch function can be used for conducting asynchronous communication between a server and JavaScript client.  
2. You can pass an options object with method: "POST" and body: data properties as the second parameter when calling fetch.  
3. The fetch function returns an object of class Promise, which represents an asynchronous operation. You can use its then method to pass a code, as an arrow function for example, that will be called when the operation completed successfully.  
4. The function to get JSON data may be an arrow function and can be as simple as this (it will return a promise object):  
5. After calling the fetch function that returns a promise, pass an arrow function that returns the JSON data as the parameter to the then method. The json method also returns a promise. Then pass another arrow function to the then call on the promise, which can look like this:

```txt
response => response.json()
```

```txt
data => {
    // do something with data.a and data.b
}
```

6. The origin of the URL https://book.example/ch18?q=6 is https://book.example as origin consists of schema + domain + port if specified, which is not the case here.  
7. If a JavaScript code running on https://example.com/map would like to send an asynchronous request to https://www.example.com/data, then it would be a cross-origin request, not a same-origin one, because the origin of https:// example.com/map (which is https://example.com) doesn’t match the origin of https://www.example.com/data (which is https://www.example.com). Note that unlike the former URL, the latter one uses the www subdomain.  
8. The best way for JavaScript on http://localhost/info to access the response from https://example.com/data would be to add one of the two following HTTP headers to the response:

Access-Control-Allow-Origin: http://localhost

Access-Control-Allow-Origin: \*