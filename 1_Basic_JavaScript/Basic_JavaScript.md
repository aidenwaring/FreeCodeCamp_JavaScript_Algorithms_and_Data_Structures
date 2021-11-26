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

## Understanding Boolean Values

```js
function welcomeToBooleans() {
  return true;
}
```

## Use Conditional Logic with If Statements

```js
function trueOrFalse(wasThatTrue) {
  if (wasThatTrue) {
    return "Yes, that was true"
  }
  return "No, that was false"
}
```

## Comparison with the Equality (==) Operator

```js
function testEqualToTwelve(val) {
  if (val == 12) {
    return "Equal to twelve";
  }
  return "Not equal to twelve";
}
testEqualToTwelve(10);
```

## Comparison with the Strict Equality (===) Operator

Strict equality `===` is the counterpart to the equality operator `==`. However, unlike the equality operator, which attempts to convert both values being compared to a common type, the strict equality operator does not perform a type conversion.

```js
3 ===  3
3 === '3'
```

These conditions would return `true` and `false` respectively.

## Understanding the typeof Operator

In JavaScript, you can determine the type of a variable or a value with the `typeof` operator, as follows:

```js
typeof 3
typeof '3'
```

`typeof 3` returns the string `number`, and `typeof '3'` returns the string `string`.

## Comparison with the Inequality (!=) Operator

```js
// Setup
function testNotEqualTo99(val) {
  if (val != 99) { 
    return "Not Equal to 99";
  }
  return "Equal to 99";
}

testNotEqualTo99(10);
```

## Comparison with the Strict Inequality Operator

```js
!===
```

## Comparison with the Greater Than Operator

```js
function testGreaterThan(val) {
  if (val > 100) {  
    return "Over 100";
  }

  if (val > 10) {  
    return "Over 10";
  }

  return "10 or Under";
}

testGreaterThan(10);
```

## Comparison with the Greater Than Or Equal To Operator

```js
function testGreaterOrEqual(val) {
  if (val >= 20) {  
    return "20 or Over";
  }

  if (val >= 10) {  
    return "10 or Over";
  }

  return "Less than 10";
}

testGreaterOrEqual(10);
```

## Comparison with the Less Than Operator

```js
function testLessThan(val) {
  if (val < 25) {  
    return "Under 25";
  }

  if (val < 55) {  
    return "Under 55";
  }

  return "55 or Over";
}

testLessThan(10);
```

## Comparison with the Less Than Or Equal To Operator

```js
function testLessOrEqual(val) {
  if (val <= 12) {  
    return "Smaller Than or Equal to 12";
  }

  if (val <= 24) {  
    return "Smaller Than or Equal to 24";
  }

  return "More Than 24";
}

testLessOrEqual(10);
```

## Comparisons with the Logical And Operator

```js
function testLogicalAnd(val) {
  if (val <= 50 && val >= 25) {
    return "Yes"
  }
  return "No";
}

testLogicalAnd(10);
```

## Comparisons with the Logical Or Operator

```js
function testLogicalOr(val) {

  if (val < 10 || val > 20) {
    return "Outside";
  }

  return "Inside";
}

testLogicalOr(15);
```

## Introducing Else Statements

```js
function testElse(val) {
  let result = "";

  if (val > 5) {
    result = "Bigger than 5";
  } else {
    result = "5 or Smaller";
  }

  return result;
}

testElse(4);
```

## Introducing Else If Statements

```js
function testElseIf(val) {
  if (val > 10) {
    return "Greater than 10";
  } else if (val < 5) {
    return "Smaller than 5";
  } else {
  return "Between 5 and 10";

  }
}

testElseIf(7);
```

## Logical Order in If Else Statements

The function is executed from top to bottom so you will want to be careful of what statement comes first.

```js
function orderMyLogic(val) {
  if (val < 5) {
    return "Less than 5";
  } else if (val < 10) {
    return "Less than 10";
  } else {
    return "Greater than or equal to 10";
  }
}

orderMyLogic(7);
```

