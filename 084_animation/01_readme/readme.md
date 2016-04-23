CSS Animations

[Read more about it here](https://developer.mozilla.org/en-US/docs/Web/CSS/animation)

[See its browser support here](http://caniuse.com/#search=animation)

# CSS Animation

A css property which is shorthand for the following properties - this shows the properties and their default values:
* animation-name: none
* animation-duration: 0s
* animation-iteration-count: 1
* animation-direction: normal
* animation-timing-function: ease
* animation-delay: 0s
* animation-fill-mode: none
* animation-play-state: running

# animation-name

**default value: none**

The animation-name CSS property specifies a *list of animations* that should be applied to the **selected element**. 

Each name indicates a **@keyframes** at-rule that defines the property values for the animation sequence.

Examples:

```css
animation-name: none;
animation-name: test_05;
animation-name: test1;

/* Multiple animations */
animation-name: test1, animation4;

/* Global values */
animation-name: initial
animation-name: inherit
animation-name: unset
```
# @keyframes

The **@keyframes** CSS at-rule lets authors control the intermediate steps in a CSS animation sequence by establishing **keyframes** (or waypoints) along the animation sequence that must be reached by certain points during the animation. 

To use keyframes, you create a **@keyframes** rule with a **name** that is then used by the **animation-name** property to match an animation to its keyframe list. 

```css
body {
    animation-name: change-color;
}

@keyframes change-color {
  0% { color: red; }
  100%   { color: gold; }
}
```

Each **@keyframes** rule contains a **style list** of keyframe selectors, each of which is comprised of a percentage along the animation at which the keyframe occurs as well as a block containing the style information for that keyframe.

You can list the keyframes in any order; they will be handled in the order in which their specified percentages indicate they should occur.

You can also use the "from" and "to" keywords:

```css
body {
    animation-name: change-color;
}

@keyframes change-color {
  from { color: red; }
  to   { color: gold; }
}
```

In order for a keyframe list to be valid, it must include rules for at least the times 0% (or from) and 100% (or to) (that is, the starting and ending states of the animation). If both of these time offsets aren't specified, the keyframe declaration is invalid; as such, it will be ignored by the parser and can't be used for animation.

If you include properties that can't be animated in your keyframe rules they get ignored, but supported properties will still be animated.

# animation-duration

**default value: 0s**

The animation-duration CSS property specifies the length of time that an animation should take to complete one cycle.

Examples:

```css
animation-duration: 6s;
animation-duration: 120ms;

/* Multiple animations */
animation-duration: 1s, 15s;
animation-duration: 10s, 30s, 230ms;
```

# animation-iteration-count

**default value: 1**

The animation-iteration-count CSS property defines the number of times an animation cycle should be played before stopping.

```css
animation-iteration-count: infinite;
animation-iteration-count: 3;
animation-iteration-count: 2.3;

/* Multiple animations */
animation-iteration-count: 2, 0, infinite;
```
# animation-direction

**default value: normal**

The animation-direction CSS property indicates whether the animation should play in reverse on alternate cycles.

```css
/* Single animation */
animation-direction: normal;
animation-direction: reverse;
animation-direction: alternate;
animation-direction: alternate-reverse;

/* Multiple animations */
animation-direction: normal, reverse;
animation-direction: alternate, reverse, normal;

/* Global values */
animation-direction: inherit;
animation-direction: initial;
animation-direction: unset;
```
