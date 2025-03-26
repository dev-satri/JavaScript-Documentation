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
1. Variables and Data Types
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

2. Operators
- Arithmetic Operators:
```
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
```
console.log(10 == "10"); // true (loose equality)
console.log(10 === "10"); // false (strict equality)
console.log(10 > 5); // true
console.log(10 < 5); // false
```
- Logical Operators:
```
console.log(true && false); // false (AND)
console.log(true || false); // true (OR)
console.log(!true); // false (NOT)
```

3. Control Flow
- Conditional Statements:
```
let age = 20;
if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}
```

- Switch Statement:
```
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
```
for (let i = 0; i < 5; i++) {
    console.log(i);
}

let j = 0;
while (j < 5) {
    console.log(j);
    j++;
}
```

# Functions in JavaScript
- Function Declaration:
```
function greet(name) {
    return "Hello, " + name;
}
console.log(greet("Alice"x`));
```

- Function Expression:
```
const add = function(a, b) {
    return a + b;
};
console.log(add(5, 3));
```

- Arrow Function:
```
const multiply = (a, b) => a * b;
console.log(multiply(2, 4));
```

# Objects and Arrays
1. Objects
```
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
```
let fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits[0]);
fruits.push("Mango"); // Add element
fruits.pop(); // Remove last element
```

# JavaScript Asynchronous Programming
- Callback Function:

```
function fetchData(callback) {
    setTimeout(() => {
        callback("Data received");
    }, 2000);
}
fetchData(data => console.log(data));
```
- Promises:
```
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
```
async function fetchData() {
    let response = await fetch("https://api.example.com/data");
    let data = await response.json();
    console.log(data);
}
fetchData();
```
### [:fast_forward: Next: JavaScript DOM Manipulation](https://github.com/dev-satri/JavaScript-Documentation/blob/main/DOM-Manipulation.md)
