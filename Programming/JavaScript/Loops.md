## For Loop


```
const cats = ["Leopard", "Serval", "Jaguar", "Tiger", "Caracal", "Lion"];

for (const cat of cats) {
	console.log(cat) // logs cats one by one
}
```

## Map and Filter

```
const cats = ["Leopard", "Serval", "Jaguar", "Tiger", "Caracal", "Lion"];

const upperCats = cats.map(x => x.toUpperCase())

console.log(upperCats) // [ "LEOPARD", "SERVAL", "JAGUAR", "TIGER", "CARACAL", "LION" ]

// can also be written like this

const toUpper = (string) => {
	return string.toUpperCase()
}

const upperCats = cats.map(toUpper)

```

```
const cats = ["Leopard", "Serval", "Jaguar", "Tiger", "Caracal", "Lion"];

const filtered = cats.filter(x => x.startsWith("L"))

console.log(filtered) // ["Leopard", "Lion"]

// can also be written like this

const lCat = (cat) => {
	return cat.startsWith("L")
}

const filtered = cats.filter(lCat)
```

## For Loop

```
for (let i = 1; i < 10; i++) {
	...
}
```

1. `let i = 1` variable i starts with 1, it is getting reassigned every time the loop repeats so we use let.
2.  As long as `i < 10` the loop continues.
3. `i++` one is added to i after each round

## Exiting and Continuing Loops

```
for (const cat of cats) {
	if (cat == "Lion") {
		break; // stops the loop
	} else {
		continue; // skips this cat and continues the loop
	}
}
``` 