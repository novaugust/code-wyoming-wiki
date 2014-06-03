# jQuery

## Document Ready

## Selecting Elements


## Attributes
Object as param

### Aside: jQuery getters and setters

Setters return jQuery object for chaining

### .data

## .html and .text

## Element traversal

* first
* eq
* find
* parent

## Class manipulation

* addClass
* removeClass
* toggleClass
* hasClass

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


# Forms

## Input
## Textarea
## Styling forms


# Accessing forms with javascript
