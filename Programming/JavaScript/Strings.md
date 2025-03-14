If you want to use multiline breaks instead of a \n you can do this:

```
let string = `this is a
multiline string`;
```

If you want to put quotes you can escape the quotes:

```
let string = "This is an escaped \"quote\"";
```

or just:

```
let string = "This is an escaped 'quote'";
let string2 = 'This is an escaped "quote"';
```

Turning a string into a number:

```
let numberString = "123";
let number = Number(numberString);
// or
let number = +numberString;
```

## String Methods

String methods return new strings, strings are immutable.

### Length

```
let text = "aaaa";
text.length; // 4
```

### Extracting String Characters

```
let text = "Hello World";
let char = text.charAt(0); // return the character at the specified index
```

```
let text = "Hello World";
let char = text.charCodeAt(0); // returns utf-16 code of the character at the specified index
```

```
let text = "Hello World";
let char = text.at(-2); // charAt cannot return characters at negative indexes 
```

```
let text = "Hello World";
let char = text[0]; // returns H, read only, returns undefined if no character found, charAt returns an empty string
```

### Extracting String Parts

```
let text = "Apple, Banana, Kiwi";
let part = text.slice(7, 13); // slices out text starting at 7th index ending with 13(not inclusive)
```

If there is no seconde parameter it will slice out the rest of the string from the starting position.
If the parameter is negative the position is counted from the end of the string.

`substring(7, 13)` is the same as `slice()` but if the parameters are lower than 0 it just counts them as 0.

`substr(7,6)` is also same as slice but the second parameter specifies the length of the extracted part.

### Converting to UpperCase and LowerCase

```
let text = "Hello World"; // Hello World
let upperText = text.toUpperCase(); // HELLO WORLD
let toLowerCase = text.toLowerCase(); // hello world
```

```
text = "Hello" + " " + "world!";
// same as
text = "Hello".concat(" ", "World!");
```

### Trimming

```
let string = "  text  ";
// let string2 = string.trim(); // would remove all whitespace
// let string2 = string.trimStart(); // would remove whitespace at the start
// let string 2 = string.trimEnd(); // would remove whitespace at the end
```

### Padding

```
let text = "5";
// let padded = text.padStart(4, x); // xxx5 // pads untile length of 4 is reached
// let padded = text.padEnd(4,x); // 5xxx
```

### Repeating

```
let text = "Hello World";
let result = text.repeat(4); // repeats Hello World 4 times
```

### Replacing

```
let text = "Hello World"
let replaceText = text.replace("World", "Sneil"); // replaces the word World with Sneil
let replaceAllText = text.replaceAll("cats", "dogs"); // replaces all cats with dogs
```

### Splitting Strings into Arrays

```
let text = "How are you doing today?";
const myArray = text.split(""); // ["H","o","w"," ","a","r","e"," ","y","o","u"," ","d","o","i","n","g"," ","t","o","d","a","y","?"]
const myArray = text.split("|"); // ["How are you doing today?"]
const myArray = text.split(","); // ["How are you doing today?"]
const myArray = text.split(" "); // ["How, are, you, doing, today?"]
```
Experiment with this shit later myself.

## IndexOf

```
console.log("bagel.indexOf("l")) // 4
console.log("bagel.indexOf("z")) // -1
```

`indexOf` will return only the first occurence of the character. If the character is not found withing the string it will return `-1`.

## ToLowerCase and ToUpperCase

```
let string = "chaR"
console.log(string.toUpperCase()) // CHAR
console.log(string.toLowerCase()) // char
```
