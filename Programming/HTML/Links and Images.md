## Anchor elements

This is a link to another page/website:

```
<a href="link to a website" target="_blank" rel="noopener noreferrer">This is a link</a>
```

`href="link to a website"` is an attribute to paste in a path to a webpage/website, the text thats wrapped in an anchor element becomes blue and has an underline if it has an href attribute.

`target="_blank"` attribute makes the webpage/website open in another tab instead of redirecting in the same tab.

`rel="noopener noreferrer"` Noopener prevents the website we redirected to from using JavaScript on your website. Noreferrer makes it so that the website we redirected to can't see the website we redirected from.

## Absolute and Relative links

An absolute link `https://www.theodinproject.com/about` leads to another website, has scheme(`https`) and domain (refer to:[[How does the web work]]).

A relative link `./about.html` leads to a webpage in your own files. 

## Images 

```
<img src="path to your image" alt="describes the image">
```

`src` attribute tells the browser where the image is located, for example:

```
<img src="../images/monkey.jpg // Goes back to parent directory, then into the images                                  //folder and then takes the image from there.
```


