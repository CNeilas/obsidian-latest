The first HTML file is usually named index.html because websites look for the index page by default.

Html files end with .html so that computer would know it's an HTML file.

## The Doctype

```
<!DOCTYPE html> // Tells browser that we are using HTML5
```

## HTML element

```
<html lang="en">
</html>
```

This is the root of the file, all content goes into html element.
The `lang` attribute is an accessibility feature.

## Head element

```
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>My Title</title>
</head>
```

Head element is the first one to go into the html element because it contains meta information.

`<meta charset="UTF-8">` Specifies the characters from different languages that are gonna be specified in the webpage.

`<meta name="viewport" content="width=device-width, initial-scale= 1.0">` is for responsiveness with different devices.

`<title>My Title</title>` Gives webpage a human readable name which is displayed on the browser's tab.

## Body element

```
<body></body>
```

`<body></body>` element is where we put all our content into, it always goes below `<head></head>` element.