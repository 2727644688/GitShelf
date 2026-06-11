# Chapter 7: JavaScript Reminders

Before delving into the world of Vue.js, it is important to recall the fundamentals of JavaScript. This section is intended to assist you in refreshing your memory and getting up to speed on the key concepts of JavaScript that are utilized throughout the book.

We will cover essential concepts such as variables, arrays, objects, arrow functions, and modules. Additionally, we will explore more advanced concepts like asynchronous functions.

If you are already familiar with JavaScript, this section will help you recall and ensure that you have the necessary basics to understand Vue.js code examples.  
If you are new to the world of JavaScript, this section will provide you with a solid foundation to comprehend the concepts used throughout the book.

Ready to reinforce your JavaScript knowledge? Let’s begin!

## Using the Keywords let and var in JavaScript

In JavaScript, let and var are two keywords used to declare variables. The main difference between them lies in the variable’s scope.

The var keyword has a function scope, meaning that the variable is accessible inside the function where it is declared, as well as anywhere inside that function.

For example:

Using var to define a variable  
```javascript
function example() {
    var x = 10;
    if (true) {
    var x = 20; // The variable x is accessible inside the function example()
    }
    console.log(x); // Displays 20
}
```

In this example, the variable x is declared inside the function example(), but it is also accessible within the if block, because var has function scope. Therefore, writing var x = 20; does not create a new variable, as the variable x was declared earlier and is directly accessible within the if block. By writing var x = 20;, we are only modifying the value of the previously created variable.

On the other hand, the let keyword has block scope, which means the variable is accessible only within the block in which it is declared and in all nested blocks inside that block.

For example:

Using let to define a variable  
```javascript
function example() {
    let x = 10;
    if (true) {
    let x = 20; // The variable x is accessible only within the "if" block
```

```txt
}
console.log(x); // Displays 10
}
```

In this example, the variable x is declared inside the function example(). However, the second declaration of x inside the if block creates a new variable x, which is accessible only within that block. The variable x outside the if block retains its initial value of 10.

In summary, the main difference between let and var is the variable’s scope: var has function scope, and let has block scope. It is generally recommended to use let rather than var in JavaScript code, as it provides better control over variable scope and helps avoid accidental variable reuse across different blocks.

## Using the const Keyword in JavaScript

In JavaScript, the const keyword is used to declare a variable that cannot be reassigned after its initial value has been assigned. It creates a variable with a constant, unchangeable reference to a value. This means that once a value is assigned to a const variable, you cannot reassign it to a different value later in the code.

Here’s an explanation of how the const keyword works and its key characteristics.

When declaring a variable using const, you must immediately assign a value to it. Unlike the var or let keywords, you cannot declare a const variable without initializing it.

**Declaration and Initialization**

```javascript
const pi = 3.14159;
```

Once a value is assigned to a const variable, its value cannot be changed. Attempting to reassign a const variable will result in an error.

**Value Immutability**

```javascript
const pi = 3.14159;
pi = 3.14; // This will result in an error
```

Like variables declared with let, const variables are block-scoped. They are only accessible within the block (enclosed by curly braces) where they are defined.

**Block Scope**

```javascript
if (true) {
    const message = "Hello";
    console.log(message); // OK
}
console.log(message); // Error: 'message' is not defined
```

You cannot declare another variable with the same name in the same scope if you’ve already declared it with const.

**No Redeclaration**

```javascript
const value = 42;
const value = 100; // Error: Identifier 'value' has already been declared
```

When using const with objects and arrays, the reference to the object or array itself is immutable, but the properties or elements within the object or array can still be modified.

**Modifying object’s properties and array’s elements**

```javascript
const person = { name: "Alice", age: 30 };
person.age = 31; // Valid, modifies a property inside the object
const numbers = [1, 2, 3];
numbers.push(4); // Valid, adds an element to the array
```

In summary, the const keyword is used to declare variables that are meant to remain constant after their initial assignment. It ensures immutability of the variable reference, but the properties or elements within objects and arrays declared with const can still be modified. Use const for values that should not be changed throughout the scope of the variable.