## Chaining if else

```js
function testSize(num) {
  if (num < 5) {
    return "Tiny";
  } else if (num < 10) {
    return "Small";
  } else if (num < 15) {
    return "Medium";
  } else if (num < 20) {
    return "Large";
  } else if (num >= 20) {
    return "Huge";
  }

  return "Change Me";
}

testSize(7);
```

## Selecting from Many Options with Switch Statements

`case` values are tested with strict equality (`===`). The `break` tells JavaScript to stop executing statements. If the `break` is omitted, the next statement will be executed.

```js
function caseInSwitch(val) {
  let answer = "";
  // Only change code below this line
  switch(val) {
    case 1:
      answer = "alpha";
      break;
    case 2:
      answer = "beta";
      break;
    case 3:
      answer = "gamma";
      break;
    case 4:
      answer = "delta";
      break;
  }
  return answer;
}

caseInSwitch(1);
```

## Adding a Default Option in Switch Statements

```js
function switchOfStuff(val) {
  let answer = "";

  switch (val) {
    case "a":
      answer = "apple";
      break;
    case "b":
      answer = "bird";
      break;
    case "c":
      answer = "cat";
      break;
    default:
      answer = "stuff"
  }

  return answer;
}

switchOfStuff(1);
```

## Multiple Identical Options in Switch Statements

```js
function sequentialSizes(val) {
  let answer = "";

  switch(val) {
    case 1:
    case 2:
    case 3:
      answer = "Low";
      break;
    case 4:
    case 5:
    case 6:
      answer = "Mid";
      break;
    case 7:
    case 8:
    case 9:
      answer = "High";
      break;
  }

  return answer;
}

sequentialSizes(1);
```

## Replacing If Else Chains with Switch

```js
function chainToSwitch(val) {
  let answer = "";

  switch(val) {
    case "bob":
      answer = "Marley";
      break;
    case 42:
      answer = "The Answer";
      break;
    case 1:
      answer = "There is no #1";
      break;
    case 99:
      answer = "Missed me by this much!";
      break;
    case 7:
      answer = "Ate Nine";
      break;
  }

  return answer;
}

chainToSwitch(7);
```

## Returning Boolean Values from Functions

```js
function isLess(a, b) {
//   if (a < b) {
//     return true;
//   } else {
//     return false;
//   }
// }

  return a < b;
}

isLess(10, 15);
```

## Return Early Pattern for Functions

When a `return` statement is reached, the execution of the current function stops and control returns to the calling location.


```js
function myFun() {
  console.log("Hello");
  return "World";
  console.log("byebye")
}
myFun();
// byebye is never shown in the console
```

```js
// Setup
function abTest(a, b) {
  if (a < 0 || b < 0) {
    return undefined;
  }

  return Math.round(Math.pow(Math.sqrt(a) + Math.sqrt(b), 2));
}

abTest(2,2);
```

## Counting Cards (Code Challenge)

```js
let count = 0;

function cc(card) {
  switch(card) {
    case 2:
    case 3:
    case 4:
    case 5:
    case 6:
      count++;
      break;
    case 7:
    case 8:
    case 9:
      break;
    case 10:
    case "J":
    case "Q":
    case "K":
    case "A":
      count--;
      break;
  }
  if (count > 0) {
    return count + " Bet";
  } else if (count <= 0) {
    return count + " Hold";
  }
}

cc(2); cc(3); cc(7); cc('K'); cc('A');
```

## Build JavaScript Objects

```js
const cat = {
  "name": "Whiskers",
  "legs": 4,
  "tails": 1,
  "enemies": ["Water", "Dogs"]
};
```

```js
const myDog = {
  "name": "Albie",
  "legs": 4,
  "tails": 1,
  "friends": ["Aiden, Madeleine"]
};
```

## Accessing Object Properties with Dot Notation

There are two ways to access the properties of an object: dot notation (`.`) and bracket notation (`[]`), similar to an array.

