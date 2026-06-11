# Chapter 20 Answers

**1.**

You can incorporate the React scripts in your web page by downloading the files and serving them from your own web server, or by using a CDN such as unpkg.com. Then load the scripts using script tags in your HTML document.

**2.**

To incorporate XML into your React JavaScript, you first need to load the Babel extension, either locally or from a CDN, using a script tag.

**3.**

JSX JavaScript <script> sections of code require type="text/babel" to work.

**4.**

You can extend React to your code either as a class using class Name extends React.Component or simply by returning code to be rendered by a function’s return statement. In both cases, ReactDOM.render must be called to initiate the rendering.

**5.**

In React, pure code doesn’t change its inputs, whereas code that does change inputs is considered impure.

**6.**

React keeps track of state with the props object and its attributes.

**7.**

To embed an expression within JSX code, you place it within curly braces, like this: Hello {props.name}.

8.

Once a class has been constructed, you can change the state of a value only by using the setState function.

9.

To enable referring to props using the this keyword within a constructor, you must first call the super method, passing it props, like this: super(props).

10.

You can create a conditional statement in JSX using the && operator after the expression. For an if...then...else statement, you can use the ternary ?: operator.