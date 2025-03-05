You run javascript by putting `<script src="path"> </script>` to the bottom of html.

Variables are storages for data.

![[variables.png]]
Variables can be declared with a `let` keyword.

```
let name = "John";
let surname = "Doe";

console.log(name)
console.log(surname)
```

You can also reassign variables:

```
let age = 11;
console.log(age); // outputs 11 to the console

age = 54;
console.log(age; // outputs 54 to the console
```

If you want to not be able to reassign a variable you can use the `const` keyword. If you try to reassignt it an error will be thrown.

```
const pi = 3.14;
pi = 10; // throws an error

console.log(pi); // outputs 3 because you cannot reassign it
```