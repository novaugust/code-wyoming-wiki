# Bootstrap Javascript Components

A majority of interactive javascript components use the `data-toggle` attribute to specify which javascript function to use, and a css selector written in a `data-target` attribute to specify the effect's target.

## Dropdowns

The easiest way to create a dropdown is to create a `.dropdown` container, inside of which you place a `<a href="#" data-toggle="dropdown">` (`button`s are fine too) and after that `<ul class="dropdown-menu">`. 

Dropdowns have three parts.

1. A container with class `dropdown`
2. A button or anchor with the attribute `data-toggle="dropdown"` (and `href="#"` if using anchors).
3. A list element with class `dropdown-menu`

## [Tabs](http://getbootstrap.com/javascript/#tabs)

Tabs have two main steps.

1. [Style a tab nav-bar](http://getbootstrap.com/components/#nav).

    Set each anchor's href to be pointing at the id of the content you want to display.
2. Create a div with class `tab-content`. Inside of it, place divs with `class="tab-pane"` and set their id to correspond with the links in the navbar. 

    Additionally add the `active` class to the div that should start displayed.

For fanciness, add `fade` to each `.tab-pane` to get a nice transition effect. Add `in` to your initial pane as well, so its class structure would be `tab-pane fade in active`.


## Collapse / Accordion

Collapse works very similarly to the dropdown components.

At its most basic, it needs only two pieces, the button to trigger the collapse, and a container with the content to collapse.

1. On the button, set `data-toggle="collapse"` and `data-target="#example"`
2. On the content, set its `id="example"` and give it a class of `collapse`.

    You can additionally add the class `in` to make the collapsed content start visible.

Collapse can also use the `data-parent` attribute to specify the parent of multiple collapses. This way, 
    all collapsible elements under the specified parent will be closed when this collapsible item is shown. 

The collapse plugin works really well with the panel component.


## [Navbars](http://getbootstrap.com/components/#navbar)
Bootstrap will make auto-collapsing navbars for us. 

Navbars are all wrapped within a `<nav>` element that has the classes `navbar` and one of either `navbar-default` or `navbar-inverted` depending on the styling you want.

```html
<nav class="navbar navbar-default">
    ...
</nav>
```

From here, we typically insert a `container` or `container-fluid` in the navbar to center and pad the content.

```html
<nav class="navbar navbar-default">
    <div class="container">
        ...
    </div>
</nav>
```

### Navbar Mobile Button
To add a button that opens and closes the menu for mobile views, give it the class `"navbar-toggle"`. Then, use the collapse techniques to have it toggle your display. That is..

1. Add `data-toggle="collapse"` to the button.
2. Add `data-target="#header-content"` to the button.

This button is best placed inside a `div.navbar-header` alongside a brand.
```html
<div class="navbar-header">
  <button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#example-navbar-collapse">
    <span class="sr-only">Toggle navigation</span>
    <!-- draw the hamburger -->
    <span class="icon-bar"></span>
    <span class="icon-bar"></span>
    <span class="icon-bar"></span>
  </button>
  <a class="navbar-brand" href="#">Brand</a>
</div>
```

### Navbar Fullscreen content

All content you want displayed only on larger screens belongs inside of a div with two classes. 

1. The first is `collapse`, which hides the content and makes for smooth toggling with buttons.

2. The second is `navbar-collapse`, which overrides collapse and displays the content on larger screens.


#### Navbar content styling

Use `navbar-left` and `navbar-right` to align menu items.

Navs should still be in unordered lists, with the BS classes of `nav` and `navbar-nav`

### [Fixed Navs](http://getbootstrap.com/components/#navbar-fixed-top)

Fix a nav by adding the `navbar-fixed-top` or `navbar-fixed-bottom` classes. Keep in mind, you'll need to add padding to the body to keep content behaving.

## Carousels

Carousels begin with a container that must have an ID on it to work properly. The carousel should also have a class of `carousel`. Finally, use the `data-ride="carousel"` property to kick in the javascript.

(Note: On the examples, carousels also have a `slide` class. I couldn't find that it actually did anything.)

```html
<div id="my-carousel" class="carousel" data-ride="carousel">
    ...
</div>
```

Inside of the carousel container you will place three separate components.
They are:

1. The carousel indicators.
2. The carousel content.
3. The carousel controls.

### Carousel indicators
The carousel indicators are the nice little dots that indicate which position you are at within the carousel. They are made from an ordered list with class `carousel-indicators`

Within the ordered list, each `li` will have two data properties
1. data-target="#my-carousel" (or whatever your carousel container's ID is)
2. data-slide-to="0" (the slide number each li corresponds to, start with the first slide being "0")

Finally, the carousel indicator that is active when the screen loads should have a class of `active`.

### Carousel Content
The carousel's content (that is, the slides themselves) go within a `div.carousel-inner`.
Inside of that, you will repeat this pattern for each slide:

1. Give the slide a container with class `item`
2. Place an image in the container
3. Add the `active` class to the slide that starts visible.

#### Slide captions
If you want to add captions to your slides, do the following. 

1. Add an additional div within the `div.item`, after the `img` tag.
2. Give this div a class of `carousel-caption`
3. Add whatever content you want over the slide within the `carousel-caption`
4. *Et voila*.

### Carousel controls
The carousel controls should go at the end of your `carousel` container. The code is fairly generic, so I'm just going to copy and paste it below. 
The things you want to be careful of are the `data-slide`, `href` and `class` attributes on each `a` tag. The content within each tag is up to you; in this examle, we're seeing bootstraps default *glyphicon* spans.

```html
<a class="left carousel-control" href="#carousel-example-generic" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left"></span>
  </a>
  <a class="right carousel-control" href="#carousel-example-generic" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right"></span>
  </a>

```

### Multiple carousels
This is why you must give each carousel an ID for things to work correctly. As long as you assigned unique IDs, things will work well.

## Modals



## Tooltips
Opt-in