```js
const myClothes = {
  "hat": "ballcap",
  "shirt": "jersey",
  "shoes": "cleats"
};

const hatValue = myClothes.hat;
const shirtValue = myClothes.shirt;
```

## Accessing Object Properties with Bracket Notation

If the property of the object you are trying to access has a space in its name, you will need to use bracket notation.

```js
const testObj = {
  "an entree": "hamburger",
  "my side": "veggies",
  "the drink": "water"
};

const entreeValue = testObj["an entree"];
const drinkValue = testObj["the drink"];
```

## Accessing Object Properties with Variables

Here is an example of using a variable to access a property:

```js
const dogs = {
  Fido: "Mutt",
  Hunter: "Doberman",
  Snoopie: "Beagle"
};

const myDog = "Hunter";
const myBreed = dogs[myDog];
console.log(myBreed);
// Doberman
```

```js
const testObj = {
  12: "Namath",
  16: "Montana",
  19: "Unitas"
};

const playerNumber = 16;
const player = testObj[playerNumber];
```

## Updating Object Properties

```js
// Setup
const myDog = {
  "name": "Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"]
};

myDog.name = "Happy Coder";
```

## Add New Properties to a JavaScript Object

```js
const myDog = {
  "name": "Happy Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"]
};

myDog.bark = "woof";
// myDog[bark] = "woof"

console.log(myDog.bark);
// woof
```

## Delete Properties from a JavaScript Object

```js
const myDog = {
  "name": "Happy Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"],
  "bark": "woof"
};

delete myDog.tails;
```

## Using Objects for Lookups

Objects can be thought of as a key/value storage, like a dictionary. If you have tabular data, you can use an object to lookup values rather than a `switch` statement or an `if/else` chain. This is most useful when you know that your input data is limited to a certain range.

```js
function phoneticLookup(val) {
  let result = "";

  // switch(val) {
  //   case "alpha":
  //     result = "Adams";
  //     break;
  //   case "bravo":
  //     result = "Boston";
  //     break;
  //   case "charlie":
  //     result = "Chicago";
  //     break;
  //   case "delta":
  //     result = "Denver";
  //     break;
  //   case "echo":
  //     result = "Easy";
  //     break;
  //   case "foxtrot":
  //     result = "Frank";
  // }

  const lookup = {
    "alpha": "Adams",
    "bravo": "Boston",
    "charlie": "Chicago",
    "delta": "Denver",
    "echo": "Easy",
    "foxtrot": "Frank"
  }
  result = lookup[val];

  return result;
}

phoneticLookup("charlie");
```

## Testing Objects for Properties

Sometimes it is useful to check if the property of a given object exists or not. We can use the `.hasOwnProperty(prop)` method of objects to determine if that object has the given property name. `.hasOwnProperty()` returns `true` or `false` if the property is found or not.

```js
function checkObj(obj, checkProp) {
  if (obj.hasOwnProperty(checkProp)) {
    return obj[checkProp];
  } else {
    return "Not Found"
  }
}
```

## Object Dot Notation vs. Bracket Notation

Dot notation looks for a specific property name whereas bracket notation looks for the value of the property name.

## Manipulating Complex Objects

Sometimes you may want to store data in a flexible Data Structure. 

A JavaScript object is one way to handle flexible data. They allow for arbitrary combinations of strings, numbers, booleans, arrays, functions, and objects.

Example:

```js
const ourMusic = [
  {
    "artist": "Daft Punk",
    "title": "Homework",
    "release_year": 1997,
    "formats": [ 
      "CD", 
      "Cassette", 
      "LP"
    ],
    "gold": true
  }
];
```

This is an array which contains one object inside. It also has a nested array. If you want to add more album records, you can do this by adding records to the top level array.

JavaScript Object Notation or JSON is a related data interchange format used to store data.

