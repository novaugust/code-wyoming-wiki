# Itinerary
###9 
Code Review! Look at projects from [Day 5](Day-5).

### 1
#### The Box Model

##### Content Box

* `width` and `height`
* avoid % height for now
* total width vs `width`

##### Padding, Border
Nothing new to add!

##### Margin

* Margin collapse
* centering with `auto`

###### Boxes Project
Make a few boxes, some inside others, setting width, height, margin, border, padding, and background-color (to help visualization)

### 2:30
#### Floating

Floats are our first look into doing actual layouts with our code.

##### Normal flow

The browser reads, and displays code, line-by-line, top to bottom

##### Float
The `float` property takes `none | left | right` values.

A floated element...
1) Render's in normal flow order
2) Shifts as far left or right as possible _within its container_
3) When floating a `block` element, be sure to set its `width` property.
4) Elements after the floated element will "bubble" up and around it.
5) Margin is useful to push the "bubbled up" elements away from the floated element.

###### Project!
1. Create a new file
1. Create a div with `id="wrapper"` in your body. We'll use this div to center everything
1. Place an H1 with text "Learning About Floats" inside of the #wrapper div.
1. Place an image with `src="//placekitten.com/200/400"` after the H1.
1. Put a paragraph with two sentences worth of text after the img.
1. Center your wrapper with a width of 640px.
1. Look at your handiwork, and observe normal flow.
1. Create the following classes in your css
```css
.float-left {
    float: left;
}
.float-right {
    float: right;
}
```
Alternate putting `float-left` and `float-right` on your image and see what happens.

###### Clear
The floated elements container may "collapse". We fix that with `clear`.

`clearfix` on ....

* `<br>`
* subsequent content

Using overflow:auto to prevent parent collapse


##### Project
Try the br , overflow, and content clearfixes.


### Homework

Build a website with a left nav.


