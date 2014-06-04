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




-------------------------------------

## Document Ready

## Attributes
Object as param

### Aside: jQuery getters and setters

Setters return jQuery object for chaining

### .data

## .html and .text


## Manipulating elements
### Moving elements
// Moving elements using different approaches.
 
// Make the first list item the last list item:
var li = $( "#myList li:first" ).appendTo( "#myList" );
 
// Another approach to the same problem:
$( "#myList" ).append( $( "#myList li:first" ) );
 
// Note that there's no way to access the list item
// that we moved, as this returns the list itself.

### Cloning
// Making a copy of an element.
 
// Copy the first list item to the end of the list:
$( "#myList li:first" ).clone().appendTo( "#myList" );

## Element traversal

* first
* eq
* find
* parent