## Manipulating Objects in JavaScript

In JavaScript, structuring and destructuring objects are techniques that allow for efficient data manipulation.

## Step 1: Structuring an Object

Structuring an object involves defining a data structure for that object. You can create an object with a list of properties and their corresponding values. For example, you can create a person object with properties like name, age, and city as follows:

**Creating the person object**

```javascript
const person = {
    name: "Gaby",
    age: 40,
    city: "Austin"
};
```

This allows us to access the values person.name (which is “Gaby”), person.age (which is 40), and person.city (which is “Austin”).

## Step 2: Object Destructuring

Object destructuring, on the other hand, allows you to extract object properties and use them independently. For instance, you can extract the name and age properties from the person object as follows:

**Destructuring the person object**

const { name, age } = person;

In this example, we create two variables, name and age, that correspond to properties of the same names in the person object. We can now use these variables independently of the rest of the object.

Destructuring can also be used to pass arguments to a function in a more concise way. For example, you can create a function that takes an object person as an argument and displays the person’s name and age:

**Using destructuring in function definition**

function displayNameAge({ name, age }) { console.log(\`The name is \${name} and the age is \${age}\`); }

In this example, we use destructuring to extract the properties name and age from the person object that is passed as an argument. We can now call this function with the person object as follows:

**Using the function**

displayNameAge(person);

This will display “The name is Gaby and the age is 40” in the console.

In summary, object structuring and destructuring in JavaScript are powerful techniques that allow for efficient and concise data manipulation.

## Step 3: Passing Objects As Function Parameters

In JavaScript, the notation { key1, key2 } is used in function parameters to perform object destructuring. This notation allows you to destructure a literal object by extracting the values associated with the specified properties and assigning them to variables with the same names as the properties.

Here’s an example to illustrate its usage:

Object as a function parameter  
```javascript
function displayDetails({ name, age }) {
    console.log(`Name: ${name}`);
    console.log(`Age: ${age}`);
}

const person = {
    name: "Gaby",
    age: 40,
    city: "Austin",
    profession: "Developer",
};

displayDetails(person); // Displays "Name: Gaby" and "Age: 40"
```

In this example, the displayDetails() function takes an object as a parameter and destructures the object to extract values associated with the name and age properties. The extracted values are then used to display the person’s details.

It’s important to note that if a specified property in the destructuring notation does not exist in the object, its value will be undefined.

Additionally, it’s possible to rename the extracted variables using the syntax { property: newVariable }.

In summary, the { key1, key2 } notation in function parameters allows for object destructuring, extracting values associated with specified properties. This leads to more concise and readable code, avoiding direct property access within the function body.

## Step 4: Using the “...” Notation with Objects

Let’s now explain the "..." (three consecutive dots) notation with objects. The "..." notation in JavaScript, also known as the spread or rest operator, is used to spread or gather the elements of an array or an object.

When used with an object, the "..." notation creates a shallow copy of the original object, including all its properties and their values. For example:

**Using the “..." notation with objects**

```javascript
const object1 = { x: 1, y: 2 };
const object2 = { ...object1 };
console.log(object2); // { x: 1, y: 2 }
```

In this example, the "..." notation is used to spread the properties of object1 into object2. This creates a shallow copy of object1, with the same properties and values.

If you write const object2 = object1;, it does not do the same thing at all! This statement creates a variable object2 that has the same memory reference as object1, thus referencing the same content as object1. If you modify the content of object1 or object2, the other object will be modified in the same way.

The "..." notation can also be used to merge multiple objects into one. For example:

**Merging objects with “..."**

```javascript
const object1 = { x: 1, y: 2 };
const object2 = { z: 3 };
```

```javascript
const object3 = { ...object1, ...object2 };
console.log(object3); // { x: 1, y: 2, z: 3 }
```

In this example, the "..." notation is used to merge the properties of objects object1 and object2 into a new object object3.

It’s important to note that the "..." notation creates only a shallow copy of the original object. If the object contains properties that are themselves objects or arrays, these properties are not deeply copied and are still shared between the original object and the copy (since it’s the references to objects or arrays that are copied, thus shared between the original object and the new object).

## Manipulating Arrays in JavaScript

In JavaScript, an array is a data structure that allows you to store and access multiple elements as an ordered list.

## Step 1: Structuring an Array

Structuring arrays in JavaScript refers to creating, initializing, and manipulating arrays to store and organize data.

Creating an array in JavaScript can be done in several ways. The most common way is to declare an empty array [] and add elements using the push() method. For example:

**Creating an array using the push() method**

```javascript
let array = [];
array.push(1);
array.push(2);
array.push(3);
console.log(array); // [1, 2, 3]
```

Another common method to create an array is by using the array literal notation, which allows you to declare and initialize an array in a single step. For example:

**Creating an array using []**

```javascript
let array = [1, 2, 3];
console.log(array); // [1, 2, 3]
```

## Step 2: Array Destructuring

Array destructuring in JavaScript refers to extracting elements from an array into separate variables. This feature is useful for manipulating arrays in a more concise and readable manner. For example:

**Array destructuring into separate variables**

```txt
let array = [1, 2, 3];
let [firstElement, secondElement, thirdElement] = array;
console.log(firstElement); // 1
console.log(secondElement); // 2
console.log(thirdElement); // 3
```

## Step 3: Using the “...” Notation with Arrays

Destructuring also allows you to retrieve a portion of an array using the "..." syntax. For example:

**Destructuring an array using the "..." notation**

```javascript
let array = [1, 2, 3, 4, 5];
let [a, b, ...rest] = array;
console.log(a); // 1
console.log(b); // 2
console.log(rest); // [3, 4, 5]
```

In this example, the "..." notation is used to retrieve the remaining elements of the array after assigning the first two elements to the variables a and b. The variable rest will contain the elements 3, 4, and 5 as an array, that is, [3, 4, 5].

## Using Import and Export of Modules in JavaScript

In JavaScript, modules are code files that can contain functions, variables, and classes, which can be imported and used in other code files. Modules allow for structuring and organizing JavaScript code, making it more modular and easier to maintain.

There are several ways to define and import modules in JavaScript, but the most common method is using the import and export syntax. Modules can be exported using the export and export default keywords, and they can be imported using the import keyword.

Here’s a simple example to illustrate the creation and usage of modules in JavaScript:

In the file myModule.js:

File: myModule.js  
```javascript
export const myVariable = "Hello world";
export function myFunction() {
    console.log("This is my function");
}
export default class MyClass {
    constructor() {
    console.log("This is my class");
    }
}
```

We export the variable myVariable, the function myFunction(), and the JavaScript class MyClass in the module myModule.js.

In another JavaScript file (e.g., test.js), we import these previously exported elements:

**File: test.js**

```javascript
import { myVariable, myFunction } from './myModule.js';
import MyClass from './myModule.js';

console.log(myVariable);
myFunction();
const myInstance = new MyClass();
```

You can also write the import statement on a single line as follows:

**File: test.js**

```javascript
import MyClass, { myVariable, myFunction } from './myModule.js';
console.log(myVariable);
myFunction();
const myInstance = new MyClass();
```

This way, we have access to the exported elements from the myModule. js file in the test.js file.

## Step 1: Using Modules in HTML Files

To use JavaScript modules in an HTML file, we use the <script> tag with the type attribute set to "module".

Here’s an example of HTML code that imports a module named myModule.js:

File: index.html  
```html
<!DOCTYPE html>
<html>
<head>
    <title>Example of Using Modules in HTML</title>
</head>
<body>
    <h1>Example of Using Modules in HTML</h1>
<script type="module">
    import { myFunction } from './myModule.js';
    myFunction();
</script>
</body>
</html>
```

The message “This is my function” is displayed in the browser console, demonstrating that the myFunction() is successfully accessible in the JavaScript code of the HTML file.

## Step 2: Using the import Statement

The import statement is used in JavaScript to import modules from one JavaScript file to another. The basic syntax for importing a module is as follows:

**Importing data from a module**

import { variableName, functionName } from './path/to/module';

This syntax allows you to import specific variables or functions from a module. The path to the module should be relative to the current JavaScript file.

Here are some examples of using the import statement in JavaScript:

Using import in a module  
```javascript
// Importing a specific variable
import { myVariable } from './myModule.js';
console.log(myVariable);
// Importing multiple variables and a function
import { myVar1, myVar2, myFunction } from './myModule.js';
console.log(myVar1);
console.log(myVar2);
myFunction();
// Importing all exported variables and functions
import * as myModule from './myModule.js';
console.log(myModule.myVar1);
console.log(myModule.myVar2);
myModule.myFunction();
```

In these examples, the import statement is used to import specific variables and functions from a module. In the last example, all exported variables and functions are imported using the \* operator, and an alias myModule is created to access the exported elements.

It’s important to note that the import statement can only be used in a module context. A JavaScript file must be explicitly marked as a module by using the type="module" directive in the <script> tag of the calling HTML file.

## Step 3: Using the export Statement

The export statement in JavaScript is used to export variables, functions, classes, or other elements from one JavaScript file to another. The exported elements can be used in other files by importing the module that contains them.

There are two main ways to export elements in JavaScript: using the export syntax or export default syntax.

The export syntax is used to export named elements. For example, to export a named variable myVariable and a named function myFunction from a file myModule.js, you can use the following syntax:

**Exporting variables (file myModule.js)**

```typescript
export const myVariable = "Hello world";
export function myFunction() {
    console.log("This is my function");
}
```

The exported elements can then be imported into another file using the import statement. Here’s an example:

**Importing variables in another module**

```javascript
import { myVariable, myFunction } from './myModule.js';
console.log(myVariable); // Displays "Hello world"
myFunction(); // Displays "This is my function"
```

## Step 4: Using the export default Statement

The export default syntax is used to export a default element from a module. For example, to export a default class from a file myModule.js, you can use the following syntax:

**Using export default (file myModule.js)**

```javascript
export default class MyClass {
    constructor() {
    console.log("This is my class");
    }
}
```

In this example, the MyClass class is exported as the default. It can be imported into another file using the following syntax:

**Importing variables in another module**

import MyClass from './myModule.js';

const myInstance = new MyClass(); // Creates a new instance of the MyClass class

In summary, the export statement in JavaScript allows you to export elements from a module to make them available in other JavaScript files. It can be used to export variables, functions, classes, or other elements and can be combined with the import statement to create modular and reusable JavaScript applications.

## Step 5: Difference Between export and export default Statements

The decision to use export or export default in JavaScript depends on how you want to expose module elements and import them later.

The export syntax is used to export multiple named elements from a module. This means that when a module is imported, the exported elements must be imported with their original names and enclosed in curly braces.

For example:

**Using export then import**

```javascript
// In the file "myModule.js"
export const myVar1 = "Hello";
export const myVar2 = "World";
export function myFunction() {
```

```javascript
console.log("This is my function");
}
// In the file that imports the module
import { myVar1, myVar2, myFunction } from './myModule.js';
// with curly braces
```

In this example, the exported elements must be imported using their original names and enclosed in curly braces. If we try to import an element with a different name than the one specified in the export, an error will be generated.

The export default syntax is used to export a default element from a module. This means that the element exported as default can be imported later using a name of our choice. Only one element can be exported as default in a module, to avoid confusion.

JavaScript will understand that we want to import the default exported element in a module because we import it without using the curly braces notation, unlike elements exported using the export statement, which are imported with the curly braces notation.

For example:

Using export default then import  
```javascript
// In the file "myModule.js"
export default class MyClass {
    constructor() {
    console.log("This is my class");
    }
}

// In the file that imports the module
import MyCustomName from './myModule.js'; // without using curly braces
const myInstance = new MyCustomName();
```

In this example, the default exported element (the MyClass class) can be imported using a name of our choice (MyCustomName in this case). This can be useful if we want to give a more meaningful name to the imported element or avoid naming conflicts.

In summary, export is used to export multiple named elements from a module, while export default is used to export an element that will be considered the default one during import. The decision to use one or the other depends on how we want to expose module elements and how we want to import them into other files.

## Using Arrow Functions in JavaScript

Arrow functions are a new function syntax introduced in ECMAScript 6 (ES6) to write functions in a more concise and readable way. Here are the main differences between arrow functions and traditional functions:

More Concise Syntax: Arrow functions have a more concise syntax than traditional functions. Instead of the classic function() {function body}, arrow functions are written like this: () => {function body}.  
No Bound this Keyword: In traditional functions, the this keyword is bound to the object that calls the function. In arrow functions, this is bound to the lexical context in which the function is defined. This means that this in an arrow function refers to this in the parent scope (the value of this in an arrow function will be the same as that of the parent).

Apart from the concise writing aspect of arrow functions, the deciding factor to use them in JavaScript code is mostly the desired value for the this variable.

Let’s now look at the syntax of these functions and then explain the value of this in each use case.

## Step 1: Using Arrow Function Syntax

Let’s start by examining the writing syntax of these functions. Here’s an example:

Using traditional functions and arrow functions  
```javascript
// Traditional function to calculate the square of a number
function square(x) {
    return x * x;
}

// Arrow function to calculate the square of a number
const square2 = (x) => x * x;

// Using the function
console.log(square2(5)); // Result: 25
```

In this example, the first function is a traditional function that calculates the square of a number. The second function is the arrow version of the same function, which uses a more concise syntax. Both functions have the same functionality, but the arrow version is more concise and easier to read.

Note that the arrow function syntax includes parentheses around the parameters (in this case, x), followed by the arrow => and then the function body (in this case, x \* x). The arrow version doesn’t require the return keyword here because it automatically returns the calculated value.

Here’s an example of an arrow function in JavaScript that uses the return statement:

Functions using the return keyword  
```javascript
// Traditional function to find the largest number in an array
function findLargest(array) {
    let largest = 0;
    for (let i = 0; i < array.length; i++) {
```

Chapter 7 JavaSc ript Reminders  
```javascript
if (array[i] > largest) {
    largest = array[i];
}
return largest;
}

// Arrow function to find the largest number in an array
const findLargest2 = (array) => {
    let largest = 0;
    for (let i = 0; i < array.length; i++) {
    if (array[i] > largest) {
    largest = array[i];
    }
    }
    return largest;
}

// Using the function
console.log(findLargest2([4, 8, 2, 10, 5])); // Result: 10
```

In this example, the first function is a traditional function that finds the largest number in an array. The second function is the arrow version of the same function, which uses a more concise syntax. Both functions have the same functionality, and the arrow version also uses the return statement to return the calculated value.

Note that the arrow function syntax still includes parentheses around the parameters and the => arrow, but this time there are also curly braces to delimit the function body. The return statement is used to return the calculated value.

## Step 2: Understanding the Value of this in Arrow Functions

The value of this in an arrow function is determined by the lexical context in which the function is defined, unlike traditional functions where this is determined by how the function is called.

In an arrow function, this refers to the value of this in the parent scope. This means that if the arrow function is defined within an object, for example, this in the arrow function refers to the parent object, not the object that calls the function.

Here’s an example to illustrate this concept:

Values of this in traditional functions and arrow functions  
```javascript
const obj = {
    name: "John",
    sayHello: function() {
    console.log(`Hello, my name is ${this.name}'); // "John"
    (this refers to obj)
    },
    sayHelloArrow: () => {
    console.log(`Hello, my name is ${this.name}'); //
    undefined (this refers to the parent of obj)
    }
}

obj.sayHello(); // Result: "Hello, my name is John"
obj.sayHelloArrow(); // Result: "Hello, my name is undefined"
```

In this example, the object obj contains two functions: sayHello() and sayHelloArrow(). sayHello() is a regular function that uses this to access the name property of the object, while sayHelloArrow() is an arrow function that also uses this to access the name property.

When the sayHello() function is called, this refers to the obj object, allowing access to the name property and displaying it in the console. However, when the sayHelloArrow() function is called, this refers to the lexical context in which the function was defined, which is the global context in this case. Therefore, this.name is undefined in the arrow function, and undefined is displayed in the console.

Depending on the value of this that we want to access, we will use either a regular function or an arrow function.

## Using the map( ) and filter( ) Methods of the JavaScript Array Class

The map(callback) and filter(callback) methods are two commonly used high-level functions in JavaScript for manipulating arrays (or collections of objects). Here’s an explanation of each method:

## Step 1: Using the map( ) Method

The map(callback) method creates a new array by applying a given function, here named callback(), to each element of the original array. The map() method takes a callback() function as a parameter.

The callback(element, index, array) function is then applied to each element of the original array. This function can take up to three arguments:

1. element: The current element being processed  
2. index (optional): The index of the current element being processed in the array  
3. array (optional): The original array on which we are applying the function

The map() method then returns a new array with the results of applying the callback() function to each original element. The resulting array will have the same length as the original array.

Here’s a simple example for better understanding:

Using the map() method  
```javascript
const array = [1, 2, 3, 4, 5];
const doubledArray = array.map(function(element) {
    return element * 2;
});
console.log(doubledArray); // [2, 4, 6, 8, 10]
```

Here, we created an array with numbers, and then we used the map() method to create a new array with the same numbers, but multiplied by 2.

The map() method returns a new array constructed from the elements of the original array. The resulting array will have the same number of elements as the original array.

To reduce the number of elements in the resulting array, we will use the filter() method, which allows us to select the elements to be included in the resulting array (but without modifying them). Let’s now look at the filter() method.

## Step 2: Using the filter( ) Method

The filter(callback) method also creates a new array, but it filters the elements of the original array that satisfy a specified condition. This method also takes a callback() function as an argument, which will be applied to each element of the original array. This callback() function must return a boolean value: true if the element should be retained in the resulting array returned by the filter() method, false otherwise.

The callback(element, index, array) filter function also takes up to three arguments:

1. element: The current element being processed  
2. index (optional): The index of the current element being processed in the array  
3. array (optional): The original array on which the function is being applied

The filter() method then returns a new array with all the elements of the original array that satisfy the specified condition.

Here’s a simple example to better understand:

**Using the filter() method**

```javascript
const array = [1, 2, 3, 4, 5];
const filteredArray = array.filter(function(element) {
    return element % 2 === 0; // Returns true if the element is even (element is kept), otherwise false
});
console.log(filteredArray); // [2, 4]
```

Here, we’ve created an array with numbers, and then we used the filter() method to create a new array with only the even numbers.

## Using Promise Objects in JavaScript

Promise objects in JavaScript are used for handling asynchronous tasks, which are tasks that don’t complete immediately. A Promise object represents a value that may not be available immediately but will be resolved (i.e., become available) at some point in the future.

## Step 1: Promise Object Definition

Promise objects are often created as return values from functions because they provide a clearer and more structured way of handling asynchronous tasks.

When an asynchronous task is executed, it doesn’t immediately return a result, as it needs to perform an operation that may take time (such as an HTTP request or file reading). While waiting for this operation to complete, the code that follows continues to execute, potentially causing synchronization and blocking issues.

Promise objects are used to address this issue. They provide a clear and structured way to handle asynchronous tasks by returning an object that represents the promise of a future result. This object can be used to attach callback functions that will be called once the asynchronous task is completed and the result is available.

For example, a function that performs an HTTP request can return a Promise object representing the promise of the request’s result. Callbacks can then be attached to this Promise object using the then() and catch() methods to handle successful results (with then()) or errors (with catch()) that may occur during the execution of the asynchronous task.

In summary, the Promise object is created as a return value from a function to handle asynchronous tasks in a structured manner by returning an object representing the promise of a future result and attaching callbacks to handle results or errors.

A Promise object can be in one of the following three states:

1. “pending”: The initial state of the Promise object, indicating that the asynchronous task is currently being executed  
2. “resolved”: The state in which the Promise object is resolved with a value  
3. “rejected”: The state in which the Promise object is rejected with an error reason

The Promise object exposes two methods for handling the results of the asynchronous task:

1. The then() Method: Used to handle the result if the task is successfully resolved  
2. The catch() Method: Used to handle errors that occur if the task is rejected

By using Promise objects, it’s possible to perform asynchronous tasks in JavaScript more efficiently and in a way that’s easier to read and maintain.

To understand the use of Promise objects, let’s take an example where we don’t use them and then the same example where we do.

## Step 2: Without Using Promise Objects

Here’s an example without using Promise objects.

Let’s say we want to load images from a server and display them in our application. Without Promise objects, we would have to use callbacks to handle the asynchrony:

## Without using Promise objects

```javascript
function loadImage(url, callback) {
    const img = new Image();
    img.onload = function() {
    // no error
    callback(null, img);
    };
    img.onerror = function() {
    // error
    callback("Unable to load the image.", null);
};
```

```javascript
img.src = url; // image loading
}
loadImage("https://example.com/image.jpg", function(error, img) {
    if (error) {
    console.error(error);
    } else {
    document.body.appendChild(img);
    }
});
```

This example uses the Image object to load an image from the server. The loadImage() function takes the image URL and a callback function as arguments. This callback will be invoked once the image has been loaded. After the image is loaded, further processing can take place within the callback function, allowing for handling of the asynchrony. The callback function has two arguments: a possible error and the loaded img (image) itself.

**Step 3: Using Promise Objects**

Now, here’s the same example using Promise objects:

**Using Promise objects**

```javascript
function loadImage(url) {
    return new Promise(function(resolve, reject) {
    const img = new Image();
    img.onload = function() {
    // no error
    resolve(img);
    };
};
```

Chapter 7 JavaSc ript Reminders  
```javascript
img.onerror = function() {
    // error
    reject("Unable to load the image.");
};
img.src = url; // image loading
});
}

loadImage("https://example.com/image.jpg")
.then(function(img) {
document.body.appendChild(img);
})
.catch(function(error) {
console.error(error);
});
```

Here, the loadImage() function returns a Promise object that is resolved with the image if the image loading succeeds, or is rejected with an error message if it fails. By using the then() method, we can handle the image once it has been loaded, and with the catch() method, we can handle errors that occur.

The use of Promise objects in this example makes the code more readable and easier to understand and provides simplified error handling.

## Using async and await Statements in JavaScript

The async and await statements are features of JavaScript that make working with Promise objects even more readable and understandable for handling asynchronous tasks.

By using async and await statements, code can be written synchronously (i.e., with sequentially following instructions) while still effectively managing asynchronous tasks. The async statement is used to mark a function as asynchronous, allowing the use of the await statement within that function.

The await statement is used to wait for the resolution of a Promise object before continuing the code execution. This avoids the use of callbacks and results in code that is easier to read and understand.

For example, here’s a usage example of Promise objects to make an HTTP request. We will then see how to write the same code using async and await statements.

**Using Promise objects to make an HTTP request**

```javascript
fetch("https://api.example.com/data")
.then(response => response.json())
.then(data => console.log(data))
.catch(error => console.error(error));
```

The fetch() and json() methods in JavaScript each return a Promise object, enabling the use of the then() and catch() methods on these methods.

Now, here’s how we can rewrite this code using async and await statements:

**Using async and await statements to make an HTTP request**

```javascript
async function getData() {
    try {
    const response = await fetch("https://api.example.com/data");
    const data = await response.json();
    console.log(data);
    } catch (error) {
```

Chapter 7 JavaSc ript Reminders  
```javascript
console.error(error);
}
}
getData();
```

Here, the getData() function is marked as async, which allows (within the getData() function) the use of the await statement to wait for the resolution of Promise objects returned by the fetch() function and the json() method. The use of async and await statements enables writing code that is more readable and easier to understand while efficiently managing asynchronous tasks.

In summary, the use of async and await statements provides an easier and more readable way to utilize Promise objects for handling asynchronous tasks. This helps avoid the use of callbacks and reduces code complexity.

## Creating an Asynchronous Function That Utilizes JavaScript’s await Statement

Let’s now see how to create an asynchronous function that can use the await statement. For this purpose, the function using await should fall into one of the following two cases:

1. The function returns a Promise object. This is the case, for example, with the previous fetch() and json() methods.  
2. The function is declared with the async keyword. In this case, the function’s return is always considered as a Promise object (even if the function returns another value).

Let’s examine these two cases now.

## Step 1: Using await with a Function That Returns a Promise Object

For await to be used with a function, the function can return a Promise object or be declared with the async keyword.

Here’s an example of a function that returns a Promise object:

**Function returning a Promise object**

```javascript
function wait(ms) {
    return new Promise(resolve => setTimeout(resolve, ms));
}
```

The wait(ms) function takes a number of milliseconds as input and returns a Promise object that will resolve after the specified number of milliseconds. The function utilizes the setTimeout() function to trigger the resolution of the Promise object after a specified delay.

To use the wait(ms) function with the await statement, you simply need to call it within a function marked with async, like this:

**Usage of await in an async function**

```javascript
async function myFunction() {
    console.log("Start"); // Display "Start"
    await wait(2000); // Wait for 2 seconds
    console.log("End"); // Then display "End" (after 2 seconds)
}
myFunction();
```

This myFunction() function uses the await statement to wait for the resolution of the Promise object returned by the wait() function. The function prints “Start” to the console, waits for two seconds using await wait(2000), and then prints “End” to the console.

In cases where the wait(ms) function wants to return a value, you can simply provide that value (“value”) as a parameter in the resolve(value) function call.

The wait(ms) function becomes the following:

Function wait(ms) that returns a value  
```javascript
function wait(ms) {
    return new Promise(resolve => setTimeout(() =>
    resolve("Waiting for " + ms + " ms"), ms));
}
```

We can no longer simply indicate setTimeout(resolve, ms) as before, because now we need to explicitly call the resolve() function and pass the return value as a parameter. Hence, the new syntax is written as setTimeout(() => resolve(value), ms).

We use the value returned by the wait(ms) function as follows:

Using the value returned by the wait(ms) function  
```javascript
async function myFunction() {
    console.log("Start"); // Display "Start"
    const result = await wait(2000); // Wait for 2 seconds
    console.log(result); // Display the result returned by the wait() function
    console.log("End"); // Then display "End"
}
myFunction();
```

## Step 2: Using await with a Function Declared with async

This is the second way to use the await statement when calling a function. The function must have been declared using the async keyword during its definition.

A function declared with the async keyword is considered to return a Promise object. Therefore, it can be used when called with the then() and catch() methods or used with the await keyword.

Using the myFunction() function with “await”  
```javascript
function wait(ms) {
    return new Promise(resolve => setTimeout(() =>
    resolve("Waiting for " + ms + " ms"), ms));
}

async function myFunction() {
    console.log("Start"); // Display "Start"
    const result = await wait(2000); // Wait for 2 seconds
    console.log(result); // Display the result returned by the wait() function
    console.log("End"); // Then display "End"
    return "myFunction(): Waiting for 2000ms";
}

async function myMainFunction() {
    const result = await myFunction();
    console.log("result =", result);
}

myMainFunction();
```

Since the myFunction() is declared with async, it can be used within a new function called myMainFunction() using the await keyword. The result returned by myFunction() will be used as the return value in myMainFunction(), asynchronously (after waiting for two seconds).

The same process can be written using promises and the then() and catch() methods:

Using promises instead of await  
```typescript
function wait(ms) {
    console.log("wait(" + ms + ")");
    return new Promise(resolve => setTimeout(() =>
    resolve("Waiting for " + ms + " ms"), ms));
}

async function myFunction() {
    console.log("Start"); // Display "Start"
    const result = await wait(2000); // Wait for 2 seconds
    console.log(result); // Display the result returned by the wait() function
    console.log("End"); // Then display "End"
    return "myFunction(): Waiting for 2000ms";
}

myFunction().then((res) => { console.log(res) });
```

The then(res) method used on the promise myFunction() allows retrieving the result of the promise, which is the string “myFunction(): Waiting for 2000ms”, in the parameter res.

## Conclusion

In this chapter, we have covered the fundamentals of JavaScript, which are the ones used in programs written with Vue.js. This knowledge is necessary to harness the full power of Vue.js in our applications.