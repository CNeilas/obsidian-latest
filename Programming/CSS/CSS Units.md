## Absolute units

`px` is an absolute unit because the size of a pixel doesn't change relative to anything else on the page. This is the only unit you should be using in web projects as other one are inches and centimeters.

## Relative units

Relative units are units that change based on their context. 

### em and rem

`em` and `rem` both refer to a font size, though they are often used to define other sizes. As a rule of thumb, `rem` is prefered.

`1em` is the `font-size` of an element. For example, if the element's `font-size` is `16px`, then setting width to `4em` would be `64px`.

`1rem` is the `font-size` of the root element (either`:root` or `html`). Works same as `em` but we don't need to worry about parent sizes, only the root.

### Viewport units

`vh` and `vw` relate to the size of the viewport. `1vh` is equal to `1%` of the viewport height and `1vw` is equal to `1%` of the viewport width.