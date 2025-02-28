This is a function:

```
function favoriteAnimal(animal) {
	return animal + " is my favorite animal!"
} // function declaration

favoriteAnimal("cat") // cat is my favorite animal // calling the function
```

```
function favoriteAnimal(PARAMETER) {...}

favoriteAnimal(ARGUMENT)
```

![[function_args_pars.png]]

Default parameters:

```
function hello(name = "Sneil") {
	return `Hello ${name}`
}
```

Anonymous function:

```
(function () {
	alert("hello")
})
```

Arrow functions:

```
const arrowFunc = () => {
	...
}

const arrowFunc = oneParam => {
	...
}
```

If no parameter is passed in:

```
function showCount(count) {
alert(count ?? "unknown") // checks if there is a count, if not says unknown
}
```

You can use return to exit the function immediately:

```
function number(count) {
	if (count + 10 == 10) {
		return;
	}
}
```