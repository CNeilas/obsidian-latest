## Child and sibling combinators

`>` - the child combinator.
`+` - the adjacent sibling combinator
`~` - the general sibling combinator

```
main div {
	css here... // the divs inside the main are selected
}

main > div {
	css here // only the divs that are children of main are selected
}

main > div > div {
	css here // the divs that are grandchildren of main or children of divs that are children of main are selected
}

.group1 + div {
	css here... // the divs that come right after .group1 classes are selected
}

.group1 + div + div {
	css here... // the divs that come after divs that come after .group1 are selected
}

.group1 ~ div {
	css here... // all div siblings of the .group1 are selected
}
```

## Pseudo-classes

### Dynamic and user action pseudo-classes

`:focus` applies to an element that is currently selected by the user.

`:hover` will affect anything under the user's mouse pointer.

`:active` applies to elements that are currently being clicked.

`:link` applies to unvisited links.

`:visited` applies to links that the user has already clicked.

### Structural pseudo-classes

These are classes based on their position within the DOM.

`:root` is a special class that represents the very top level of the document. This is (almost) equvalent to the html element. This is where you place global CSS rules.

`:first-child` and `:last-child` will match elements that are the first or last sibling.

`:empty` will match elements that have no children at all.

`:only-child` will match elements that dont have any siblings.

`:nth-child` is a bit more flexible:

```
.myList:nth-child(5) {// selects the 5th element with class .myList}
.myList:nth-child(3n) {// selects every 3rd element with class .myList}
.myList:nth-child(3n + 3){// selects every 3d element beginning with 3rd one in .myList}
.myList:nth-child(even) {// selects every even element with class .myList}
```

## Pseudo-elements

`::marker` allows us to customize the styling of `<li>` elements bullets or numbers.

`::first-letter` and `::first-line` allow you to give styling to the first letter or first line of some text.

`::selection` lets you change the highlighting when a user selects text on the page.

`::before` and `::after` allows us to add extra elements onto the page with CSS. We can use this to decorrate text.

```
.emojify::before {
	content: 'something that comes before text';
}

.emojift::after {
	content: 'something that comes after text';
}
```

## Attribute selectors

`[attribute]` - This will select anything where the given attribute exists.

`selector[attribute]` -Optionally we can combine this with selectors.

`[attribute="value"]` - This gets really specific as it matches both attribute and the value of it.

```
[src] {
	this will target any element that has a src attribute
}

img[src] {
	this will only target images with src
}

img[src="puppy.jpg"] {
	this will target elements with a src attribute that is exactly "puppy.jpg"
}
```

`[attribute^="value"]` - `^=` will match strings from the start.
`[attribute$="value"]` - `$=` will match strings from the end.
`[attribute*="value"]` - `*=` will match from anywhere in the string.
