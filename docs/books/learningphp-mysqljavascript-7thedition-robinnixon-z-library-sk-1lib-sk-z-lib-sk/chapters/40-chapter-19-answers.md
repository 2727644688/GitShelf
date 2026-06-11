# Chapter 19 Answers

1.

The function to abbreviate DOM access uses the getElementById method, like this:

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

Given an element with an ID box, you’d then call the functions as follows:

```javascript
getById('box')
getBy('#box') // note the # prefix
```

2.

You can modify a CSS attribute of an object using the setAttribute function, like this:

```txt
myobject.setAttribute('font-size', '16pt')
```

You can also (usually) modify an attribute directly (using slightly modified property names where required), like this:

```txt
myobject.fontSize = '16pt'
```

3.

The properties that provide the width and height available in a browser window are window.innerHeight and window.innerWidth.

4.

To make something happen when the mouse passes over and out of an object, attach the mouseover and mouseout events.

5.

To create a new element, use code such as:

```javascript
elem = document.createElement('span')
```

To add the new element to the DOM, use code such as:

```javascript
document.body.appendChild(elem)
```

6.

To make an element invisible, set its visibility property to hidden (set it to visible to restore it again). To collapse an element’s dimensions to zero, set its display property to none (setting this property to block is one way to restore it to its original dimensions).

7.

To set up a single event at a future time, call the setTimeout function, passing it the code or function name to execute and the time delay in milliseconds.

8.

To set up repeating events at regular intervals, use the setInterval function, passing it the code or function name to execute and the time delay between repeats in milliseconds.

9.

To release an element from its location in a web page to enable it to be moved around, set its position property to relative, absolute, or fixed. To restore it to its original place, set the property to static.

10.

To achieve an animation rate of 50 frames per second, you should set a delay between interrupts of 20 milliseconds. To calculate this value, divide 1,000 milliseconds by the desired frame rate.