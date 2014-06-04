#jQuery Basics Review
```javascript
var someElement = $('#someElement'); //get someElement and save it in a var
```

## jQuery Classes
```javascript
// NOTE: Don't write it as ".aClass" (no period)
//       We aren't writing selectors.
//Add a class
someElement.addClass('aClass');
//Remove a class
someElement.removeClass('anotherClass');
//Toggle a class
someElement.toggleClass('toggleMe');
//Ask *if* an element has a class (returns true or false)
someElement.hasClass('mayOrMayNotHaveThisClass');
```

## jQuery Events
### Click Events
```javascript
var elementToClick = $('#clickMe');
//Here's the magic.
elementToClick.click(function () {
    //Write the code to execute on a click.
});

/*OR*/
var functionToRunOnClick = function () {
    //Write the code to execute on a click.
};
//You can instead pass a variable that holds a function.
//Note the lack of () after the variable name,
// we're not running it, just referencing it.
elementToClick.click(functionToRunOnClick);
```
### Scroll Events
Detect when the user scrolls using `.scroll(..)`.

Scroll let's us say, "When the user scrolls, run this code (or better put, run this function)"

```javascript
//We want to watch for scrolls on the window itself.
//Note the lack of quotes -- it's a variable, not a string.
//(window is already created by the browser for us, like document)
$(window).scroll(function () {//again, you can use a variable instead
    //This code will get run a lot! Be careful.
    //Use $(window).scrollTop() to get how far the user has scrolled.
    var distanceScrolled = $(window).scrollTop(); //returns a number
    if (distanceScrolled > 300) {
        //run this code when we're more than 300px down the page.
    }
})
```
## Chaining

When jQuery functions return the element you are operating on, you can chain multiple operations.
```javascript
$('#target').toggleClass('hello').addClass('roar').removeClass('meow');
```

# jQuery Getters & Setters
Getters/Setters are a common theme throughout jQuery. They are functions that, when given no parameter, return ("get") the value. When given a parameter, they "set" the value.

## `.text(..)`

#### Getting Text
Pass no value to `.text()` to **get** the element's text.

```javascript
var userName = $('input#userName').text();
```

#### Setting Text
Pass a string to **set** the element's text.
```javascript
$('#set-my-text').text('Text set!');
```

### Putting it together

```javascript
//Get the name the user typed in.
var userName = $('input#userName').text();
//Make sure that user name exists.
if (userNotFound(userName)) {
    $('#statusBox').text('That user name was not found.');
} else {
    //User exists.. do login, or what have you
}
```
## Project: Unread email tracker

Write some javascript that changes the title of a page to reflect the number of unread emails, like Gmail does.


## `html`

```javascript
$('#messageBox').html('This is a message with <strong>strong</strong> elements in it, and a <a href="example.com">link</a>. It overwrote whatever was in the messagebox')
```

# Creating and Appending Elements
The jQuery function, when given html rather than a css selector, will create the html.
## Creating elements
#### Create a div
```javascript
var newDiv = $('<div>');//make me a div and save it in `newDiv`
//newDiv is not yet a part of the dom! it only exists in the JS.
newDiv.text('Text inside the div, brah.').click(function () {..});
```
#### Create an h2
```javascript
var newH2 = $('<h2>').text('This is a heading');
//OR
var otherH2 = $('<h2>This is a heading</h2>');
```

## Appending Elements (Inserting into DOM, etc)
Append inserts things as the last element in the target.
### `appendTo`
To append an element, call its `appendTo` function, passing the element you want to append it to.

```javascript
var h1 = $('<h1>').text('My Webpage');
var body = $('body');
h1.appendTo(body);
```

### `append`
This code does the same as the code above.

```javascript
var h1 = $('<h1>').text('My Webpage');
var body = $('body');
body.append(h1);
```

## Prepend
Same functionality as `append`, but inserts it as the **first** element in the parent.
### `prependTo`
### `prepend`


## insertBefore & insertAfter
```html
<div class="container">
  <h2>Greetings</h2>
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```
```javascript
$( "<p>Test</p>" ).insertAfter( ".inner" );
```
```html
<div class="container">
  <h2>Greetings</h2>
  <div class="inner">Hello</div>
  <p>Test</p>
  <div class="inner">Goodbye</div>
  <p>Test</p>
</div>
```
-----------------------------
```javascript
//Insert a new li at the 5th position.
$( "<li>Test</li>" ).insertAfter( "li:nth-child(4)" );
```

# Removing elements from the dom
## `remove`
```javascript
$('#deleteMe').remove();
```

## `unattach`
Unattach removes the element from the DOM, but does not delete it.
That way, we can save it in a variable, and reattach (append, prepend, insert, etc) it later.
```javascript
var keepForLater = $('#keepMe').unattach();
```




# Inputs: A quick look at forms

```html
<!-- Notice: No closing tag -->
<input>
```

## Input Types
`type` attribute

```html
<!-- the default -->
<input type="text">
```

```html
<!-- hides the text entered into it -->
<input type="password">
```

## Accessing Input Values via jQuery

```html
<input type="text" id="userName" placeholder="User Name">
```

```javascript
//Get whatever has been typed into the #userName element.
var userNameValue = $('#userName').val();
```

`val` is a getter/setter.

```javascript
//Enter 'Bob Smith' into the #userName element.
$('#userName').val('Bob Smith');
```

## Project: Ghost login screen
