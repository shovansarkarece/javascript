# Scope in JavaScript
- **Scope in JavaScript refers to the context in which variables are declared and accessed.**
- **It defines the visibility and lifetime of variables. When a variable is declared, it is bound to a specific scope, and its accessibility is determined by that scope.**

## In JavaScript We have a Global Scope, Function Scope and Block Scope

# Lexical Scoping:
- **Lexical scope (or static scope) determines variable accessibility based on where functions are defined in the source code, not where they are called. Inner functions can access variables in their outer (parent) scopes.**
- **Key Property: Functions remember the scope in which they were created, even if called outside that scope.**
- **Lexical scoping in JavaScript is like a set of rules that determines where a variable can be used in your code.**
- **It follows the physical structure of your code, so if a variable is declared inside a function or block, it can usually be used only within that function or block.**
- **Lexical scope is the foundation of closures, where a function "closes over" variables in its parent scope, preserving them even after the parent function has executed.**
- **Lexical Scope is the foundation for closures, allowing inner functions to "remember" variables from their parent scopes.**
#### Example:
```
function outerFunction() {
  let outerVar = "I'm from the outer scope";

  function innerFunction() {
    console.log(outerVar); // Accessible due to lexical scope
  }

  return innerFunction;
}

const myInnerFunction = outerFunction();
myInnerFunction(); // "I'm from the outer scope"

```
### Another Example
```
const username = 'Anurag'
let userAge = 25
var a = 50

// function add() {
//   const username = 'Akash'
//   const x = 5
//   const y = 8
//   console.log(x + y)
//   console.log(username)
// }

function subtract() {
  const x = 15
  const y = 18
  const z = 28
  // console.log(x - y)
  // console.log(username)

  function child() {
  // debugger

    const childName = 'Golu'
    // console.log(childName);
    // console.log(x,z);

    if(true){
      let num1 = 78
      var num2 = 987
      console.log(num1);
      console.log(num2);
    }
    console.log(num2);

    function grandChild() {
      const grandChildName = 'Molu'
      // console.log(grandChildName);
    }
    grandChild()
  }


  child()

}
```
# Scope Chaining:
- **Scope chaining is the process by which JavaScript, when looking for the value of a variable, checks the current scope
and then looks in the outer (enclosing) scopes until it finds the variable or reaches the global scope.**
- **Key Concept: Variables in inner scopes have access to variables in their outer scopes, creating a chain of accessible scopes.**

# Global Scope:
- **Variables: Variables declared outside of any function or block have global scope.**
- **Access: Global variables are accessible from any part of the code, including inside functions and blocks.**
# Global Variable vs. Local Variable:
## Global Variable: 
- **A variable declared in the global scope is referred to as a global variable. It has global visibility and can be accessed from anywhere in the code.**
## Local Variable: 
- **A variable declared within a function (function scope) or a block (block scope) is often referred to as a local variable. It has local visibility, limited to the function or block where it's declared.**
```
//  var globalVariable = "I am a global variable";

// function exampleFunction() {
//   console.log(globalVariable); // Accessible within the function
// }

// console.log(globalVariable); // Accessible globally
```
# Function Scope:
- **Variables: Variables declared inside a function have function scope.**
- **Access: Function-scoped variables are only accessible within the function where they are declared.**
```
//  function exampleFunction() {
//     var functionScopedVar = "I am a function-scoped variable";
//     console.log(functionScopedVar); // Accessible within the function
//   }

// console.log(functionScopedVar); // Error: functionScopedVar is not defined
```
# Block Scope:
- **Variables: Variables declared with let and const inside a block (e.g., an if statement or a for loop) have block scope.**
- **Access: Block-scoped variables are only accessible within the block where they are declared.**
- **let and const are block scope**
```
const username = 'Anurag'
let userAge = 25
var a = 50
function add() {
  const username = 'Akash'
  const x = 5
  const y = 8
  console.log(x + y)
  console.log(username)
}
function subtract() {
  const x = 15
  const y = 18
  console.log(x - y)
  console.log(username)
}
add()
subtract()
console.log('Program Ended')
```
#### Graphical representation of above code

![image](https://github.com/user-attachments/assets/461b020f-8c19-4415-b2d9-60e5f1a936da)

### Summary table of global scope, block scope,lexical scope and local scope
![image](https://github.com/user-attachments/assets/c218c22a-696b-4715-ade6-05e65b650ef3)

# Interview Question
```
const globalVariable = "I'm a global variable";

function myFunction() {
  // Function scope
  const functionVariable = "I'm a function variable";

  if (true) {
    // Block scope
    const blockVariable = "I'm a block variable";
    console.log(blockVariable)
    console.log(functionVariable)
    console.log(globalVariable)
  }

  console.log(functionVariable);
}
```
### Output:
```
I'm a block variable
I'm a function variable
I'm a global variable
I'm a function variable
```
