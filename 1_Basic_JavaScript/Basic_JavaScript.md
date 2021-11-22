# Basic JavaScript

JavaScript is a scripting language you can use to make web pages interactive. It is one of the core technologies of the web, along with HTML and CSS, and is supported by all modern browsers.

## Comment Your JavaScript Code

```js
// Hello
/* Hello */
```

## Declare JavaScript Variables

JavaScript provides eight different data types which are `undefined`, `null`, `boolean`, `string`, `symbol`, `bigint`, `number`, and `object`.

```js
var myName;
```

## Storing Values with the Assignment Operator

```js
var a;
a = 7;
```

## Assigning the Value of One Variable to Another

```js
var a;
a = 7;
var b;
b = a;
```

## Initializing Variables with the Assignment Operator

```js
var a = 9;
```

## Declare String Variables

```js
var myFirstName = "Aiden";
var myLastName = "Waring";
```

"Aiden" is called a string literal. A string literal, or string, is a series of zero or more characters enclosed in single or double quotes.

## Understanding Uninitialized Variables

When JavaScript variables are declared, they have an initial value of `undefined`. If you do a mathematical operation on an undefined variable your result will be `NaN` which means "Not a Number". If you concatenate a string with an `undefined` variable, you will get a literal string of `undefined`.

```js
var a = 5;
var b = 10;
var c = "I am a";

a = a + 1;
b = b + 5;
c = c + " String!";
```

## Understanding Case Sensitivity in Variables

```js
var studlyCapVar;
var properCamelCase;
var titleCaseOver;

studlyCapVar = 10;
properCamelCase = "A String";
titleCaseOver = 9000;
```

## Explore Differences Between the var and let Keywords

One of the biggest problems with declaring variables with the `var` keyword is that you can easily overwrite variable declarations:

A keyword called `let` was introduced in ES6, a major update to JavaScript, to solve this potential issue with the `var` keyword.

Unlike `var`, when you use `let`, a variable with the same name can only be declared once.

This results in an error:

```js
let camper = "James";
let camper = "David";
```

```js
let catName = "Oliver";
let catSound = "Meow!";
```

## Declare a Read-Only Variable with the const Keyword, or const vs. let

`const`, another keyword introduced in ES6, are read only and are a constant value. Once a variable is assigned with `const`, it cannot be reassigned:

```js
const FAV_PET = "Cats";
FAV_PET = "Dogs";
```

The console will display an error due to reassigning the value of `FAV_PET`.

Use `let` where you want the variable to change, and `const` where you want the variable to remain constant.

```js
const FCC = "freeCodeCamp";
let fact = "is cool!";
fact = "is awesome!";
console.log(FCC, fact);
```

## Add Two Numbers with JavaScript

`Number` is a data type in JavaScript which represents numeric data.

```js
const sum = 10 + 10;
```

## Subtract One Number from Another with JavaScript

```js
const difference = 45 - 33;
```

## Multiply Two Numbers with JavaScript

```js
const product = 8 * 10;
```

## Divide One Number by Another with JavaScript

```js
const quotient = 66 / 33;
```

## Increment a Number with JavaScript

```js
i++;
```

```js
i = i + 1;
```

```js
let myVar = 87;
myVar++;
```

## Decrement a Number with JavaScript

```js
i--;
```

```js
i = i - 1;
```

```js
let myVar = 11;
myVar--;
```

## Create Decimal Numbers (Floats) with JavaScript

```js
const ourDecimal = 5.7;
let myDecimal = 5.7;
```

## Multiply Two Decimals with JavaScript

```js
const product = 2.0 * 2.5;
```

## Divide One Decimal by Another with JavaScript

```js
const quotient = 4.4 / 2.0;
```

## Finding a Remainder in JavaScript

The remainder operator `%` gives the remainder of the division of two numbers.

In mathematics, a number can be checked to be even or odd by checking the remainder of the division of the number by `2`.

```js
const remainder = 11 % 3;
```

## Compound Assignment With Augmented Addition

```js
myVar = myVar + 5;
```

```js
myVar += 5;
```

```js
let a = 3;
let b = 17;
let c = 12;

a += 12;
b += 9;
c += 7;
```

## Compound Assignment With Augmented Subtraction

```js
myVar = myVar - 3;
```

```js
myVar -= 3;
```

```js
let a = 11;
let b = 9;
let c = 3;

a -= 6;
b -= 15;
c -= 1;
```

## Compound Assignment With Augmented Multiplication


```js
myVar = myVar * 2;
```

```js
myVar *= 2;
```

```js
let a = 5;
let b = 12;
let c = 4.6;

a *= 5;
b *= 3;
c *= 10;
```

## Compound Assignment With Augmented Division

```js
myVar = myVar / 4;
```

```js
myVar /= 4;
```

```js
let a = 48;
let b = 108;
let c = 33;

a /= 12;
b /= 4;
c /= 11;
```
