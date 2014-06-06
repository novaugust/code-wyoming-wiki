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

------------------------------------------------------
#Forms

##The Form Element

* action:
        URL or file name/path for server-side processing script
        
        Alternatively, use "mailto" to open the user's default email client with your info
* method: get / post
* autocomplete: on/off (html5)

## Form Controls

### Form control attributes
* name
* value
* readonly
* required (html5)
* placeholder (html5)

### Input

##### Input "type"
* text (default)
* checkbox
* hidden
* password
* radio
* reset
* submit
* button
* email (html5)

#### Radio, Checkbox

* checked

#### Buttons
In ye old times, inputs were used as buttons. Now, we have the button element.

type
The type of the button. Possible values are:
submit: The button submits the form data to the server. This is the default if the attribute is not specified, or if the attribute is dynamically changed to an empty or invalid value.
reset: The button resets all the controls to their initial values.
button: The button has no default behavior. It can have client-side scripts associated with the element's events, which are triggered when the events occur.

Value is the text to be shown on the btn


### Textarea
opens & closes!

### Select & Option
####Select

* name
* visible (defaults to 1)

* Select has the name
* Options have the values
* Text inside option is displayed to user

## Label
Uses "for" to link to IDs of form controls

## Fieldset & Legend elements
### Fieldset
Groups fields together in a lovely box
### Legend
A heading for each fieldset. Should be the first thing in a fieldset (it's optional though)

-------------------------------------------------------
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