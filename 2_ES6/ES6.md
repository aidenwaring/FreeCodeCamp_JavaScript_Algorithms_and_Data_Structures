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
```

