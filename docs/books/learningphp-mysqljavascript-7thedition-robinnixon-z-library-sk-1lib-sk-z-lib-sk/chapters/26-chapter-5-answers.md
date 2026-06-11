# Chapter 5 Answers

**1.**

Using functions prevents the need to copy or rewrite similar code sections many times over by combining sets of statements so they can be called by a simple name.

**2.**

By default, a function can return a single value. But by utilizing arrays, references, and global variables, it can return any number of values.

**3.**

When you use a variable by name, such as by assigning its value to another variable or by passing its value to a function, its value is copied. The original does not change when the copy is changed. But if you reference a variable, only a pointer (or reference) to its value is used so that a single value is referenced by more than one name. Changing the value of the reference will change the original as well.

**4.**

Scope refers to which parts of a program can access a variable. For example, a variable of global scope can be accessed by all parts of a PHP program.

**5.**

To incorporate one file within another, you can use the include or require directives or their safer variants, include\_once and require\_once.

**6.**

A function is a set of statements referenced by a name that can receive and return values. An object may contain zero or many functions (which are then called methods) as well as variables (which are called properties), all combined in a single unit.

7.

To create a new object in PHP, use the new keyword like this:

```txt
$object = new Class;
```

8.

To create a subclass, use the extends keyword with syntax such as this:

class SubClass extends ParentClass { ... }

9.

To cause an object to be initialized when you create it, you can call a piece of initializing code by creating a constructor method called \_\_construct within the class and place your code there.

10.

Using properties not explicitly declared emits a deprecation notice starting with PHP 8.2. Previously, they were implicitly declared upon first use. But declaring them has always been considered good practice as it helps with code readability and debugging and is especially useful to other people who may have to maintain your code.