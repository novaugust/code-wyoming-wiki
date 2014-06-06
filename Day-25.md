# jQuery

## document.ready
------------------------------------------------------
#Forms


# Forms

[Convenient form processor / tester](http://www.cs.tut.fi/cgi-bin/run/~jkorpela/echo.cgi)

See also [forms.md](https://github.com/PitchEngine/code-wyoming/blob/master/Week%205/Day-25/forms.md)

##The Form Element

* action:
        URL or file name/path for server-side processing script
        
        Alternatively, use "mailto" to open the user's default email client with your info
* method: get / post
* autocomplete: on/off (html5)

#### Method

* get (default)
    The data sent via get requests is tacked onto the URL sent to the server, separated by a question mark. This is appropriate for allowing users to bookmark the location of what they were sent to. It has a length limit.
* post
    Post is best for secure data, like credit cards or other personal info. It's also preferable for sending large amounts of data.


## Form Controls

### Form control attributes
* name
* value
* readonly
* required (html5)
* placeholder (html5)

### Input
datalist's are cool.
```html
<input list="edulevel" type="text" name="education">
<datalist id="edulevel">
    <option value="High School">
    <option value="Bachelors">
</datalist>
```


##### Input "type"
* text (default)
* checkbox
* hidden
* password
* radio
* reset
* submit
* button
* file

###### Html5 Input Types
* email
* search
* tel
* url
* date
* time
* number
* color

#### Radio, Checkbox

* checked

#### Buttons
In ye old times, inputs were used as buttons. Now, we have the button element.

##### type
The type of the button. Possible values are:
* *submit*: The button submits the form data to the server. This is the default if the attribute is not specified, or if the attribute is dynamically changed to an empty or invalid value.
* *reset*: The button resets all the controls to their initial values.
* *button*: The button has no default behavior. It can have client-side scripts associated with the element's events, which are triggered when the events occur.


### Textarea
Has opening and closing tags, good for large bodies of text.

### Select & Option
####Select

* name
* size (defaults to 1)
* `<select>` has the name attribute
* `<option>`s each have a value
* Text for each option goes between its 
* `<optgroup>` can be used to group options together. use `label` attribute to give them a name.


## Label
Uses "for" to link to IDs of form controls

## Fieldset & Legend elements
### Fieldset
Groups fields together in a lovely box
### Legend
A heading for each fieldset. Should be the first thing in a fieldset (it's optional though)
