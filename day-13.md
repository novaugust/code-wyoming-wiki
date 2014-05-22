SUPER ADVANCED CSS!! Or,

#Let's break the interwebs.

## Transitions

##FLEXBOX!
[Guide](http://css-tricks.com/snippets/css/a-guide-to-flexbox/)
[CanIUse Flexbox?](http://caniuse.com/flexbox)

### flex container
CSS for the demo:
```css
.flex-item {
    padding: 2%;
    margin: 1em;
    background: rgba(0, 0, 0, 0.3);
    border-radius: 1em;
}
```
1. display: flex | inline-flex

2. flex-direction: row (default) | column | row-reverse | column-reverse;
    row is left to right
3. flex-wrap: nowrap (default) | wrap | wrap-reverse (check these out in row, not column)
    By default, flex items live on one line.

3.5 shorthand
```
flex-flow:  <‘flex-direction’> || <‘flex-wrap’>
```

4. justify-content: flex-start | flex-end | center | space-between | space-around

    flex-end : align to the end of the container (right or bottom, depending on direction)
    flex-start: reverse of end
    center: obvious
    space-between: justified on each line, with first and last at edges
    space-around: equal amount

5. align-items: flex-start | flex-end | center | baseline | stretch (default)
    Check these guys out with a column. Align-items works on the "cross axis", vs the "main axis" that justify content uess

6. align-content: 
    Make sure flex-wrap is `wrap` or `wrap-reverse`

### Flex items
First off: vertical centering!!!!
margin: auto;
black magic
```css
/* VERTICAL CENTERING! ZOMG! */
.parent {
  display: flex;
  height: 300px; /* Or whatever */
}

.child {
  width: 100px;  /* Or whatever */
  height: 100px; /* Or whatever */
  margin: auto;  /* Magic! */
}
```
1. order
2. flex-grow (0)
3. flex-shrink (1)
4. flex-basis (length)
5. shorthand
```css
flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
```



6. align-self
#### Project: rebuild casey's project with flexbox?
Copy the html directly.
Copy css, but remove all margin/width/display/float code.