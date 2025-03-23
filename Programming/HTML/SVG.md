SVG stands for "Scalable Vector Graphics", these are images defined not by pixels but by math instead. This makes the SVG's scale however you want without losing quality as opposed to "raster graphics" which are dependent on their grid size.

Svg is defined using XML which makes them human readable and editable in text editors.

It would look something like this:

```
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
  <rect x=0 y=0 width=100 height=50 />
  <circle class="svg-circle" cx="50" cy="50" r="10"/>
</svg>
```

These are made to be interoperable with HTML, meaning we can put SVG's into HTML code without any changes. These can also be accessed with JS([[DOM Manipulation]])

## Drawbacks

These are only nice to use as Icons or very simple images as they have to be written out with XML.

## Anatomy

`xmlns` - stands for "XML NameSpace". This specifies the dialect of XML. The dialect of SVG is language specific. Without it some browsers will not render your image or render it incorrectly.

`viewBox` - defines the bounds of SVG. This defines positions of diffferent points of the elements, defines aspect ratio and the origin of my SVG as well.

`class, id` - these function just like they do in HTML.

Elements like `<circle>` `<rect>` `<path>` `<text>` are defined by the SVG namespace.The are our basic building blocks. Although you can make very complex SVG's, the are mostly made using these attributes.

## Embedding SVG's

You can either link them using:
`img` or `background-image:url(./my-images.svg)` or just paste them into your HTML.