```js
const myMusic = [
  {
    "artist": "Billy Joel",
    "title": "Piano Man",
    "release_year": 1973,
    "formats": [
      "CD",
      "8T",
      "LP"
    ],
    "gold": true
  },
  {
    "artist": "Tycho",
    "title": "Dive",
    "release_year": 2011,
    "formats": [
      "CD",
      "LP"
    ],
    "great_album": true
  }
];

```

## Accessing Nested Objects

The sub-properties of objects can be accessed by chaining together the dot or bracket notation.

```js
const myStorage = {
  "car": {
    "inside": {
      "glove box": "maps",
      "passenger seat": "crumbs",
      "drink_tray": "coffee"
     },
    "outside": {
      "trunk": "jack"
    }
  }
};

const gloveBoxContents = myStorage.car.inside["glove box"];
myStorage.car.outside.trunk;
```

## Accessing Nested Arrays

Similar to accessing nested objects, array bracket notation can be chained to access nested arrays.

```js
const myPlants = [
  {
    type: "flowers",
    list: [
      "rose",
      "tulip",
      "dandelion"
    ]
  },
  {
    type: "trees",
    list: [
      "fir",
      "pine",
      "birch"
    ]
  }
];

const secondTree = myPlants[1].list[1];
// Selects "pine"
```

## Record Collection (Code Challenge)

```js
const recordCollection = {
  2548: {
    albumTitle: 'Slippery When Wet',
    artist: 'Bon Jovi',
    tracks: ['Let It Rock', 'You Give Love a Bad Name']
  },
  2468: {
    albumTitle: '1999',
    artist: 'Prince',
    tracks: ['1999', 'Little Red Corvette']
  },
  1245: {
    artist: 'Robert Palmer',
    tracks: []
  },
  5439: {
    albumTitle: 'ABBA Gold'
  }
};

function updateRecords(records, id, prop, value) {
  if (prop !== 'tracks' && value !== "") {
    records[id][prop] = value;
  } else if (prop === 'tracks' && records[id].hasOwnProperty(prop) === false) {
    records[id][prop] = [value]; 
  } else if (prop === 'tracks' && value !== "" && records[id].hasOwnProperty(prop)) {
    records[id][prop].push(value);
  } else if (value === "") {
    delete records[id][prop];
  }
  return records;
}

updateRecords(recordCollection, 5439, 'artist', 'ABBA');
updateRecords(recordCollection, 5439, 'artist', 'ABBA');
updateRecords(recordCollection, 5439, "tracks", "Take a Chance on Me");
updateRecords(recordCollection, 2548, "artist", "");
updateRecords(recordCollection, 1245, "tracks", "Addicted to Love");
updateRecords(recordCollection, 2468, "tracks", "Free");
updateRecords(recordCollection, 2548, "tracks", "");
updateRecords(recordCollection, 1245, "albumTitle", "Riptide");
```

## Iterate with JavaScript While Loops

A `while` loop runs while a specified condition is true and stops once that condition is no longer true.

```js
const myArray = [];
let i = 5;

while (i >= 0) {
  myArray.push(i);
  i--;
}
// [5, 4, 3, 2, 1, 0]
```

## Iterate with JavaScript For Loops

The most common type of JavaScript loop is called a `for` loop because it runs for a specific number of times.

`for (a; b; c)`, where `a` is the initialization statement, `b` is the condition statement, and `c` is the final expression.

The condition statement is evaluated at the beginning of every loop iteration and will continue as long as it evaluates to `true`. When the condition is `false` at the start of the iteration, the loop will stop executing.

The final expression is executed at the end of each loop iteration, prior to the next condition check and is usually used to increment or decrement your loop counter.

```js
const myArray = [];

for (let i = 1; i <= 5; i++) {
  myArray.push(i);
}
// [1, 2, 3, 4, 5]
```

## Iterate Odd Numbers With a For Loop

For loops don't have to iterate one at a time. By changing our `final-expression`, we can count by even numbers.

We'll start at `i = 0` and loop while `i < 10`. We'll increment `i` by 2 each loop with `i += 2`.

