DOM is a tree-like representation of the contents of a webpage, it's a tree of nodes with different relationships depending on how they are arranged in the HTML document.

![[DOM_Tree.png]]

## Targeting nodes with selectors

This is HTML we will be working with:

```
<div id="container">
	<div class="display"></div>
	<div class="controls"></div>
</div>
```

You target nodes with CSS selectors (don't worry about example syntax, will explain later): 

```
const container = document.querySelector("#container") // selects the div with an id of container

const display = container.firstElementChild // selects the first child of the container element which is a div with display class

const controls = document.querySelector(".controls") // selects div with controls class

const display = controls.previousElementSibling // selects the elements that is before controls
```

## DOM methods

### Query selectors

`document.querySelector(selector)` -  returns a reference to the first match of `selector`.

`document.querySelectorAll(selectors)` - returns a NodeList containing references toall of the matches of the `selectors`.

`document.getElementsByClassName(class)` - returns a collection of elements with the specified class name.

`document.getElementsByTagName(tag)` - returns a collection of elements with the specified tag name.

`document.getElementById(id)` - returns an element with the specified id.

NodeList looks and behaves like an  array but it does not have array methods, you can convert it into an array using `Array.from()` or the spread operator:

```
let array1 = [...NodeList] // this uses spread operator
let array2 = Array.from(NodeList) // this uses Array.from()
```

### Element creation

`document.createElement(tagName, [options])` - creates a new element of tag type tagName. `[options]` - means you can add some optional parameters to the function. // Worry about this later.

`const div = document.createElement("div")` - this does not put your new element into the DOM, it just creates a new element in memory, you can manipulate it by adding styles, text, classes, id's, etc. before placing it on the page.

### Append elements

`parentNode.appendChild(childNote)` - appends childNode as the last child of parentNode.

`parentNode.insertBefore(newNode, referenceNode)` - inserts newNode into parentNode before referenceNode.

### Remove elements

`parentNode.removeChild(child)` - removes child from parentNode on the DOM and returns a reference to child.

## Altering elements

When you have a reference to an element, you can use that to alter the element's properties. This allows you to change classes, add/remove/alter attributes, add styling.

```
// creates a new div
const div = document.createElement("div")
```

### Adding inline style

```
// adds the indicated style rule to the div
div.style.color = "blue" 

// adds several style rules
div.style.cssText = "color: blue; background: white;"

// adds several style rules
div.setAttribute("style", "color: blue; bacground: white;")
```

If you need to access kebab-cased properties like `background-color` with JS, you will need to use camelCase with dot or bracket notation. With bracket notation you can use either kebab or camel cases but the property has to be a string.

```
// dot notation with camelCase
div.style.backgroundColor

// bracket notation with kebab-case
div.style["background-color"]

// bracket notation with camelCase
div.style["backgroundColor"]

// this does not work
div.style.background-color
```

### Editing attributes

```
// if id exists edit it, if does not creates the div
div.setAttribute("id", "theDiv")

// return value of specified attribute
div.getAttribute("id") // theDiv

// removes specified attribute
div.removeAttribute("id")
```

###  Working with classes

```
// adds a new class
div.classList.add("new")

// removes a specified class
div.classList.remove("new")

// if div does not have class then adds it, if it does then removes it
div.classList.toggle("active")
```

It is vest to use toggle as it is cleaner than adding and removing inline CSS.

### Adding text content

```
// creates a text node and inserts in into div
div.textContent = "Hello World!"
```

### Adding HTML content

```
// renders the HTML inside div
div.innerHTML = "<span>Hello World!</span>"
```

It is prefered to use textContent if you only need to add text to avoid potential security risks.