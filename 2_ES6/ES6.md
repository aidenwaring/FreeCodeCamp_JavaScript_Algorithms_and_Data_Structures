# ES6

## Compare Scopes of the var and let keywords

When you declare a variable with the `var` keyword, it is declared globally, or locally if declared inside a function.

When you declare a variable with the `let` keyword inside a block, statement, or expression, its scope is limited to that block, statement, or expression.

```js
function checkScope() {
  let i = 'function scope';
  if (true) {
    let i = 'block scope';
    console.log('Block scope i is: ', i);
  }
  console.log('Function scope i is: ', i);
  return i;
}
```

## Mutate an Array Declared with const

Some developers prefer to assign all their variables using `const` by default, unless they know they will need to reassign the value. Only in that case, they use `let`.

However, it is important to understand that objects (including arrays and functions) assigned to a variable using `const` are still mutable. Using the `const` declaration only prevents reassignment of the variable identifier.

```js
const s = [5, 6, 7];
s = [1, 2, 3];
// ^^ This will result in an error
s[2] = 45;
console.log(s);

// [5, 6, 45]
```

You can mutate the array however you cannot reassign the variable's value.

```js
const s = [5, 7, 2];
function editInPlace() {
  s[0] = 2;
  s[1] = 5;
  s[2] = 7;
}
editInPlace();
```

## Prevent Object Mutation

`const` declaration alone doesn't really protect your data from mutation. To ensure your data doesn't change, JavaScript provides a function `Object.freeze` to prevent data mutation.

```js
let obj = {
  name:"FreeCodeCamp",
  review:"Awesome"
};
Object.freeze(obj);
obj.review = "bad";
// ^^ This will return an error
obj.newProp = "Test";
// ^^ This will return an error
console.log(obj); 

// { name: 'FreeCodeCamp', review: 'Awesome' }
```

```js
function freezeObj() {
  const MATH_CONSTANTS = {
    PI: 3.14
  };
  Object.freeze(MATH_CONSTANTS);
  try {
    MATH_CONSTANTS.PI = 99;
  } catch(ex) {
    console.log(ex);
  }
  return MATH_CONSTANTS.PI;
}
const PI = freezeObj();

// [TypeError: "PI" is read-only]
```

## Use Arrow Functions to Write Concise Anonymous Functions

In JavaScript, we often don't need to name our functions, especially when passing a function as an argument to another function. Instead, we create inline functions. We don't need to name these functions because we do not reuse them anywhere else.

```js
// Named function
function sayGreetings() {
  return "Greetings!";
}

const myFunction = function sayHello() {
  return "Hello!";
}

// Removed `sayHi()` as code will not need to reference the function's name. We can assign the function to a variable for use in another function
const myFunction = function() {
  return "Hey there!";
}
```

ES6 provides us with the syntactic sugar to not have to write anonymous functions in the way shown above. Instead we can use arrow function syntax.

```js
const myFunction = () => {
  return "Hi!";
}
```

When there is no function body and only a return value, arrow function syntax allows you to omit the keyword return as well as the brackets surrounding the code. This helps simplify smaller functions into one-line statements.

```js
const myFunction = () => "Hello!";
```

This method will return `"Hello!"` by default.

```js
// JavaScript function
var magic = function() {
  return new Date();
};

// ES6 Arrow function
const magic = () => new Date();
```

## Write Arrow Functions with parameters

Just like a regular function, you can pass arguments into an arrow function.

```js
const doubler = () => 5 * 2;

const doubler = (num) => num * 2;
```

If an arrow function has a single parameter, the parentheses enclosing the parameter may be ommitted.

```js
const doubler = num => num * 2;
```

It is also possible to provide multiple parameters into an arrow function.

```js
const multiplier = (num1, num2) => num1 * num2;
```

```js
// var concat = function(arr1, arr2) {
//   return arr1.concat(arr2);
// };

const concatArrow = (arr1, arr2) => arr1.concat(arr2); 

console.log(concatArrow([1, 2], [3, 4, 5]));
```

## Set Default Parameters for Your Functions

In order to help us create more flexible functions, ES6 introduces default parameters for functions.

```js
const greeting = (name = "Anonymous") => "Hello " + name;

console.log(greeting("John"));
console.log(greeting());

// Hello John
// Hello Anonymous
```

```js
const increment = (number, value = 1) => number + value;
```

## Use the Rest Parameter with Function Parameters

