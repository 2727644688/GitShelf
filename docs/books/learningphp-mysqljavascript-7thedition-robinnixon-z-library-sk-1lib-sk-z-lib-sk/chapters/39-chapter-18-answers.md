# Chapter 18 Answers

1.

The CSS operators ^=, \$=, and \*= match the start, end, or any portion of a string, respectively.

2.

The property you use to specify the size of a background image is background-size, like this:

```txt
background-size:800px 600px;
```

3.

You can specify the radius of a border using the border-radius property:

```txt
border-radius:20px;
```

4.

To flow text over multiple columns, use the column-count, columngap, and column-rule properties, like this:

```txt
column-count:3;
column-gap :1em;
column-rule :1px solid black;
```

5.

The four functions you can use to specify CSS colors are hsl, hsla, rgb, and rgba. For example:

color:rgba(0%,60%,40%,0.4);

6.

To create a gray shadow under some text, offset diagonally to the bottom right by 5 pixels, with a blurring of 3 pixels, use this declaration:

text-shadow:5px 5px 3px #888;

7.

You can indicate that text is truncated with an ellipsis by using this declaration:

text-overflow:ellipsis;

8.

To include a Google web font such as Lobster in a web page, first select it from the Google Fonts website, then copy the provided <link> tag into the <head> of your HTML document. It will look something like this:

```txt
<link href='https://fonts.googleapis.com/css?family=Lobster'
rel='stylesheet'>
```

You can then refer to the font in a CSS declaration:

```css
h1 { font-family:'Lobster', arial, serif; }
```

9.

The CSS declaration you would use to rotate an object by 90 degrees is:

```txt
transform: rotate(90deg);
```

10.

To set up a transition on an object so that when any of its properties are changed the change will transition immediately and linearly over the course of half a second, use this declaration:

```txt
transition:all .5s linear;
```

11.

To create a flexbox container set its display property to flex.

12.

To define how flex items are spaced along the main axis of a flexbox, use the justify-content property of the container.

13.

To control the alignment of flex items along the cross axis of a flexbox container use the align-items property of the container.

14.

The two properties that determine how much a flexbox element can grow and shrink are flex-grow and flex-shrink.

15.

To change the order of elements in a flexbox container, assign numeric values to the order properties of the individual elements, with lower values appearing first.

16.

To set up a CSS grid layout, set the display property of the container object to either grid or inline-grid.

17.

To specify the flow direction of a grid container, use the container’s grid-auto-flow property.

18.

You can place items into a grid by using the items’ grid-column and grid-row properties.

19.

You can set the spacing of a grid with the gap property, which also has an older property name of grid-gap; both work the same way.

20.

You can align grid items vertically and horizontally using the justifyitems and align-items properties.