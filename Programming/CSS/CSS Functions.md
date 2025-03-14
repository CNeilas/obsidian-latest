When the css property value is a word followed by a pair of parentheses containing information between them - `background-color: rgb(0, 0, 0);` - you are using CSS functions.

## Calc()

The most powerful use cases include:
	1. Mixing units
	2. The ability to nest `calc( calc() - calc() )`

Example:

```
:root {
	--header: 3rem;
	--footer: 40px;
	--main: calc(100vh - calc(var(--header) + var(--footer)));
}
```

## Min()

```
#iconHolder {
width: min(150px, 100%);
height: min(150px, 100%);
}
```

If there is 150px available to the image, it will take up 150px, if not it will take 100%.
150px is the maximum allowed value. You can also do basic math in min.

## Max()

`width: max(100px, 4em, 50%`;

This works same as min but in reverse. This will select whichever value is bigger.

## Clamp()

```
h1 {
	font-size: clamp(320px, 80vw, 60rem);
}
```

1. Smallest value is 320px.
2. Ideal value is 80vw.
3. Largest is 60rem.

Clamp uses these values to set the smallest ideal and biggest value.

https://www.theodinproject.com/lessons/node-path-intermediate-html-and-css-css-functions assignment  later to see how clamp works