In order to help us create more flexible functions, ES6 introduces the *rest parameter* for function parameters. 

```js 
function myFunc(...args)
```

With the *rest parameter*, you can create functions that take a variable number of arguments. These arguments are stored in an array that can be accessed later from inside the function.

```js
function howMany(...args) {
  return "You have passed " + args.length + " arguments.";
}
console.log(howMany(0, 1, 2));
// You have passed 3 parameters
console.log(howMany("string", null, [1, 2, 3], { }));
// You have passed 4 parameters
```

The rest parameter eliminates the need to check the `args` array and allows us to apply `map()`, `filter()` and `reduce()` on the parameters array.

```js
// const sum = (x, y, z) => {
//   const args = [x, y, z];
//   return args.reduce((a, b) => a + b);
// }

const sum = (...args) => args.reduce((a, b) => a + b);

console.log(sum(1, 2, 3))
```

```js
const sum = (...args) => args.reduce(
  (a, b) => a + b
 );

console.log(sum(1, 2, 3));
// 6
```

## Use the Spread Operator to Evaluate Arrays In-Place

ES6 introduces the *spread operator*, which allows us to expand arrays and other expressions in places where multiple parameters or elements are expected.

```js
const arr = [6, 89, 3, 45];
const maximus = Math.max(...arr);
// 89
```

`...arr` returns an unpacked array. In other words, it *spreads* the array. 

**Copying an array**

```js
const arr1 = ['JAN', 'FEB', 'MAR', 'APR', 'MAY'];
let arr2;

arr2 = [...arr1];

console.log(arr2);
```

**Spread in array literals**

```js
let parts = ['shoulders', 'knees'];
let lyrics = ['head', ...parts, 'and', 'toes'];
//  ["head", "shoulders", "knees", "and", "toes"]
```

## Use Destructuring Assignment to Extract Values from Objects

*Destructuring assignment* is special syntax introduced in ES6, for neatly assigning values taken directly from an `object`.

```js
// ES5
const user = { name: 'John Doe', age: 34 };

const name = user.name;
const age = user.age;

console.log(name);
console.log(age);
// John Doe
// 34
```

```js
// ES6
const user = { name: 'John Doe', age: 34 };

const { name, age } = user;

console.log(name);
console.log(age);
```

Here, the `name` and `age` variables will be created and assigned the values of their respective values from the `user` object. This is much cleaner.

```js
const HIGH_TEMPERATURES = {
  today: 77,
  tomorrow: 80
};

// ES5
// const today = HIGH_TEMPERATURES.today;
// const tomorrow = HIGH_TEMPERATURES.tomorrow;

// ES6
const { today, tomorrow } = HIGH_TEMPERATURES;

console.log(today, tomorrow)
// 77 80
```

## Use Destructuring Assignment to Assign Variables from Objects

Destructuring allows you to assign a new variable name when extracting values. You can do this by putting the new name after a colon when assigning the value.

Using the same object from the last example:

```js
const user = { name: 'John Doe', age: 34 };
```

Here's how you can give new variable names in the assignment:

```js
const user = { name: 'John Doe', age: 34 };

const { name: userName, age: userAge } = user;

console.log(userName, userAge);
// John Doe 34
```

You may read it as "get the value of `user.name` and assign it to a new variable named `userName`" and so on.

```js
const HIGH_TEMPERATURES = {
  yesterday: 75,
  today: 77,
  tomorrow: 80
};

// ES5  
// const highToday = HIGH_TEMPERATURES.today;
// const highTomorrow = HIGH_TEMPERATURES.tomorrow; 

//ES6
const { today: highToday, tomorrow: highTomorrow } = HIGH_TEMPERATURES;
```

## Use Destructuring Assignment to Assign Variables from Nested Objects

You can use the same principles from the previous two lessons to destructure values from nested objects.

```js
const user = {
  johnDoe: { 
    age: 34,
    email: 'johnDoe@freeCodeCamp.com'
  }
};
```

Here's how to extract the values of object properties and assign them to variables with the same name:

```js
const user = {
  johnDoe: { 
    age: 34,
    email: 'johnDoe@freeCodeCamp.com'
  }
};

const { johnDoe: { age, email }} = user;
```

And here's how you can assign an object properties' values to variables with different names:

```js
const { johnDoe: { age: userAge, email: userEmail }} = user;
```

