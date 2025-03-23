
![[CSS_changes.png]]

Selectors are what you select different html elements with.

This is a universal selector that selects everything:

```
* {
	color: purple;
}
```

Using a group of selectors for the same change:

```
.read, 
.unread {
	color: white;
	background-color: black;
}
```

 Chaining selectors is when you chain selectors with no space in between resulting in both selectors needed to change the element:

```
.needed#needed {
	color: blue;
}
```

Descendant selectors select an element that has the first selector as a descendant:

```
.father .son {
	color: bluel;
}
```

Images by default are the size of the actual image, if you want to change it without messing with the proportions:

```
img {
	height: auto;
	width: 500px;
}
```

