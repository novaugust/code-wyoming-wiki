# jQuery

## document.ready

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


# Forms
[Convenient form processor / tester](http://www.cs.tut.fi/cgi-bin/run/~jkorpela/echo.cgi?meow=woof)
See also [forms.md](https://github.com/PitchEngine/code-wyoming/blob/master/Week%205/Day-25/forms.md)


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
* submit
* reset
* file
* hidden
* date 5
* time 5
* number
* color

##### Radio
##### Checkbox

### Dropdowns (select)

* `optgroup`

### Textarea

## Labels

## Fieldset & legend

## Styling forms


# Accessing forms with javascript