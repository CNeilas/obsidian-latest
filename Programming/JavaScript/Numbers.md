Integers without a period or exponent notation are accurate up to 15 digits:

```
let x = 999999999999999; // 999999999999999
let y = 9999999999999999; // 10000000000000000
```

The maximum number of decimals is 17.

Floating point arithmetic is not always 100% accurate.

```
let x = 0.2 + 0.1; // 0.30000000000000004
```

This problem is fixed by multiplying and dividing:

```
let x = (0.2 * 10 + 0.1 * 10) / 10
```

If you add a number and a string together it will result in string concatination:

```
let x = 10;
let y = "20";
let z = x + y; // "1020"
```

JavaScript converts String numbers into numbers if you do any mathematical operations on them, but if its adding them to each other with a `+` then its just a string concatenation.

NaN is not a number. If you do mathematical operations with it the result is NaN, the `typeof NaN` returns `number`.

If you want to have a maximum number you can use `Infinity` or `-Infinity`.

There is a `new Number(500)` object syntax but you should not use it as it complicates code, slows down execution speed and has unexpected behaviour.

A usefull number method is `toFixed(number of decimals)`. 

```
const lotsOfDecimal = 1.766584958675746364;
const twoDecimalPlaces = lotsOfDecimal.toFixed(2); // 1.77
```

You can use increment `++` and decrement `--` operators to increment/decrement by 1: 

```
let a = 10;
let b = 10;
a++ // returns 10 first and then makes it into 11 so when called next time it will be 11
b-- // same but returns 10 first and then makes it into 9
```

If you do `++` or `--` first it will return the incremented or decremented value instantly.

You can only do this with an already existing variable. This will not work:

```
let a = 10;
a++; // works

10++; // doesn't work
```

`-x` makes a number into either negative or positive. If number `-1` `-x` will become `1`. If the number is `1` `-x` will become `-1`.

Unary `+` makes a string into a number and a negative number into a positive number.

```
let a = -1;
+a; // 1

let b = "5";
+b; // 5
```