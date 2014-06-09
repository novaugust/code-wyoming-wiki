# Styling Forms

See [mdn form styling guide](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms/Styling_HTML_forms) and mdn [advanced form styling](

### `:checked`, the `+` selector, and `<label>`

### `:focus`

### `[type=...]`

### search boxes
Don't ask me. Just do it.
```css
input[type=search] {
-webkit-appearance: none;
}
```

### font normalizing
```css
button, input, select, textarea {
  font-family : inherit;
  font-size   : 100%;
}
```

# more jQuery




## `attr`

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




## Styling forms

# Accessing forms with javascript