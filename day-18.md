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