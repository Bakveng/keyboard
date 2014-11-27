TEST

# A Parallax JavaScript library based on HTML / CSS

[Demo](http://razorfish.github.com/Parallax-JS)

## Usage

Any `<section>` tag, along with any element with the `animate` class is parsed for parallax effects.  `<section>` tags are assumed to line up one-after-another, all other tags can have any effect desired.

### Animation States

To define an animation, simply add several custom css classes in your stylesheet that control the state of an element at one point in time.  Animations are automatically generated between these states:

- `.start` -- The style of the element when the `<section>` tag first comes into view
- `.focus` -- The style of the element with the `<section>` tag fills the screen
- `.to` -- The style of the element when the `<section>` anim-delay is over
- `.end` -- The style of the element when the `<section>` tag is just leaving the view

### Other Controls

Add properties to your elements, e.g. `<section anim-pause="200">`

- `anim-pause` -- How long to pause at this element
- `anim-detached` -- Set to `true` if this element should not add to the page scroll length (In other words, it still gets animated, but is dependent on usually parent elements)
- `anim-speed` -- Speed multiplier for the animation.  Defaults to `1`
- `onFocus` -- Global JS function name to call when the animation comes into focus
- `onBlur` -- Global JS function name to call when the animation leaves focus
- `data-nav` -- Name for navigation sidebar.  Overrides default generated by `side-nav.js`

### Side Navigation

include `side-nav.js` to add an auto-generated side navigation bar.  This bar is generated from all `section h2:first` elements.

##Features

All animations are done using CSS3 transformations whenever possible and fall back to normal CSS positioning when necessary.