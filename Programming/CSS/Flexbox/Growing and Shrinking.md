`flex` is a shorthand property.  `flex: 1;` equates to `flex-grow: 1;` `flex-shrink: 1;` `flex-basis: 0;` or `flex: 1 1 0;`

## Flex Grow

`flex-grow` is makes the element grow relatively to the other elements until theres no space anymore.

```
.flex-container {
  display: flex;
}

/* this selector selects all divs inside of .flex-container */
.flex-container div {
  background: peachpuff;
  border: 4px solid brown;
  height: 100px;
  flex: 1 1 0%;
}

/* only div.two is selected here */
.flex-container .two {
  flex: 2 1 0%;
}
```

![[flex_grow.png]]

## Flex Shrink

`flex-shrink` shrinks the items if their size becomes bigger than the parent. You can specify the item's shrink value to either not shrink or shrink less in relation to other elements.

```
.flex-container {
  display: flex;
}

/* this selector selects all divs inside of .flex-container */
.flex-container div {
  background: peachpuff;
  border: 4px solid brown;
  height: 100px;
  width: 250px;
  flex: 1 1 auto;
}

.flex-container .two {
  flex-shrink: 0;
}
```

![[flex_shrink.png]]

## Flex Basis

`flex-basis` sets the initial size of the item. If `flex-basis: 0;` on the container the items will shrink evenly, if we want the item to respect the width value when shrinking and specify an item to not shrink the container should have `flex-basis: auto;`

Flex basis on 0:

![[flex_even.png]]

Flex basis on auto:

![[flex_shrink.png]]