```js
const ourArray = [];

for (let i = 0; i < 10; i += 2) {
  ourArray.push(i);
}
// [0, 2, 4, 6, 8]
```

```js
// Setup
const myArray = [];

// Only change code below this line
for (let i = 1; i <= 9; i += 2) {
  myArray.push(i);
}
// [1, 3, 5, 7, 9]
```

## Count Backwards With a For Loop

```js
const ourArray = [];

for (let i = 10; i > 0; i -= 2) {
  ourArray.push(i);
}
// [10, 8, 6, 4, 2]
```

```js
const myArray = [];

for (let i = 9; i >= 1; i -= 2) {
  myArray.push(i);
}
// [9, 7, 5, 3, 1]
```

## Iterate Through an Array with a For Loop

```js
const myArr = [2, 3, 4, 5, 6];

let total = 0;

for (let i = 0; i < myArr.length; i++) {
  total += myArr[i];
}
// 20;
```

## Nesting For Loops

If you have a multi-dimensional array, you can use the same logic as the prior waypoint to loop through both the array and any sub-arrays. Here is an example:

```js
const arr = [
  [1, 2], [3, 4], [5, 6]
];

for (let i = 0; i < arr.length; i++) {
  for (let j = 0; j < arr[i].length; j++) {
    console.log(arr[i][j]);
  }
}
```

This outputs each sub-element in `arr` one at a time. Note that for the inner loop, we are checking the `.length` of `arr[i]`, since `arr[i]` is itself an array.

```js
function multiplyAll(arr) {
  let product = 1;
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr[i].length; j++) {
      product *= arr[i][j];
    }
  }
  return product;
}

multiplyAll([[1, 2], [3, 4], [5, 6, 7]]);
```

## Iterate with JavaScript Do...While Loops

The next type of loop you will learn is called a `do...while` loop. It is called a `do...while` loop because it will first `do` one pass of the code inside the loop no matter what, and then continue to run the loop while the specified condition evaluates to true.

```js
const ourArray = [];
let i = 0;

do {
  ourArray.push(i);
  i++;
} while (i < 5);
// [0, 1, 2, 3, 4]
```

The example above behaves similar to other types of loops, and the resulting array will look like `[0, 1, 2, 3, 4]`. However, what makes the `do...while` different from other loops is how it behaves when the condition fails on the first check. Let's see this in action: Here is a regular `while` loop that will run the code in the loop as long as `i < 5`:

```js
const ourArray = []; 
let i = 5;

while (i < 5) {
  ourArray.push(i);
  i++;
}

// []
```

In this example, we initialize the value of `ourArray` to an empty array and the value of `i` to 5. When we execute the `while` loop, the condition evaluates to `false` because `i` is not less than 5, so we do not execute the code inside the loop. The result is that `ourArray` will end up with no values added to it, and it will still look like `[]` when all of the code in the example above has completed running.

Now, take a look at a `do...while` loop:

```js
const ourArray = []; 
let i = 5;

do {
  ourArray.push(i);
  i++;
} while (i < 5);

// [5]
```

Essentially, a `do...while` loop ensures that the code inside the loop will run at least once.

```js
// Setup
const myArray = [];
let i = 10;

// Only change code below this line
do {
  myArray.push(i);
  i++;
} while (i < 10);
```

## Replace Loops using Recursion

```js
function sum(arr, n) {
  if (n <= 0) {
    return 0;
  } else {
    return sum(arr, n - 1) + arr[n - 1];
  }
}
```

## Profile Lookup (Code Challenge)

```js
// Setup
const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];

function lookUpProfile(name, prop) {
  for (let x = 0; x < contacts.length; x++) {
    if (contacts[x].firstName === name) {
      if (contacts[x].hasOwnProperty(prop)) {
        return contacts[x][prop];
      } else {
        return "No such property";
      }
    }
  }
  return "No such contact";
}

lookUpProfile("Akira", "likes");
```

## Generate Random Fractions with JavaScript

