An array is a special variable that can hold more than one value.

```
const cars = ["Saab", "Volvo", "BMW"]

// can also be written like this

const cars = [
	"Saab", 
	"Volvo",
	"BMW"
]

// another way is to add value after creating an array

const cars = []
cars[0] = "Saab"
cars[1] = "Volvo"
cars[2] = "BMW"

// can also use new keyword but it's useless. don't do it
```

## Accessing Array Elements

```
const cars = ["Saab", "Volvo", "BMW"]
let car = cars[0] // Saab
let car = cars.at(-1) // BMW
```

## Changing an Array Element

```
const cars = ["Saab", "Volvo", "BMW"]
cars[0] = "Opel" // changes from Saab to Opel
```

## Converting an Array to a String

```
const fruits = ["Banana", "Orange", "Apple", "Mango"]
document.getElementById("demo").innerHTML = fruits.toString() // result is Banana,Orange,Apple,Mango
```

### Joining an Array into a String

```
const fruits = ["Banana", "Orange", "Apple", "Mango"]
document.getElementById("demo).innerHTML = fruits.join(" * ") // result Banana*Orange*Apple*Mango
```
## Accessing the Full Array

```
const cars = ["Saab", "Volvo", "BMW"]
document.getElementById("demo").innerHTML = cars // result is Saab,Volvo,BMW
```

The typeof shows that arrays are objects.

Arrays are special type of objects, so they can contain all types of variables like objects, other arrays, functions.

## Array Properties and Methods

```
const fruits = ["Banana", "Orange", "Apple", "Mango"]
let length = fruits.length // 4
```

### Accessing the First and Last Array Elements

```
const fruits = ["Banana", "Orange", "Apple", "Mango"]
let firstFruit = fruits[0] // Banana
let lastFruit = fruits[fruits.length -1] // Mango
```

### Looping through Elements

```
const fruits = ["Banana", "Orange", "Apple", "Mango"]

for (let i = 0; i < fruits.length; i++) {
	console.log(fruits[i]) // consoles every fruit one by one
}

// you can use forEach

fruits.forEach(myFunction)

const myFunction = fruit => {
	console.log(fruit)
}
```

### Adding and Removing Elements 

```
const cars = ["Saab", "Volvo", "BMW"]
cars.push("Opel") // adds Opel to the end of an array
cars.pop() // removes the last element from an array which now is Opel
cars.shift() // removes the first element from an array
cars.unshift("Opel") // adds Opel to the beginning of an array
```

To recognize an array:

```
Array.isArray(fruits) // true or false
(fruits instanceof Array) // true or false
```

### Adding Arrays Together

```
const myGirls = ["Cecilie", "Lone"]
const myBoys = ["Emil", "Tobias", "Linus"]

const myChildren = myGirls.concat(myBoys)
```

```
const arr1 = ["Cecilie", "Lone"]
const arr2 = ["Emil", "Tobias", "Linus"]
const arr3 = ["Robin", "Morgan"]

const myChildren = arr1.concat(arr2, arr3)

// you can also just add a value

const myChildren2 = arr1.concat("Piotr")
```

### copyWithin()

Copies values to a specified index starting from another specified index overwriting other values 

```
const fruits = ["Banana", "Orange", "Apple", "Mango", "Mango", "Mango"]

document.getElementById("demo").innerHTML = fruits.copyWithin(2,0)

// result is Banana,Orange,Banana,Orange,Apple,Mango

const fruits = ["Banana", "Orange", "Apple", "Mango", "Kiwi"];  
fruits.copyWithin(2, 0, 2); // specifies which elements
// result is Banana,Orange,Banana,Orange,Kiwi,Papaya
```

### Flattening an Array

```
const myArr = [[1,2], [3,4], [5,6]]
const newArr = myArr.flat() // [1, 2, 3, 4, 5, 6]

const myArr = [1, 2, 3, 4, 5, 6]
const newArr = myArr.flatMap(x => [x, x * 10]) // 1,10,2,20...
```

### Splicing and Slicing Arrays

```
// first parameter specifies index, seconde parameter specifies how many elements should be removes, returns removed elements

const fruits = ["Banana", "Orange", "Apple", "Mango"]
fruits.splice(2, 0, "Lemon", "Kiwi") // Banana, Orange, Lemon, Kiwi, Apple, Mango

const fruits = ["Banana", "Orange", "Apple", "Mango"]
fruits.splice = (2, 2, "Lemon", "Kiwi") // Banana, Orange, Lemon, Kiwi
```

Using splice() to remove elements:

```
const fruits = ["Banana", "Orange", "Apple", "Mango"]
fruits.splice(0, 1) // Orange, Apple, Mango
```

There is a toSpliced() method that does not alter the original array and makes a copy of an array:

```
const fruits = ["Banana", "Orange", "Apple", "Mango"]
const spliced = fruits.toSpliced(0, 2) // Apple, Mango
```

slice() slices a piece of an array and puts it into another.

```
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"]
const citrus = fruits.slice(3) //  Apple, Mango
const citrus = fruits.slice(1, 3) // Orange, Lemon
```