There are 8 data types.

## Numbers

Just the usual numbers, `NaN` and `Infinity`.

## BigInt

Numbers can only go up to `9007199254740991`. Because of that there is a big int. Big int has an n athe the end of the number to specify that it is a big int.

```
const bigInt = 1234567812345789123751845172551235125n;
```

## String

```
let a = "String";
let b = 'String';
let c = `String`;

//you can put other variables into a string if it's in backticks

let d = `${a} is nice.`
```

## Booleans

Booleans are literally just `true` and `false`

## Null

Null represents nothing: 
```
let age = null;
```

## Undefined

It's when there is no value assigned to a variable.

```
let a;
console.log(a); // undefined
```

## Objects and Symbols

All other types are primitive, objects are non primitive because it can store all types of data.
Symbols are used to make unique indentifiers for objects. It is mentioned here just to know about the 8th data type