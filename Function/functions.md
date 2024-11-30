![image](https://github.com/user-attachments/assets/e9165208-57e6-479e-a3fc-02d141ccff35)
## Function Syantax
![image](https://github.com/user-attachments/assets/44c62e8e-b012-47d7-8d4c-81690cce0fda)
## Purpose of Function
```
//  3 students at a same time wants to find the sum of two numbers
// 1st student
// var a = 5,
//   b = 10;
// var sum1 = a + b;
// console.log(sum1);

// // 2nd student
// var a = 15,
//   b = 15;
// var sum2 = a + b;
// console.log(sum2);

// // 3rd student
// var a = 55,
//   b = 15;
// var sum3 = a + b;
// console.log(sum3);

// lets make a reusable code

// function sum(a, b) {
//   return a + b;
// }

// console.log(sum(5, 5));
// console.log(sum(15, 50));
// console.log(sum(25, 750));
```
### Output:
```
10
65
775
```
# Function Declaration
![image](https://github.com/user-attachments/assets/efecc04c-36cc-43d4-85aa-df093276fe04)
- ** Declare a function using the function keyword, followed by the function name, parameters (if any), and the function body.**
- **This step defines the function and specifies what code should be executed when the function is called.**
#### Example-1
```
 function greet() {
   console.log("Hello Guys, Welcome to Thapa Technical JS Course ");
 }
```
#### Example-2
```
function sum(a,b){
    console.log(a+b)
}
```
#### Example-3
```
// function print(){
//     console.log("suman")
// }
```
# Function Invocation
![image](https://github.com/user-attachments/assets/226f28f1-d651-49de-bd60-36cfac3bceb3)
- **After declaring a function, you can invoke or call it by using its name followed by parentheses.**
- **If the function has parameters, provide values (arguments) for those parameters inside the parentheses.**
- **How to call a function**
- **`greet();`**
#### Example-1
- **1.Write a function to find the sum of two numbers with parameters.**
```
// function sum(a,b){
//     console.log(a+b)
// }
// sum(10,20)
// sum(100,200)
// sum(1000,2000)
```
### Output:
```
30
300
3000
```
#### Example-2
```
// function print(){
//     console.log("suman")
// }
// print()
```
### Output:
```
suman
```
# Function Parameter
![image](https://github.com/user-attachments/assets/4f7a6b02-6135-4681-b963-aa283b47be51)
- **A function parameter is a variable that is listed as a part of a function declaration.It acts as a placeholder for a value that will be provided when the function is called.**
- **Parameters allow you to pass information into a function, making it more versatile and reusable.**
- **Syntax:**
```
function functionName(parameter1, parameter2, ...params) {
    Function body
    Code to be executed when the function is called
 }
```
# Function Argument
![image](https://github.com/user-attachments/assets/8e29fa36-4d70-42e5-a6a6-4a41c8d17ed4)
- **A function argument is a value that you provide when you call a function. Arguments are passed into a function to fill the parameters defined in the function declaration.**
- **syntax:`functionName(argument1, argument2, ...)`;**
### Write a JavaScript program that defines a function called greet to welcome individuals to the JS Course. The function should take a name parameter and output the message "Hello [name], Welcome to Thapa Technical JS Course".Call the function twice, once with the argument "vinod" and once with the argument "ram".
```
// function greet(name) {
//   console.log("Hello " + name + ", Welcome to JS Course");
// }
// greet("ram");
// greet("sita");
```
### Output:
```
ram
sita
```
# 1. Write a function to find the sum of two numbers.
- **"1st declare the function & then call it" In JavaScript, it's a good practice to declare (define) your functions before you call them. This ensures that the function is available for use when you try to call it.**
### Example-1
```
// Function definition
// function sum() {
//   var a = 15,
//     b = 10;
//   console.log(a + b);
// }
// // Calling the function
// sum();
```
### Output:
```
25
```
# Function expressions
- **A function expression is a way to define a function as part of an expression. It can be either named or anonymous. If it's named, it becomes a named function expression.**
### Example-1
```
// var result = function sum(a, b) {
//   console.log(a + b);
// };
// result(10, 15);
```
### Output:
```
25
```
### Example-2
```
function greet(name){
    return `Hello ${name}`
}
let result = greet('suman')
console.log(result)
```
### Output:
```
Hello suman
```
# Anonymous Function
- **An anonymous function is a function without a name. It can be created using either a function expression or a function declaration without a specified name.**
```
 var result = function (a, b) {
   console.log(a + b);
 };
 result(10, 15);
```
### Output:
```
25
```
# Return Keyword
- **Return Keyword: In JavaScript, the return statement is used within a function to specify the value that the function should produce or provide back to the code that called it. The return statement stops the execution of a function and sends a value back to the caller**
- **Syntax: `return expression;`**
### Example 1: Returning a Sum of two number
```
// function sum(a, b) {
//   //   console.log(a + b);
//   return a + b;
//   console.log("hello I am function");
// }
// var result = sum(5, 5);
// // console.log(result);
// console.log("the sum of two number is " + result);
// console.log(sum(5, 5));
// console.log(sum(15, 50));
// console.log(sum(25, 750));
```
### Example 2:
```
// function sum(a,b){
//     return a+b
// }
// let result = sum(10,20)
// console.log(result)
```
### Output:
```
30
```
# IIFE - immediately invoked function expression
- **An IIFE, or Immediately Invoked Function Expression, is a JavaScript function that is defined and executed immediately after its creation. It is a way to create a self-contained block of code that doesn't interfere with the surrounding code and executes immediately**
### Syntax:
```
// (function () {
//   // code to be executed
// })();

// var result = (function (a, b) {
//   console.log(a + b);
//   return a + b;
// })(5, 10);

// console.log("the sum of two number is " + result);
```
# Interview Questions ( IIFE with Parameters)
### Question 1: Calculator Function
- **Write a JavaScript function calculator that takes two numbers and an operator as parameters and returns the result of the operation. The function should support addition, subtraction, multiplication, and division.**
```
const calculator = (num1, num2, operator) => {
  let result;
  switch (operator) {
    case "+":
      return num1 + num2;
    case "-":
      result = num1 - num2;
      return result;
    case "*":
      result = num1 * num2;
      return result;
    case "/":
      if (num2 === 0) {
        return "0 is not allowed";
      } else {
        result = num1 / num2;
        return result;
      }
    default:
      return "no operator found";
  }
};
console.log(calculator(5, 2, "+")); // Output: 7
console.log(calculator(8, 4, "-")); // Output: 4
console.log(calculator(8, 4, "*")); // Output: 32
console.log(calculator(10, 2, "/")); // Output: 5
```
### Output:
```
7
4
32
5
```
### Write a function to reverse a given string without using built-in reverse methods.
```
const isReverse = (str) => {
  let reverse = "";
  for (let char = str.length - 1; char >= 0; char--) {
    reverse = reverse + str[char];
  }
  return reverse;
};
console.log(isReverse("vinod thapa"));
```
### Output:
```
SJ emocleW
```
# Arrow Function
![image](https://github.com/user-attachments/assets/7d2df97b-f50b-411c-84f4-db0f0efe0583)

```
// console.log('we are learning arrow_function')
//////// Example-1
// let print = () => console.log("suman");
// print();
//////// Example-2
// let sum = (a,b) =>console.log(a+b)
//////// Example-3
// let sum = (a, b) => {
//   console.log("ram");
//   return a + b;
// };
// console.log(sum(10, 20));
```
# Higher-order functions and callback function
- **Higher-order functions and callback functions are closely related but are not the same thing. Here's a detailed explanation of both and how they interact:**
## 1. Higher-Order Functions
- **A higher-order function is a function that does one or both of the following:**
- **Takes another function as an argument (a callback function).Returns a function as its output.**
- **Higher-order functions provide flexibility in programming by allowing functions to operate on other functions.**

### Example:
```
function higherOrderFunction(callback) {
  callback(); // Calls the callback function
}
function sayHello() {
  console.log("Hello!");
}
higherOrderFunction(sayHello); // Passes `sayHello` as a callback
```
#### Key Characteristics:
- **Can take functions as arguments.Can return functions as values.**
- **Examples in JavaScript: `map()`, `filter()`, `reduce()`, `setTimeout()`.**
## 2. Callback Functions
- **A callback function is a function that is passed as an argument to another function and is intended to be executed at a later time (either synchronously or asynchronously).**
#### Example:
```
function greet(name) {
  console.log(`Hello, ${name}!`);
}
function processUserInput(callback) {
  const userName = "Alice";
  callback(userName); // Executes the callback function with a value
}
processUserInput(greet); // Passes `greet` as the callback
```

![image](https://github.com/user-attachments/assets/78730f12-6e58-4782-9d12-24ceb2606a22)
### Example-1
![image](https://github.com/user-attachments/assets/52e0cf26-8e03-4041-a3c5-67269e58787e)
### Example-2
```
// console.log("we are learning callback function")

const print = () =>{
    console.log("printing press")
}
const print2 = () =>{
    console.log("printing press 2")
}

const test = (name,callback1,callback2) =>{
   console.log('inside the test function ',name)
   callback1();
   callback2();
}

test('suman',print,print2)
```
### Output
```
// inside the test function  suman
// printing press
// printing press 2
```
#### Key Characteristics:
- **Passed as an argument to another function.**
- **Executed inside the higher-order function, either synchronously or asynchronously.**
- **Common in asynchronous programming: `setTimeout()`, API calls, event listeners.**
- **Are They the Same?No, they are not the same, but they are related:**
- **A higher-order function is the function that accepts another function (a callback) as an argument or returns a function.**
- **A callback function is the function that is passed to a higher-order function to be executed later.**
### Analogy:
- **Think of a higher-order function as a boss delegating tasks and a callback function as the worker performing those tasks.**

# Scope in Function
### Function Global Scope
![image](https://github.com/user-attachments/assets/87f7d6b0-20e3-4cfd-a626-689e913ca16e)
### Function Local Scope
![image](https://github.com/user-attachments/assets/ca1dea07-2367-4017-9c1d-d5902c7ca882)
### Block Scope with let and const
![image](https://github.com/user-attachments/assets/4bd150f6-f8f6-400a-bd4b-0fd17247ca57)
# Difference between Method and Functions 
- **In JavaScript, functions and methods are related but distinct concepts. Here's a breakdown to clarify the difference:**
## Function
- **A function is a standalone block of code designed to perform a specific task.**
- **It is not tied to any object and can be invoked directly.**
- **Functions are declared using the function keyword, arrow functions (=>), or as anonymous functions.**
### Example:
```
function greet(name) {
    return `Hello, ${name}!`;
}
// Invoking a function
console.log(greet("Alice")); // Outputs: Hello, Alice!
```
### Method
- **A method is a function that is a property of an object.**
- **It is invoked on the object it belongs to, and typically operates on that object’s data.**
- **Methods are defined as functions inside an object or class.**
### Example:
```
const person = {
    name: "Alice",
    greet() {
        return `Hello, ${this.name}!`;
    }
};

// Invoking a method
console.log(person.greet()); // Outputs: Hello, Alice!
```
### Differences:

![image](https://github.com/user-attachments/assets/5b85ea8e-b02d-414b-b519-98192c091461)
