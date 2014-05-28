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



## Modals



## Tooltips
Opt-in

# [LESS](http://lesscss.org/)

Less is a CSS Pre-compiler. It lets us write powerful CSS-like code that is then *compiled* (converted) into code.
We do not link directly to our LESS code from our HTML. Instead, we add an extra step that compiles our LESS to CSS.
Brackets has a plugin that automaticallyour LESS code into CSS.


Why would we want something like this?

## [Nesting](http://lesscss.org/features/#features-overview-feature-nested-rules)

If our html was like so...

```html
<header>
    <h1></h1>
    <h2></h2>
    <p></p>
</header>
```

Instead of writing a series of selectors like this in our css

```css
header h1 {...}
header h2 {...}
header p {...}
```

We can write this
```less
header {
    h1 {...}
    h2 {...}
    p {...}
}
```

## [Variables](http://lesscss.org/features/#features-overview-feature-variables)

We want our CSS to be consistent, that is, use the same colors over and over. The downside to this is, we have to re-write our code, meaning we have very WET CSS by its nature.

With LESS, we can instead save our value to a **variable** and reuse that variable. Later, if we want to change our colors, we only have to change it in one place.

```less
@nice-blue: #5B83AD;
@light-blue: @nice-blue + #111;

#header {
  color: @light-blue;
}
```

LESS takes that code and writes this CSS for us.

```css
#header {
  color: #6c94be;
}
```


## [Mixins](http://lesscss.org/features/#features-overview-feature-mixins)
## Imports