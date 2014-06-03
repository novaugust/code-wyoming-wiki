
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