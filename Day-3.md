#Day 3 Agenda

Itinerary
-------------
#### 0900
##### Review Multipage Websites
Go over the class's websites together.

#### 1000
##### Wrap up HTML

* Nested lists

#### 1030
##### Intro to CSS

* Advantages
    * Separate style from structure
    * Reuse style
    * Smaller html files
* Types of CSS
    * Inline
    * Embedded
    * External
    * _Imported_
* CSS Syntax
    Rules, selectors, declarations

#### 1100
##### CSS Colors

* color & background-color properties
* color values
* hex
* hex shorthand
* rgb
* hsl

##### Project! Inline CSS via the `Style` attribute
1. Create a simple webpage with a single heading and paragraph.
2. Set the heading to be "Inline CSS" and the paragraph to say "This paragrpah inherits the styles applied to the body tag."

3. Finally, set some styles.
4. Give the body a background color of `#F5F5F5` and set its text's color to `#008080`.
5. Give the h1 the same properties, but swap the colors (set its background to `#008080` and color to `#F5F5F5`)
6. Launch the browser and check things out. 
7. Add another paragraph, with a color of `#333`. Give it the text "This paragraph overrides the text color style applied to the body tag".
8. Never use inline styles in this class ever, ever again.


##### Embedded CSS

* The `style` element.

###### Project! Coloring your website

1. Create a copy of your multipage website project from yesterday.
2. Open up the homepage.
3. Use embedded styles to set a background-color and color for your body, h1, and h2.

#### 1300
##### Text Properties

* `font-family`
    * serif
    * sans-serif
    * monospace
    * cursive
    * fantasy
* Custom fonts
    `@font-face {font-family:SomeFont;, src:url(somefont.woff) format("woff");}`
    See also [google fonts](http://google.com/webfonts) and [font squirrel](http://fontsquirrel.com)
* `font-weight`
* `font-style`
* `line-height`
* `text-align`
* `text-decoration`
* `text-transform`
* `text-transform`
* `white-space`

##### Dimensions in CSS
* px, em, rem, %
* `font-size`
* `text-indent`
* `text-shadow` horizontal offset, vertical offset, blur radius, color


##### Project! Setting the text on your embedded CSS Page
Keep using the file you set the colors on previously. Now, add some new rules.
###### the h1

Give your h1 "double spacing" with a line-height of 200%.
Give it a font-family of your choice, with a fallback.
Apply a text-shadow, play around to find something you like. I recommend a color of #CCC.

###### h2s
Try aligning your h2s in the center, and giving them the same font as your h1

###### Paragraphs
Give your paragraphs an indentation of 3em or so.
Try giving them a font size that's just under the normal, or just over if you prefer. ie, a .9 or 1.1 em

###### Lists
Make your ul / ol / dl, whichever, have a font-weight of bold. We're going to use inheritance here to let the list-items pick that up from their parent.

#### 1430
##### Complex selectors

* `,` the comma selector, "AND"
* the `class` attribute and `.`
* the `id` attribute and `#`
* naming things
* descendant selector: ` `
* span

##### Mini-Project!

Give a "featured" class to some (but not all) of your list items. Then write a selector that "calls-out" those items, perhaps by turning them red-ish (`#C70000`).
Check out your handiwork.
Next up, choose a special phrase in your text. Maybe it's your name or some other combination of words that are significant. Wrap that phrase in a span, give it a class, and write a selector on that class that makes the font bold and large.

##### External Style Sheets

* `link` element
* style.css
###### Mini-project!
Create a page with a single paragraph, and an external stylesheet. Just set the background-color and the color of the body in the stylesheet. The trick here is making sure you're correctly using the `<link>` element.

##### Project! Use an external sheet for your multipage site
Move your embedded CSS into its own file, and create a `link` element in each of your webpages that links to that file.

#### The "Cascade"
* or, CSS's _rules of precedence_

` Browser defaults < External < embedded < inline < attributes `


#### 15:59
##### Bonus Lesson: Centering Webpages

There are three steps to centering content in a webpage.
1. Put your content in a div or other block element container.
2. Set the width of that element to be less than the full width of the page.
3. Set the left and right margins of the container to be automatically calculated to share extra space.

__index.html__
```html
<body>
    <div id="wrapper">
        <h1>This is the heading</h1>
        <p>This is your content</p>
    </div>
</body>
```
__style.css__
```css
#wrapper {
    width: 80%;
    margin-left: auto;
    margin-right: auto;
}
```
Try making your browser wider and smaller, and then change your code so that the `width` is `700px` and try resizing your browser again. We'll talk about what this difference means next time.

