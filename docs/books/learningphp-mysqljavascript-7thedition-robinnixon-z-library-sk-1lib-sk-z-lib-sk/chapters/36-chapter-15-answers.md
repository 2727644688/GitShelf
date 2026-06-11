# Chapter 15 Answers

**1.**

JavaScript functions and variable name are case-sensitive. The variables Count, count, and COUNT are all different.

**2.**

To write a function that accepts and processes an unlimited number of parameters, use the rest parameter syntax ...params, or as the less preferred option, access parameters through the arguments array, which is a member of all functions.

**3.**

One way to return multiple values from a function is to place them all inside an array and return the array.

**4.**

When defining a class, use the this keyword to refer to the current object.

**5.**

Yes, if using the recommended class syntax. If functions are used to create the object, the methods do not have to be defined within the class definition. If a method is defined outside the constructor, the method name must be assigned to the this object within the class definition.

**6.**

New objects are created via the new keyword.

**7.**

To create a multidimensional array, place subarrays inside the parent array.

8.

In JavaScript, objects can be used to emulate “associative arrays,” so you use the object syntax (key : value, within curly braces) to create such “array,” as in:

```txt
assocarray = {
forename : "Paul",
surname : "McCartney",
group : "The Beatles"
}
```

9.

A statement to sort an array of numbers into descending numerical order would look like this, using an anonymous arrow function:

```javascript
numbers.sort((a, b) => b - a)
```