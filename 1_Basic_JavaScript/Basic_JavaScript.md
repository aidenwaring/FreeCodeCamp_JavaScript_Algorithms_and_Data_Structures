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

## Escaping Literal Quotes in Strings

```js
const myStr = "I am a \"double quoted\" string inside \"double quotes\".";
```

## Quoting Strings with Single Quotes

String values in JavaScript may be written with single or double quotes, as long as you start and end with the same type of quote. The reason why you might want to use one type of quote over the other is if you want to use both in a string.

```js
let goodString = 'And so I said "What is up?".';
let badString = "And so I said "What is up?".";
let fixedString = "And so I said \"What is up?\".";
```

```js
const myStr = '<a href="http://www.example.com" target="_blank">Link</a>';
```

## Escape Sequences in Strings

Quotes are not the only characters that can be escaped inside a string. There are two reasons to use escaping characters:

- To allow you to use characters you may not otherwise be able to type out, such as a carriage return.
- To allow you to represent multiple quotes in a string without JavaScript misinterpreting what you mean.

| Code | Output          |
| ---- | --------------- |
| `\'` | Single Quote    |
| `\"` | Double Quote    |
| `\\` | Backslash       |
| `\n` | Newline         |
| `\r` | Carriage Return |
| `\t` | Tab             |
| `\b` | Word Boundary   |
| `\f` | Form Feed       |

```js
const myStr = "FirstLine\n\t\\SecondLine\nThirdLine";
```

## Concatenating Strings with Plus Operator

```js
const myStr = "This is the start." + " This is the end.";
```

## Concatenating Strings with the Plus Equals Operator

We can also use the `+=` operator to concatenate a string onto the end of an existing string variable.

```js
let myStr = "This is the first sentence.";
myStr += " This is the second sentence.";
```

## Constructing Strings with Variables

```js
const myName = "Aiden Waring";
const myStr = "My name is " + myName + " and I am well!";
```

## Appending Variables to Strings

We can also append variables to a string using the plus equals (`+=`) operator.

```js
const someAdjective = "spicy!";
let myStr = "Learning to code is ";
myStr += someAdjective;
```

## Find the Length of a String

You can find the length of a `String` value by writing `.length` after the string variable or string literal.

```js
let lastNameLength = 0;
const lastName = "Lovelace";
lastNameLength = lastName.length;
```

## Use Bracket Notation to Find the First Character in a String

Bracket notation is a way to get a character at a specific index within a string.

```js
let firstLetterOfLastName = "";
const lastName = "Lovelace";
firstLetterOfLastName = lastName[0];
```

## Understand String Immutability

In JavaScript, `String values are immutable, which means that they cannot be altered once created.

```js
let myStr = "Bob";
myStr[0] = "J";
// Cannot change the value of myStr to "Job"
// TypeError: Attempted to assign to readonly property.
```

```js
let myStr = "Jello World";
myStr = "Hello World";
```

## Use Bracket Notation to Find the Nth Character in a String

```js
const lastName = "Lovelace";
const thirdLetterOfLastName = lastName[2];
```

## Use Bracket Notation to Find the Last Character in a String

```js
const lastName = "Lovelace";
const lastLetterOfLastName = lastName[lastName.length - 1];
```

## Use Bracket Notation to Find the Nth-to-Last Character in a String

```js
const lastName = "Lovelace";
const secondToLastLetterOfLastName = lastName[lastName.length - 2 ];
```

## Word Blanks (Code Challenge)

```js
const myNoun = "dog";
const myAdjective = "big";
const myVerb = "ran";
const myAdverb = "quickly";

const wordBlanks = "My " + myNoun + " is " + myAdjective + " and when I called him to come to me he" + myVerb + " very " + myAdverb;
```

## Store Multiple Values in one Variable using JavaScript Arrays

With JavaScript `array` variables, we can store several pieces of data in one place.

```js
const myArray = ["Hello", 1];
```

## Nest one Array within Another Array

A nested array is also called a multi-dimensional array.

```js
const myArray = [["Hello", "World"],[1, 2]];
```

## Access Array Data with Indexes

We can access the data inside arrays using indexes.

```js
const myArray = [50, 60, 70];
const myData = myArray[0];
```

## Modify Array Data With Indexes

Unlike strings, the entries of arrays are mutable and can be changed freely, even if the array was declared with `const`.

```js
const myArray = [18, 64, 99];
myArray[0] = 45;
```

## Access Multi-Dimensional Arrays With Indexes

One way to think of a multi-dimensional array, is as an array of arrays. When you use brackets to access your array, the first set of brackets refers to the entries in the outer-most (the first level) array, and each additional pair of brackets refers to the next level of entries inside.

```js
const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];

