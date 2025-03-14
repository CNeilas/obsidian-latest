## Static and relative positioning

The default position mode that we are used to is `position: static;`. The difference between `static` and `relative` is that `static` the default position of every element and cannot use `top` `right` `bottom` `left`. The relative on the other hand is pretty much the same as static, except it can use `top` `right` `bottom` `left` positions.

## Absolute positioning

`position: absolute;` allows you to position something at an exact point on the screen without disturbing the other elements around it. This removes element from the normal document flow while being positioned relative to an ancestor element. They are also not affected by other elements as well. Using `absolute` position allows you to use `top` `left` `bottom` `right` and is very usefull when you want modals, images with captions or icons on top of elements. 

## Fixed positioning

Fixed position is removed from the normal flow of the document and is positioned relative to the viewport. You can use `top` `right` `bottom` `left` to position the element and it will stay in the same place on the screen as the user scrolls.

## Sticky positioning 

This is similar to a fixed element but it is not taken out of the normal document flow. `sticky` elements act like normal elements until you scroll past them, then they start acting like fixed elements.

https://www.theodinproject.com/lessons/node-path-intermediate-html-and-css-positioning  This is for when I want to get a bit more deep into this, for now i just want to progress to the projects and js.