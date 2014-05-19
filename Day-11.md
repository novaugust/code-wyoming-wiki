### Main project
Finishing & fluid-izing the landing page

#### Wrap ups:
##### Links: 
* The `target` attribute
* `sms`
* `tel`
* fragment links (`#`)
*  html5 block links


##### Linear-Gradient
1. Gradients are background images.
2. Direction can be set with first parameter, `to right` or `to bottom left`. Alternatively, degrees can be specified with the `deg` unit, as in, `45deg`
3. Color stops: fake columns
```css
linear-gradient(
      to right, 
      #fffdc2,
      #fffdc2 15%,
      #d7f0a2 15%,
      #d7f0a2 85%,
      #fffdc2 85%
    );
```
##### Multiple Background Images
Commas, yo!
##### Browser prefixes
```css
background-color: #8FA5CE;

background-image: url(linear-pic.png); 
background-repeat: repeat-y;

filter: progid:DXImageTransform.Microsoft.gradient(startColorstr=#FFFFFFFF, endColorstr=#FF8FA5CE);
background: -o-linear-gradient(#FFFFFF, #8FA5CE);
background: -moz-linear-gradient(#FFFFFF, #8FA5CE);
background: -webkit-linear-gradient(#FFFFFF, #8FA5CE);
background: linear-gradient(to bottom, #FFFFFF, #8FA5CE);
```

##### Favicon
Simply place a file named exactly `favicon.ico` in your root directory, or link to an image with the link tag. (Web standards prefer the second route, see [here](http://www.w3.org/2005/10/howto-favicon))
* 16x16 or 32x32
* 8bit or 24bit
* `.ico`, `.png`, or `.gif`

```html
<link rel="shortcut icon" href="myfavicon.ico" type="image/x-icon">
<link rel="icon" href="myfavicon.ico" type="image/x-icon">
<link rel="icon" href="myfavicon.png" type="image/png">
<link rel="icon" href="myfavicon.gif" type="image/gif">
```


##### Gallery Project Revisited
We're going to use absolute positioning to make our galleries more interactive.

1. Add a second image tag to each li. 
   a. Give the new image a class of "full". 
   b. Set the full class to have  `display: none;` by default.
2. Make room for the large images to show up on the right side of the screen - make your thumbs take up a smaller percentage of real estate
3. Set the `.full` images to be absolutely positioned in the blank space (might be helpful to turn their display back on until you have them in place)
4. Set a hover rule that makes the correct full image to become visible.


##### Pseudo-elements
* `::before`
* `::after`
* `::first-letter`
* `::first-line`

```css
p::first-line {
    text-transform: uppercase;
    font-size: .9em;
}
```