arr[3];
arr[3][0];
arr[3][0][1];
```

- `arr[3]` is `[[10, 11, 12], 13, 14],` 

- `arr[3][0]` is `[10, 11, 12]`

- `arr[3][0][1]` is `11`.

```js
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14],
];

const myData = myArray[2][1];
```

## Manipulate Arrays With push()

An easy way to append data to the end of an array is via the `push()` function.

`.push` takes one or parameters and "pushes" them to the end of the array.

```js
const myArray = [["John", 23], ["cat", 2]];

myArray.push(["dog", 3]);
```

## Manipulate Arrays With pop()

`.pop()` is used to pop a value off of the end of an array. We can store this popped off value by assigning it to a variable. 

In other words, `.pop()` removes the last element from an array and returns that element.

```js
const myArray = [["John", 23], ["cat", 2]];

const removedFromMyArray = myArray.pop();
```

## Manipulate Arrays With shift()

`.shift()` is used to 'shift off' / remove the first element in the array.

```js
const myArray = [["John", 23], ["dog", 3]];

const removedFromMyArray = myArray.shift();
```

## Manipulate Arrays With unshift()

Not only can you `shift` elements off of the beginning of an array, you can also `unshift` elements to the beginning of an array i.e. add elements in front of the array.

```js
const myArray = [["John", 23], ["dog", 3]];
myArray.shift();

myArray.unshift(["Paul", 35]);
```

## Shopping List (Code Challenge)

```js
const myList = [
  ["Chocolate", 15],
  ["Banana", 1],
  ["Bread", 5],
  ["Apples", 2],
  ["Mangoes", 3]
];
```

## Write Reusable JavaScript with Functions

```js
function myFunction() {
  console.log("Hi World");
}

myFunction()
```

## Passing Values to Functions with Arguments

```js
function testFun(param1, param2) {
  console.log(param1, param2);
}
```

```js
function functionWithArgs(param1, param2) {
  console.log(param1 + param2);
}

functionWithArgs(1, 2);
```

## Return a Value from a Function with Return

```js
function timesFive(param) {
  return param * 5;
}

timesFive(20);
```

## Global Scope and Functions

In JavaScript, scope refers to the visibility of variables.

Variables which are defined outside of a function block have Global scope.

Variables declared without either `let` or `const` have global scope.

```js
const myGlobal = 10;

function fun1() {
  oopsGlobal = 5;
}

function fun2() {
  var output = "";
  if (typeof myGlobal != "undefined") {
    output += "myGlobal: " + myGlobal;
  }
  if (typeof oopsGlobal != "undefined") {
    output += " oopsGlobal: " + oopsGlobal;
  }
  console.log(output);
}
```

## Local Scope and Functions

Variables which are declared within a function, as well as the function parameters, have local scope.

```js
function myLocalScope() {
  let myVar = 1;
  console.log('inside myLocalScope', myVar);
}
myLocalScope();

// myVar is not defined outside of myLocalScope
console.log('outside myLocalScope', myVar);
```

## Global vs. Local Scope in Functions

It is possible to have both local and global variables with the same name. When you do this, the local variable takes precedence over the global variable.

- Local > Global

```js
const outerWear = "T-Shirt";

function myOutfit() {
  const outerWear = "sweater"
  return outerWear;
}

myOutfit();
// returns "sweater"
```

## Understanding Undefined Value returned from a Function

In the case that the function doesn't have a `return` statement, when you call it, the function processes the inner code but the returned value is `undefined`.

```js
let sum = 0;

function addThree() {
  sum = sum + 3;
}

function addFive() {
  sum += 5;
}

addThree();
addFive();
```

## Assignment with a Returned Value

```js
let processed = 0;

function processArg(num) {
  return (num + 3) / 5;
}

processed = processArg(7);
```

## Stand in Line (Code Challenge)

In Computer Science a queue is an abstract Data Structure where items are kept in order. New items can be added at the back of the queue and old items are taken off from the front of the queue.

```js
function nextInLine(arr, item) {
  arr.push(item);
  item = arr.shift();
  return item;
}

const testArr = [1, 2, 3, 4, 5];

console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));
```