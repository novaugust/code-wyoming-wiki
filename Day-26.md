# Styling Forms

See [mdn form styling guide](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms/Styling_HTML_forms) and mdn [advanced form styling](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms/Advanced_styling_for_HTML_forms)
## Form Pseudo-Classes

* `:checked`
    Applies to `checkbox` and `radio` inputs.
* `:enabled`
* `:disabled`
* `:invalid`
* `:valid`
* `:focus`

### `:checked`, the `+` selector, and `<label>`
```html
<label>
    <input type="checkbox">
    <span class="checkbox"></span>
    Checkbox Demo
</label>
```

```css
input {display: none;}
/* draw a fake checkbox */
span.checkbox {
    display: inline-block;
    width: 10px;
    height: 10px;
    border: 2px solid gray;
    border-radius: 2px;
    background-color: black;
    cursor: pointer;
}
/* the magic */
input:checked + span.checkbox {
    background-image: url(checkmark.gif);
}
```
###### Example2: EULA

```html
<label for="terms">
       <span class="btn btn-default">Show terms take two</span>
    </label>
    <div id="eula">
       <input type="checkbox" id="terms">
       <h1>End User License Agreement</h1>
       <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias eligendi, dolorem voluptatibus cupiditate. Maiores totam, iusto nisi, minus modi delectus, ipsum veritatis quam nemo obcaecati beatae explicabo officiis tempore, aut?</p>
       <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sunt id debitis sequi placeat amet. Praesentium vel, adipisci consectetur doloribus in, maiores porro aspernatur incidunt illum odit enim, quam voluptate non.</p>
       <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sunt id debitis sequi placeat amet. Praesentium vel, adipisci consectetur doloribus in, maiores porro aspernatur incidunt illum odit enim, quam voluptate non.</p>
       <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sunt id debitis sequi placeat amet. Praesentium vel, adipisci consectetur doloribus in, maiores porro aspernatur incidunt illum odit enim, quam voluptate non.</p>
       <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sunt id debitis sequi placeat amet. Praesentium vel, adipisci consectetur doloribus in, maiores porro aspernatur incidunt illum odit enim, quam voluptate non.</p>
       <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sunt id debitis sequi placeat amet. Praesentium vel, adipisci consectetur doloribus in, maiores porro aspernatur incidunt illum odit enim, quam voluptate non.</p>
   </div>
```
```css
#eula input#terms,
#eula input#terms ~ h1,
#eula input#terms ~ p {
    display: none;
}

#eula input#terms:checked ~ h1,
#eula input#terms:checked ~ p {
    display: block;
}
```

### Attribute Selectors

```css
element[attr=value] {...}

/* real example */
input[type=email] {...}
```

* `^=`  starts with / prefix

```css
a[href^=https]{
    background-image: url(lock.jpg);
}
```

* `$=`  end with / suffix
* `*=`  contains somewhere

* `|=`  end with / suffix
* `~=`  whitespace separated list of things (like how we do the class attr)

```css
/* equivalent */
div.main {}
div[class~=main]{}
```

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

```javascript
var someLinksHref = $('a').attr('href');
var id = $('main').attr('id');
if (!id) {
//main didn't have an id.. let's give it one
    $('main').attr('id', 'mains-new-id');
}
```

### `data`
shorthand for attr('data-xxxx')

```javascript
.attr('data-my-attr')
.data('my-attr');
```

## Manipulating elements
### Moving elements
Moving elements using different approaches.
 
Make the first list item the last list item:
```javascript
$( "#myList li:first-child" ).appendTo( "#myList" );
```
 
// Another approach to the same problem:
```javascript
$( "#myList" ).append($("#myList li:first-child"));
```
 
// Note that there's no way to access the list item
// that we moved, as this returns the list itself.

### Cloning
Making a copy of an element.
 
Copy the first list item to the end of the list:
```javascript
$( "#myList li:first" ).clone().appendTo( "#myList" );
```

## Element traversal


* eq
* first

```javascript
$('p').eq(0).addClass('lead'); //get the first p
$('p').first().addClass('lead'); //get the first p
```

* find
```javascript

$('footer').find('a'); //same as $('footer a');

var getLinks = function (element) {
    returns element.find('a');
}
```

* parent

```
$('li').parent(); //returns the immediate parent, so hopefully a ul...

$('nav > ul > li > a').parent().parent().parent(); //the nav
```