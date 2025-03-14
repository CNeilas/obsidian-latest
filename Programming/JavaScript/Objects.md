Objects are a non-primitive data type that is used to store complex entities, `jey: value` pairs. `key` is a string and `value` is anything you want. Objects are created by using figure brackets {...}. Objects are like file cabinets, and every file is stored by key, so it's easy to find, remove or add files.

![[object_example.png]]

## Creating an empty object

```
let user = new Object()
let user = {}
```

![[initializing_object.png]]

Usually the `{...}` syntax is used. This declaration is called an object literal.

## Literals and properties

Putting properties into `user` as `key: value` pairs:

```
let user = {
	name: "John",
	age: 30
}
```

![[assigning_obj_properties.png]]

We can add remove and read files anytime using the dot notation.

Getting values:

```
console.log(user.name)
console.log(user.age)
```

Adding values:

```
user.isAdmin = true // since there was no isAdmin it added a new property
```

Deleting values:

```
delete user.name
```

If you want multiword property names they must be in quotes:

```
let user = {
	name: "John",
	age: 30,
	"likes birds": true,
}
```

## Square brackets

You can access multiword named properties with bracket notation:

`user["likes birds"]`

You can also make keys depend of what the user inputs as opposed to naming it yourself:

```
let key = "likes birds"

user[key] = true // this wouldn't work with dot notation
```

This can be used like this:

```
let user = {
	name: "John",
	age: 30,
}

let key = prompt("What do you want to know about the user", "name")
alert(user[key])
```

## Computed properties

We can use square brackets in an object literal to create a computed property:

```
// fruit becomes apple when user types apple in,
let fruit = prompt("Which fruit to buy?", "apple") 

let bag {
	// this makes the fruit connected to prompt above, making fruit into whatever the user chooses to type in
	[fruit]: 5,
}
alert(bag.apple) // 5 if fruit = "apple"
```

Another way of writing this:

```
let fruit = prompt("Which fruit to buy?", "apple")
let bag = {}
bag[fruit] = 5
```

We can make it a little more complex:

```
let fruit = "apple"
let bag = {
	[fruit + "Computers"]: 5, // bag.appleComputers = 5
}
```

## Property value shorthand

In real code existing variables are used as property names:

```
function makeUser(name, age) {
return {
	name: name,
	age: age,
	}
}

let user = makeUser("John", 30)
alert(user.name)
```

Instead of `name: name` we can use a shorthand property:

```
function makeUser(name, age) {
	return {
		name,
		age,
	}
}
```

Normal and shorthand properties can be used in the same object:

```
let user = {
	name,
	age: 30,
}
```

## Property naming limitations

There are none, you can use whatever you want.

## Testing property existance

```
let user = {}

alert(user.noSuchProperty === undefined) // true means there are no such prop
```

We have a special operator `in` for that:

```
"key" in object
###############
let user = {name: "John", age: 30}

alert("age" in user) // true
alert("blabla" in user) // false
```

```
let user = {age: 30}
let key = "age"
alert(key in user)
```

It is better to use `in`, because sometimes `undefined` can be stored as a value as well.

## The "for...in" loop 

```
let user = {
	name: "John",
	age: 30,
	isAdmin: true,
}

for (let key in user) {
	alert(key) // name, age, isAdmin
	alert(user[key]) // John, 30, true
}
```

## Order of properties

Properties with numbers for names are ordered in an ascending order:

```
let code = {
	"49": "Germany",
	"41": "Switzerland",
	"44": "Great Britain",
	"1": "USA",
}

for (let code in codes) {
	alert(code) // 1, 41, 44, 49
}
```

Properties with strings are ordered by the time they were added:

```
let user = {
	name: "John",
	surname: "Smith",
}
user.age = 25

for (let prop in user) {
	alert(prop) // name, surname, age
}
```

You can cheat the ordering by making numbers non-integer. Instead of `"44"` you can write `"+44"`.

## Reassigning object data type variables

```
let animal = {species: "dog"}
let dog = animal

animal = {species: "cat"}

console.log(animal) // {species: "cat"}
console.log(dog) // {species: "dog"}
```