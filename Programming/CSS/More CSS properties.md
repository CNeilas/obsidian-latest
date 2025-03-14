## Background

The `background` property is a shorthand property for 8 different background related properties.

### Background attachement 

https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment 

Some weird stuff about background image's position.

### Background clip

https://developer.mozilla.org/en-US/docs/Web/CSS/background-clip

Seems very specific so not getting into it rn as well.

### Background color

```
body {
	background-color: red; // sets background color
}
```

### Background image

```
body {
	background-image: url(""); // sets background image
}
```

### Background origin

```
background-origin: border-box;
background-origin: padding-box;
background-origin: content-box;
```

Sets the background's origin: from the border start, inside the border, inside the padding.

### Background position

Sets the position of the background image in the box.

```
background-position: top;
background-position: left;
background-position: center;
background-position: 25% 75%;
background-position: bottom 50px right 100px;
background-position: right 35% bottom 45%;
```


### Background-repeat

Sets how background images are repeated:

```
background-repeat: repeat-x;
background-repeat: repeat;
background-repeat: space;
background-repeat: round;
background-repeat: no-repeat;
background-repeat: space repeat;
```

### Background size

```
background-size: contain; // works well with no-repeat
background-size: cover;
background-size: 30%;
background-size: 200px 100px;
```

## Border

This is a very simple shorthand.

```
border: 1px solid black;
border-bottom: 1px solid black;
border-radius: 10%; // makes border more round
```

## Box shadow

Just use a box shadow generator, it adds a shadow effect around an element.

## Overflow

Using `overflow` you can define what happens if there is too much content for the parent, for example you can make it scrollable.