```js
const LOCAL_FORECAST = {
  yesterday: { low: 61, high: 75 },
  today: { low: 64, high: 77 },
  tomorrow: { low: 68, high: 80 }
};

const { today: { low: lowToday, high: highToday } } = LOCAL_FORECAST;
```

## Use Destructuring Assignment to Assign Variables from Arrays

ES6 makes destructuring arrays as easy as destructuring objects.

One key difference between the spread operator and array destructuring is that the spread operator unpacks all contents of an array into a comma-separated list. Consequently, you cannot pick or choose which elements you want to assign to variables.

Destructuring an array lets us do exactly that:

```js
const [a, b] = [1, 2, 3, 4, 5, 6];
console.log(a, b);
// 1 2
```

The variable `a` is assigned the first value of the array, and `b` is assigned the second value of the array.

## Use Destructuring Assignment with the Rest Parameter to Reassign Array Elements

In some situations involving array destructuring, we might want to collect the rest of the elements into a separate array.

```js
const [a, b, ...arr] = [1, 2, 3, 4, 5, 7];
console.log(a, b);
console.log(arr);

// 1 2
// 3 4 5 6 7
```

Variables `a` and `b` take the first and second values from the array. After that, because of the rest parameter's presence, `arr` gets the rest of the values in the form of an array. 

The rest element only works correctly as the last variable in the list.

```js
const source = [1,2,3,4,5,6,7,8,9,10];
function removeFirstTwo(list) {
  const [a, b, ...arr] = list
  return arr;
}
const arr = removeFirstTwo(source);
```

## Use Destructuring Assignment to Pass an Object as a Function's Parameters

In some cases, you can destructure the object in a function argument itself.

```js
// ES5
const profileUpdate = (profileData) => {
  const { name, age, nationality, location } = profileData;

}

// ES6
const profileUpdate = ({ name, age, nationality, location }) => {

}
```

Where is `profileData` in the ES6 example? When `profileData` is passed to the above ES6 function, the values are destructured from the function parameter for use within the function.

```js
const stats = {
  max: 56.78,
  standard_deviation: 4.34,
  median: 34.54,
  mode: 23.87,
  min: -0.75,
  average: 35.85
};

// ES5
const half = (stats) => (stats.max + stats.min) / 2.0; 
// ES6
const half = ({ max, min }) => (max + min) / 2.0;
```

## Create Strings using Template Literals

Template literals allow you to create multi-line strings and to use string interpolation features to create strings.

```js
const person = {
  name: "Zodiac Hasbro",
  age: 56
};

const greeting = `Hello, my name is ${person.name}!
I am ${person.age} years old.`;

console.log(greeting);
```

