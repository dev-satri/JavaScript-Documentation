# JavaScript
JavaScript (JS) is a high-level, interpreted programming language primarily used for creating interactive and dynamic web applications. It is a core technology of the web, alongside HTML and CSS, enabling client-side scripting to enhance user experiences.

## Key Features of JavaScript
`Dynamically Typed`: Variables do not require explicit type definitions.<br>
`Prototype-Based`: Uses prototype inheritance rather than classical OOP inheritance.<br>
`Event-Driven & Asynchronous`: Supports event-based programming and async operations with promises and async/await.<br>
`Multi-Paradigm`: Supports functional, object-oriented, and imperative programming.<br>
`Runs in Browsers`: Executed by web browsers, making it the primary language for front-end development.<br>
`Node.js for Backend`: JavaScript can also be used on the server side with Node.js.<br>

# JavaScript Basics
## Variables and Data Types
- Declaring Variables:
```
var name = "John"; // Function-scoped
let age = 25; // Block-scoped
const PI = 3.14; // Constant value
```
- Data Types:
`Primitive Types:` String, Number, Boolean, Undefined, Null, Symbol, BigInt<br>
`Reference Types:` Object, Array, Function
`Example`
```
let num = 10; // Number
let str = "Hello"; // String
let isActive = true; // Boolean
let user = { name: "John", age: 30 }; // Object
let arr = [1, 2, 3, 4]; // Array
```

## Operators
- Arithmetic Operators:
```js
let a = 10;
let b = 5;
console.log(a + b); // Addition
console.log(a - b); // Subtraction
console.log(a * b); // Multiplication
console.log(a / b); // Division
console.log(a % b); // Modulus
console.log(a ** b); // Exponentiation
```

- Comparison Operators:
```js
console.log(10 == "10"); // true (loose equality)
console.log(10 === "10"); // false (strict equality)
console.log(10 > 5); // true
console.log(10 < 5); // false
```
- Logical Operators:
```js
console.log(true && false); // false (AND)
console.log(true || false); // true (OR)
console.log(!true); // false (NOT)
```

## Control Flow
- Conditional Statements:
```js
let age = 20;
if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}
```

- Switch Statement:
```js
let day = "Monday";
switch (day) {
    case "Monday":
        console.log("Start of the week");
        break;
    case "Friday":
        console.log("Weekend is near");
        break;
    default:
        console.log("Regular day");
}
```

- Loops:
```js
for (let i = 0; i < 5; i++) {
    console.log(i);
}

let j = 0;
while (j < 5) {
    console.log(j);
    j++;
}
```
# Type Conversion
## Implicit Type Conversion (Type Coercion)

### Number to String
```js
console.log(5 + "5");  // "55" (Number converted to String)
console.log(true + " is a boolean"); // "true is a boolean"
```
### String to Number
```js
console.log("5" - 2);  // 3 (String converted to Number)
console.log("10" * "2"); // 20 (Both strings converted to numbers)
console.log("10" / "2"); // 5
console.log("5" - "hello"); // NaN (Not a Number)
```
### Boolean to Number
```js
console.log(true + 2);  // 3 (true = 1, false = 0)
console.log(false + 10); // 10
```
### Null and Undefined
```js
console.log(null + 5);  // 5 (null is treated as 0)
console.log(undefined + 10); // NaN (undefined leads to NaN)
```
## Explicit Type Conversion (Type Casting)
You can manually convert types using JavaScript's built-in functions.
### Convert to Number
Use `Number()`, `parseInt()`, `parseFloat()`
```js
console.log(Number("42"));  // 42
console.log(Number("42.5"));  // 42.5
console.log(Number("42px"));  // NaN
console.log(parseInt("42px"));  // 42
console.log(parseFloat("42.5px"));  // 42.5
console.log(Number(true));  // 1
console.log(Number(false)); // 0
```
### Convert to String
Use `String()` or `.toString()`
```js
console.log(String(123));  // "123"
console.log((123).toString());  // "123"
console.log(String(true));  // "true"
```
### Convert to Boolean
Use `Boolean()`
```js
console.log(Boolean(0));  // false
console.log(Boolean(1));  // true
console.log(Boolean("")); // false (empty string is false)
console.log(Boolean("Hello")); // true (non-empty string is true)
console.log(Boolean(null)); // false
console.log(Boolean(undefined)); // false
console.log(Boolean(NaN)); // false
console.log(Boolean([])); // true (empty array is true)
console.log(Boolean({})); // true (empty object is true)
```
## Special Cases
```js
console.log(Number(null));  // 0
console.log(Number(undefined)); // NaN
console.log(5 + true);  // 6 (true is 1)
console.log(5 + false); // 5 (false is 0)
console.log("5" + null); // "5null" (null is converted to string)
console.log("5" - null); // 5 (null is converted to 0)
console.log("5" - undefined); // NaN (undefined leads to NaN)
```
## Checking Types
Use `typeof` to check data types.
```js
console.log(typeof "Hello"); // "string"
console.log(typeof 42); // "number"
console.log(typeof true); // "boolean"
console.log(typeof []); // "object"
console.log(typeof {}); // "object"
console.log(typeof null); // "object" (special case)
console.log(typeof undefined); // "undefined"
console.log(typeof NaN); // "number"
```

# Functions in JavaScript
- Function Declaration:
```js
function greet(name) {
    return "Hello, " + name;
}
console.log(greet("Alice"x`));
```

- Function Expression:
```js
const add = function(a, b) {
    return a + b;
};
console.log(add(5, 3));
```

- Arrow Function:
```js
const multiply = (a, b) => a * b;
console.log(multiply(2, 4));
```

# Objects and Arrays
1. Objects
```js
let person = {
    name: "John",
    age: 30,
    greet: function() {
        console.log("Hello, " + this.name);
    }
};
console.log(person.name);
person.greet();
```
2. Arrays
```js
let fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits[0]);
fruits.push("Mango"); // Add element
fruits.pop(); // Remove last element
```

# JavaScript Asynchronous Programming
- Callback Function:
```js
function fetchData(callback) {
    setTimeout(() => {
        callback("Data received");
    }, 2000);
}
fetchData(data => console.log(data));
```
- Promises:
```js
let promise = new Promise((resolve, reject) => {
    let success = true;
    if (success) {
        resolve("Success");
    } else {
        reject("Error");
    }
});
promise.then(res => console.log(res)).catch(err => console.log(err));
```
- Async/Await:
```js
async function fetchData() {
    let response = await fetch("https://api.example.com/data");
    let data = await response.json();
    console.log(data);
}
fetchData();
```
### [:fast_forward: Next: JavaScript DOM Manipulation](https://github.com/dev-satri/JavaScript-Documentation/blob/main/DOM-Manipulation.md)