JavaScript has a `Math.random()` function that generates a random decimal number between `0` (inclusive) and `1` (exclusive). Thus `Math.random()` can return a `0` but never return a `1`.

```js
function randomFraction() {
  return Math.random();
}
```

## Generate Random Whole Numbers with JavaScript

It's great that we can generate random decimal numbers, but it's even more useful if we use it to generate random whole numbers.

- Use `Math.random()` to generate a random decimal.
- Multiply that random decimal by `20`.
- Use another function, `Math.floor()` to round the number down to its nearest whole number.

Remember that `Math.random()` can never quite return a `1` and, because we're rounding down, it's impossible to actually get `20`. This technique will give us a whole number between `0` and `19`.

```js
Math.floor(Math.random() * 20);
// Returns a random whole number between 0 and 19
```

```js
function randomWholeNum() {
  return Math.floor(Math.random() * 10);
}
// Returns a random whole number between 0 and 9
```

## Generate Random Whole Numbers within a Range

Instead of generating a random whole number between zero and a given number like we did before, we can generate a random whole number that falls within a range of two specific numbers.

To do this, we'll define a minimum number `min` and a maximum number `max`.

```js
Math.floor(Math.random() * (max - min + 1)) + min
```

```js
function randomRange(myMin, myMax) {
  return Math.floor(Math.random() * (myMax - myMin + 1)) + myMin;
}
```

## Use the parseInt Function

```js
const a = parseInt("007");
// 7
```

The above function converts the string `007` to the integer `7`. If the first character in the string can't be converted into a number, then it returns `NaN`.

```js
function convertToInteger(str) {
  return parseInt(str);
}

convertToInteger("56");
// 56
```

## Use the parseInt Function with a Radix

The `parseInt()` function parses a string and returns an integer. It takes a second argument for the radix, which specifies the base of the number in the string. The radix can be an integer between 2 and 36.

```js
parseInt(string, radix);
```

```js
const a = parseInt("11", 2);
```

The radix variable says that `11` is in the binary system, or base 2. This example converts the string `11` to an integer `3`.

```js
function convertToInteger(str) {
  return parseInt(str, 2);
}

convertToInteger("10011");
```

## Use the Conditional (Ternary) Operator

```js
function checkEqual(a, b) {
  return a == b ? "Equal" : "Not Equal";
}

checkEqual(1, 2);
```

## Use Multiple Conditional (Ternary) Operators

```js
function checkSign(num) {
  return num == 0 ? "zero"
   : num > 0 ? "positive"
   : "negative"; 
}

checkSign(10);
```

## Use Recursion to Create a Countdown

```js
function countdown(i) {
  console.log(i);
  if i < 1 {
    return;
  } else {
    countdown(i - 1);
  }
}
/* 
10
9
8
7
6
5
4
3
2
1
0 
*/
```

```js
function countdown(n) {
  if (n < 1) {
    return [];
  } else {
    const arr = countdown(n - 1);
    arr.unshift(n);
    return arr;
  }
}

/*
[ 1 ]
[ 2, 1 ]
[ 3, 2, 1 ]
[ 4, 3, 2, 1 ]
[ 5, 4, 3, 2, 1 ]
[ 6, 5, 4, 3, 2, 1 ]
[ 7, 6, 5, 4, 3, 2, 1 ]
[ 8, 7, 6, 5, 4, 3, 2, 1 ]
[ 9, 8, 7, 6, 5, 4, 3, 2, 1 ]
[ 10, 9, 8, 7, 6, 5, 4, 3, 2, 1 ]
*/
```

## Use Recursion to Create a Range of Numbers

```js
function rangeOfNumbers(startNum, endNum) {
  if (endNum - startNum === 0) {
    return [startNum];
  } else {
    var numbers = rangeOfNumbers(startNum, endNum - 1);
    numbers.push(endNum);
    return numbers;
  }
}

rangeOfNumbers(1, 10);
// [ 1, 2, 3, 4,  5, 6, 7, 8, 9, 10 ]
```