Firstly, the example uses backticks ``(`),`` not quotes (`'` or `"`), to wrap the string. 

Secondly, notice that the string is multi-line, both in the code and the output. This saves inserting `\n` within strings. 

The `${variable}` syntax used above is a placeholder. Basically, you won't have to use concatenation with the `+` operator anymore. To add variables to strings, you just drop the variable in a template string and wrap it with `${` and `}`. Similarly, you can include other expressions in your string literal, for example `${a + b}`.

## Write Concise Object Literal Declarations Using Object Property Shorthand

```js
// ES5
const getMousePosition = (x, y) => ({
  x: x,
  y: y
});

// ES6
const getMousePosition = (x, y) => ({ x, y });
```

`getMousePosition` is a simple function that returns an object containing two properties. ES6 provides the syntactic sugar to eliminate the redundancy of having to write `x: x`. You can simply write `x` once, and it will be converted to `x: x`.

```js
const createPerson = (name, age, gender) => {
  return {
    name,
    age,
    gender
  };
};
```

## Write Concise Declarative Functions with ES6

When defining functions within objects in ES5, we have to use the keyword `function` as follows:

```js
const person = {
  name: "Taylor",
  sayHello: function() {
    return `Hello! My name is ${this.name}.`;
  }
};
```

With ES6, you can remove the `function` keyword and colon altogether when defining functions in objects. Here's an example of this syntax:

```js
const person = {
  name: "Taylor",
  sayHello() {
    return `Hello! My name is ${this.name}.`;
  }
};
```

```js
const bicycle = {
  gear: 2,
  setGear(newGear) {
    this.gear = newGear;
  }
};
bicycle.setGear(3);
console.log(bicycle.gear);
// 3
```

## Use class Syntax to Define a Constructor Function

ES6 provides a new syntax to create objects, using the `class` keyword.

It should be noted that the `class` syntax is just syntax, and not a full-fledged class-based implementation of an object-oriented paradigm, unlike in languages such as Java, Python, Ruby, etc.

In ES5, we usually define a `constructor` function and use the `new` keyword to instantiate an object.

```js
var SpaceShuttle = function(targetPlanet){
  this.targetPlanet = targetPlanet;
}
var zeus = new SpaceShuttle('Jupiter');
```

The `class` syntax simply replaces the `constructor` function creation:

```js
class SpaceShuttle {
  constructor(targetPlanet) {
    this.targetPlanet = targetPlanet;
  }
}
const zeus = new SpaceShuttle('Jupiter');
```

This `constructor` is invoked when `new` is called to create a new object.

```js
class Vegetable {
  constructor(name) {
    this.name = name
  }
}

const carrot = new Vegetable('carrot');
console.log(carrot.name);
// carrot
```

## Use getters and setters to Control Access to an Object

You can obtain values from an object and set the value of a property within an object.

Getter functions are meant to simply return (get) the value of an object's private variable to the user without the user directly accessing the private variable.

Setter functions are meant to modify (set) the value of an object's private variable based on the value passed into the setter function.

```js
class Book {
  constructor(author) {
    this._author = author;
  }
  // getter
  get writer() {
    return this._author;
  }
  // setter
  set writer(updatedAuthor) {
    this._author = updatedAuthor;
  }
}
const novel = new Book('anonymous');
console.log(novel.writer);
novel.writer = 'newAuthor';
console.log(novel.writer);
// anonymous
// newAuthor
```

Notice the syntax used to invoke the getter and setter. They do not even look like functions. Getters and setters within classes are important because they hide internal implementation details.

```js
class Thermostat {
  constructor(fahrenheit) {
    this.fahrenheit = fahrenheit
  }
  get temperature() {
    return (5 / 9) * (this.fahrenheit - 32);
  }
  set temperature(celsius) {
    this.fahrenheit = (celsius * 9.0) / 5 + 32;
  }
}
const myTemp = new Thermostat(76);
myTemp.temperature();
myTemp.temperature = 30;
/*
  Setters obfuscate the fact that they're functions to callers. 
  When you have an object with a setter, to invoke the setter, assign to the property:
*/
```

## Create a Module Script

ES6 introduced a way to easily share code among JavaScript files.

This involves exporting parts of a file for use in one or more other files, and importing the parts you need, where you need them.

In order to take advantage of this functionality, you need to create a script in your HTML document with a `type` of `module`. Here’s an example:

```html
<script type="module" src="filename.js"></script>
```

A script that uses this `module` type can now use the `import` and `export` features you will learn about in the upcoming challenges.

```html
<html>
  <body>
    <script type="module" src="index.js"></script>
  </body>
</html>
```

## Use export to Share a Code Block

In order to share a function or core block with other files, you first need to `export` it.

```js
export const add = (x, y) => {
  return x + y;
}
```

The above is a common way to export a single function, but you can achieve the same thing like this:

```js
const add = (x, y) => {
  return x + y;
}

export { add };
```

When you export a variable or function, you can import it in another file and use it without having to rewrite the code. 

```js
export { add, subtract };
// Multiple exports
```

```js
const uppercaseString = (string) => {
  return string.toUpperCase();
}

const lowercaseString = (string) => {
  return string.toLowerCase()
}

export { uppercaseString, lowercaseString }
```

## Reuse JavaScript Code Using import

`import` allows you to choose which parts of a file or module to load that have been exported from other files.

```js
import { add } from './math_functions.js';
```

Here, import will find add in math_functions.js, import just that function for you to use, and ignore the rest.

You can also import multiple modules like so:

```js
import { add, subtract } from './math_functions.js';
```

```js
import { uppercaseString, lowercaseString } from './string_functions.js'

uppercaseString("hello");
lowercaseString("WORLD!");
```

## Use * to Import Everything from a File

```js
import * as myMathModule from "./math_functions.js";
```

The above `import` statement will create an object with the variable name `myMathModule`. The object will contain all of the exports from `math_functions.js` in it, so you can access the functions like you would any other object property.

```js
import * as myMathModule from "./math_functions.js";

myMathModule.add(2,3);
myMathModule.subtract(5,3);
```

```js
import * as stringFunctions from './string_functions.js'

stringFunctions.uppercaseString("hello");
stringFunctions.lowercaseString("WORLD!");
```
