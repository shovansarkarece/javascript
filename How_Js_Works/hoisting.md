# Hoisting
- **Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.**
- **This means that no matter where functions and variables are declared, they are moved to the top of their scope regardless of whether their scope is global or local.**
- **When a function declaration is hoisted, its entire definition (including the body) is moved to the top of its containing scope during the creation phase.**
- **This means that you can call the function before it's actually declared in the code, and it will still work as expected.**
- **Very very Important:Hoisting is not working for let and const only when we use var then only it works**
- **Behind the scene in memory creation phase every variable initialize as undefined and function definition also stored.That's why we are not getting any error.**
```
/////Example-1
console.log(myVar);
var myVar;

greet();

var myVar = 10;
const greet = () => {
  console.log("Welcome, If you are reading this, Don't forget you are awesome");
};
/////Example-2
console.log(a)

var a = 'variable1'

hi()

// Function Definition
// Function Declaration
function hi() {
    console.log('Hello');
}

// Function Definition
// Function Expression
var sayHi = function() {    //anonymous function
    console.log('Hiii');
}

// IIFE


sayHi()
```
# The Temporal Dead Zone
- **The Temporal Dead Zone (TDZ) is a term in JavaScript used to describe the phase in which variables declared using let and const are in scope but cannot yet be accessed.**
- **This concept arises because these variables are hoisted to the top of their enclosing block or function during compilation but remain uninitialized until the actual execution reaches their declaration.
- **Attempting to access these variables before their declaration results in a ReferenceError.**

## Key Characteristics of the Temporal Dead Zone:
- **Hoisting: Variables declared with let and const are hoisted, but unlike var, they are not initialized to undefined. Instead, they remain in the TDZ until their declaration is executed.**

- **Scope: The TDZ starts from the beginning of the block or function in which the variable is declared and ends when the variable is initialized.**

- **Error: Accessing a variable in the TDZ results in a ReferenceError.**

- **Purpose: This behavior enforces the safe usage of let and const by ensuring that you do not accidentally use them before they are declared.**

#### Example
```
console.log(a); // ReferenceError: Cannot access 'a' before initialization
let a = 5;

function example() {
  console.log(b); // ReferenceError: Cannot access 'b' before initialization
  const b = 10;
}
```
### Why Does the TDZ Exist?
- **The TDZ ensures that developers avoid unintentional usage of variables before they are properly initialized. It enforces cleaner and more predictable code.**
- **By contrast, variables declared with var are initialized to undefined during hoisting, leading to potential bugs like this:**
#### Example
```
console.log(x); // undefined
var x = 3;      // Hoisting causes x to be undefined initially
```
- **In summary, the TDZ is an essential aspect of JavaScript's block-scoping rules, reinforcing better coding practices.**
