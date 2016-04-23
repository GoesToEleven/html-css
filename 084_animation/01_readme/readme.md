CSS Animations

[Read more about it here](https://developer.mozilla.org/en-US/docs/Web/CSS/animation)

[See its browser support here](http://caniuse.com/#search=animation)

# CSS Animation

A css property which is shorthand for the following properties - this shows the properties and their default values:
* animation-name: none
* animation-duration: 0s
* animation-timing-function: ease
* animation-delay: 0s
* animation-iteration-count: 1
* animation-direction: normal
* animation-fill-mode: none
* animation-play-state: running

# animation-name

## default value: none

The animation-name CSS property specifies a *list of animations* that should be applied to the **selected element**. 

Each name indicates a **@keyframes** at-rule that defines the property values for the animation sequence.

Examples:

```css
animation-name: none;
animation-name: test_05;
animation-name: -specific;
animation-name: sliding-vertically;

animation-name: test1;
animation-name: test1, animation4;
animation-name: none, -moz-specific, sliding;

animation-name: initial
animation-name: inherit
animation-name: unset
```
