# jQuery

## Document Ready

## Selecting Elements


## Attributes
Object as param

### Aside: jQuery getters and setters

Setters return jQuery object for chaining

### .data

## .html and .text

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

## Element traversal

* first
* eq
* find
* parent

# Forms

## How forms work
Server & Client
## The `form` element
### Form Attributes
#### Action

#### Method

* get (default)
   The data sent via get requests is tacked onto the URL sent to the server, separated by a question mark. This is appropriate for allowing users to bookmark the location of what they were sent to. It has a length limit.
* post
    Post is best for secure data, like credit cards or other personal info. It's also preferable for sending large amounts of data.

## Variables Names and Values
* name
* value

## Form controls
### Common Attributes
* name
* value
* placeholder (html5)

### Input

```html
<input list="edulevel" type="text" name="education">
<datalist id="edulevel">
    <option value="High School">
    <option value="Bachelors">
</datalist>
```

#### Types

* password
* search (5)
* email (5)
* tel (5)
* url (5)

### Textarea


## Styling forms


# Accessing forms with javascript
