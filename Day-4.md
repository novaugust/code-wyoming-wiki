Outline
-----------

* Customizing text project
* CSS: Selectors
* The "Cascade"
* github & git

Itinerary
------------

#### 0900

##### Project! Setting the text on your Multipage website
Keep using the files you set the colors on previously. Now, add some new rules.

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

#### 0930
##### Complex selectors

* `,` the comma selector, "AND"
* the `class` attribute and `.`
* the `id` attribute and `#`
* naming things
* descendant selector: ` `
* `span`

#### 10:30 (Don't forget to take a break)
##### Mini-Project!

Give a "featured" class to some (but not all) of your list items. Then write a selector that "calls-out" those items, perhaps by turning them red-ish (`#C70000`).

Check out your handiwork.

Next up, choose a special phrase in your text. Maybe it's your name or some other combination of words that are significant. Wrap that phrase in a span, give it a class, and write a selector on that class that makes the font bold and large.



##### The "Cascade"
or, CSS's ___rules of precedence___

` Browser defaults < External < embedded < inline < attributes `


#### 11:30
##### Github
Introduction to Github and git.

#### 1300
##### More CSS
* Border
    * width
    * style
    * color
    * TRBL
* Padding
    * TRBL
    * 1, 2, 3, 4 arguments

###### Mini-Project!
__Headings__
* Working with your MPWS, put padding on the h1 (15px looks pretty nice)
* Give your h2s a 2px, dashed bottom border with a color of your choice

__Footer__
* Put a top border on your footer. Make it a solid, "thin" border with a lighter gray color like `#aeaed4`
* Give the footer a bit of padding on the top, around `10px` should be good.
* Try lightening up your footer's text if it's copyright, by changing its color from the default `#000` to `#333`.