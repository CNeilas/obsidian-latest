
## Using custom properties

```
.error-modal {
	--color-error-text: red;
	--modal-border: 1px solid black;
	--modal-font-size: calc(2rem + 5vw);

	color: var(--color-error-text);
	border: var(--modal-border);
	font-size: var(--modal-font-size);
}
```

## Fallback values

A fallbackis just a var inside of var in case the first var wasnt available:

```
fallback {
	--color-text: white;

	background-color: var(--undeclared-property, black);
	color: var(--undeclared-again, var(--color-text, yellow));
}
```

## :root

You can declase vars in  `:root` and then use them on any element you want:

```
:root {
	--main-color: red;
}

.cool-paragraph {
	color: var(--main-color);
}

.exciting-paragraph {
	background-color: var(--main-color);
}
```

You can also create themes: 

```
:root.dark {
	--border-btn: 1px solid rgb(220, 220, 220);
	--color-base-bg: rgb(18, 18, 18);
	--color-base-text: rgb(240, 240, 240);
	--color-btn-bg: rgb(36, 36, 36);
}

:root.light {
	code...
}
```

You can use a button to toggle classses on `:root` .

You can also used `prefers-color-scheme`:

```
@media (prefers-color-scheme: dark) {
:root {
	...
}
}
```

This is used when the user uses a dark theme on their system.

https://www.theodinproject.com/lessons/node-path-intermediate-html-and-css-custom-properties to get deeper into this later.