# Chapter 11 Answers

1.

The associative arrays used to pass submitted form data to PHP are \$\_GET for the GET method and \$\_POST for the POST method.

2.

The difference between a text box and a text area is that although they both accept text for form input, a text box is a single line, whereas a text area can be multiple lines and include word wrapping.

3.

To offer three mutually exclusive choices in a web form, you should use radio buttons, because checkboxes allow multiple selections.

4.

You can submit a group of selections from a web form using a single field name by using an array name with square brackets, such as choices[], instead of a regular field name. Each value is then placed into the array, whose length will be the number of elements submitted.

5.

To submit a form field without the user seeing it, place it in a hidden field using the attribute type="hidden".

6.

You can encapsulate a form element and supporting text or graphics, making the entire unit selectable with a mouse click, by using the <label> and </label> tags.

7.

To prevent XSS attacks, that is, to convert HTML into a format that can be displayed but will not be interpreted as HTML by a browser, use the PHP htmlentities or htmlspecialchars function.

8.

You can help users complete fields with data they may have submitted elsewhere by using the autocomplete attribute, which prompts the user with possible values.

9.

To ensure that a form is not submitted with missing data, you can apply the required attribute to essential inputs.