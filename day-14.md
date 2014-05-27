## Tables
### Table children
* caption
* colgroup
* thead
* tbody
* tfoot

#### Grand Children
* tr
* td
* th

## Transforms
[CSS Tricks:Transform](http://css-tricks.com/almanac/properties/t/transform/)
[Transforms + Transitions](http://css3.bradshawenterprises.com/transforms/)
Transformed elements still occupy their original space (like relative elements)

* transform-origin: x y;

### Transform
Multiple transformations just need spaces

* matrix (?!?)
* rotate(angle)
* translateX, translateY, translate(x, y)
* scale(sx[, sy]), scaleX, scaleY  (angle)

## Animations
### Animation property
Animations are a W3C working draft! Check out the CanIUse for them.

[CanIUse Css Animation?](http://caniuse.com/css-animation)

[CSS Tricks Animation Tricks](http://css-tricks.com/css-animation-tricks/)

[Animations on MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Using_CSS_animations)


* animation-duration
* animation-delay
    Time between element loading and beginning of animation (5s)
* animation-direction: normal (default) | reverse |alternate | alternate-reverse |   
* animation-iteration-count
    How many times to repeat; `infinite` is an option here
* animation-name
    Link to your keyframe
* animation-timing-function
    This is a big deal. See [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-timing-function)
    
```
.element-to-animate {
  animation: NAME-YOUR-ANIMATION 5s infinite;
}
```
### Keyframes
Use commas if you have shared start and stops
```css
@keyframe your-animation-name {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}
```
If you have just two stops, use `from` and `to`.

## Bootstrap
### Helper classes