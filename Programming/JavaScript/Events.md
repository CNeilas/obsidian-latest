There are three primary ways to dynamically use [[DOM Manipulation]]:
1. You can specify function attributes directly on your HTML elements.
2. You can set properties in the form of on `<eventType>`, such as `onclick` or `on mousedown`, on the DOM nodes in your JavaScript.
3. You can attach even listeners on the DOM nodes in your JavaScript.

## Method 1

`<button onclick="alert('Hello World')">Click Me</button>`

This method is not preferred since it clusters HTML with uneccessary code and we can only attach one method per HTML element.

## Method 2

```
<!-- the HTML file -->
<button id="btn">Click Me</button>
```

```
// the JavaScript file
const btn = document.querySelector("#btn")
btn.onclick = () => alert("Hello World")
```

This is a little better since we are moving the JavaScript to a separate file, but it still leaves the problem of being able to only put one method per element.

## Method 3

```
<!-- the HTML file -->
<button id="btn">Click Me</button>
```

```
// the JavaScript file
const btn = document.querySelector("#btn")
btn.addEventListener("click", () => {
	alert("Hello World");
})
``` 

This method is a tad bit more complex, but it allows us to put multiple event listeners on one element and separates JavaScript from HTML.

These methods can also be used with named functions as well:

METHOD 1:

```
<!-- the HTML file -->
<button onclick="alertFunction()">Click Me</button>
```

```
//METHOD 1
const alertFunction = () => alert("YAY, YOU DID IT!")
```

METHOD 2 & 3:

```
<!-- the HTML file -->
<button id="btn">Click Me</button>
```

```
// METHOD 2 & 3

const alertFunction = () => alert("woohoo")
const btn = document.querySelector("#btn")

// METHOD 2
btn.onclick = alertFunction

// METHOD 3
btn.addEventListener("click", alertFunction)
```

It is a really good idea to use named functions for events since it considerably cleans up your code, especially if it is used in multiple places.

You can also access more information about an even by passing a parameter to the function that we are calling:

```
btn.addEventListener("click", e => {
console.log(e)
}) 
```
When we are passing a function or a parameter to event listener we call it a callback fuction. A callback function is a function being passed into another function as a parameter.

The `e` parameter in the callback function contains an object that references the event itself. It has many usefull properties and methods that check which mouse buttons or which keys were pressed, it also has information about the event's **target** (the DOM node).

## Event Objects

The **target** is a reference to the DOM element that was clicked, so if we did
`e.target.style["color"] = "red"` the button text would become red. You can also change the event from `click` to `keydown` for example. It has a `key` property that checks which key was pressed.

`console.log(e.key)` would log the button.

## Preventing default behaviour

The most common example for this are form submissions. Whenever you submit a form it automatically refreshes the website. The problem occurs when the user puts in wrong information and later the website refreshes and they have to rewrite everything.

`e.preventDefault()` fixes this issue.

## Attaching listeners to groups of nodes

```
<div id="container">
  <button id="one">Click Me</button>
  <button id="two">Click Me</button>
  <button id="three">Click Me</button>
</div>
```

```
// returns a nodelist of buttons
const buttons = document.querySelectorAll("button")

// use .forEach to iterate through each button
buttons.forEach((button) => {
	// for every button we add a listener"
	button.addEventListener("click", () => {
		alert(button.id)
	})
})
```

## Capturing and Bubbling

Bubbling is when an event happens on an element it happens on where you pressed and then happens on all the parents all the way up to the document,

Capturing is when it first goes from the window, document, html and etc. to where you pressed and then goes down (bubbling phase).