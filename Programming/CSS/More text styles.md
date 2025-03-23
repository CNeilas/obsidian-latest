## Fonts

If you change the font and it is not installed on the user's computer the default font will be used which is often ugly. To go around this, use:

```
body {
  font-family: system-ui, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
}
```

This goes through the user's fonts and tries to pick out the one that the user has on his system.

## Web fonts

If you want to use a font that isn't on the user's device you have to link to an external API. Adding callbacks is a must because there is not guarantee that the link wont change or that API won't go down at some point.

## Online font libraries

You can use a font library with either `@import` or `<link>`.

## Self hosted fonts

You can self host fonts, not gonna get into that rn.

## Text styles

### Font style

```
h1 {
	font-style: italic; // makes the font italic
}
```

### letter-spacing

```
.wide {
	letter-spacing: 0.5rem; // the distance between letters
}
```

### line-height

```
p.line-height {
	line-height: 1.5; // puts space between lines of text.
}
```

### text-transform

Changes the case of the given text.

### text-shadow

Just adds shadow on elements.

### ellipsis

No idea what this does, have to try later:

```
.overflowing {
	white-space: nowrap;
	overflow: hidden;
	text-overflow: ellipsis;
}
``` 

Oh it makes the Hell...(it does ... at the end of content that does not fit, adding this because I realized I couldn't understand this reading it after a while) if text overflows, funny.