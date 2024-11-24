# How JavaScript Works?
![image](https://github.com/user-attachments/assets/bb5d910b-d125-48f0-8b90-db83e526d824)

[Click Here to see JavaScript AST Visualiser](https://www.jointjs.com/demos/abstract-syntax-tree)

## 1: Parsing Phase
### 1. Lexical analysis
- **Lexical analyzer, also known as a lexer, is the first step in the process of compiling a JavaScript program.**
- **It breaks the program down into tokens, which are the basic building blocks of the language.**

## 2. Syntax analysis
- **Takes the stream of tokens from lexical analysis and checks them for correct syntax.**
- **If the syntax is correct, syntax analysis generates a tree-like structure called a parse tree or abstract syntax tree (AST).**
- **The AST represents the hierarchical structure of the program.**

## 2. Compilation (JIT - Just-In-Time Compilation):
- **After the AST is created, the JavaScript engine typically goes through a compilation phase.**
- **In modern engines, like V8 in Chrome, SpiderMonkey in Firefox, or JavaScriptCore in Safari, this compilation often involves a combination of two approaches:**

## Parse and Compile: 
- **The engine parses the code and compiles it into an intermediate form, such as bytecode or machine code.**

## Just-In-Time Compilation (JIT): 
- **Some engines use JIT compilation, where the intermediate code is compiled just before execution.**
- **This allows the engine to optimize the code based on runtime information, improving performance.**

## 3. Execution:
- **Once the code is compiled, the JavaScript engine executes it.**
- **During execution, the engine creates execution contexts, manages the scope chain, handles variable assignments, and calls functions.**
# Global Execution Context
- **It is the default context created by the JavaScript engine before any code is executed.**
- **In a browser environment, the global execution context is associated with the window object.
In Node.js, it is associated with the global object.**
![image](https://github.com/user-attachments/assets/6a22a090-bd4c-4d24-9463-ec42eabb5ffb)


### The execution context consists of two phases: 
- **the creation phase (where variables and functions are hoisted) and the execution phase (where the code is actually run).**
- **The JavaScript engine uses a call stack to keep track of the execution context.**
- **When a function is called, a new frame is added to the stack, and when the function completes, its frame is removed (LIFO - Last In, First Out).**
### Example
![image](https://github.com/user-attachments/assets/1c843b45-e451-4c55-a139-c95a1bed6fec)

## More on inside execution phase
### Call Stack
- **In order to manage the execution contexts, the JavaScript engine uses a call stack.**
- **The call stack is a data structure that keeps track of the currently executing functions in a program.**
- **It operates on the Last In, First Out (LIFO) principle, meaning that the last function added to the stack is the first one to be executed and completed.**

![image](https://github.com/user-attachments/assets/3739b9df-3644-4091-bff5-3ccedb2fcdf1) ![image](https://github.com/user-attachments/assets/569951f2-dd8e-4efb-a9b7-7e4d40d471a1)
![image](https://github.com/user-attachments/assets/524db53f-2b00-49d1-85b9-864ee263ae1f) ![image](https://github.com/user-attachments/assets/ad8118f1-0bf0-488a-869c-e88065e7c566)
![image](https://github.com/user-attachments/assets/ecf3d79b-feb2-4036-9db9-3bfa071718a7)

### Heap Memory:
- **The heap memory is where dynamically allocated memory resides.**
- **This is where objects, closures, and other dynamically allocated data are stored.**
- **While the call stack manages the flow of execution and function contexts, the heap memory holds data that is referenced by these execution contexts.**

### Here's a basic overview of how the call stack works:
- **During the execution of a JavaScript program,The JavaScript engine goes through the creation phase before executing any code.
- **During this phase, it sets up the global execution context. The global execution context is the first one to be created and pushed onto the call stack.**
- **This happens when the JavaScript engine starts executing the code.**

# Key activities during the creation phase include:
- **Creating the global object (window in browsers, global in Node.js).**
- **Setting up the this reference.**
- **Creating the outer environment reference (which is null for the global context).**
- **Creating the variable environment and allocating memory for global variables and functions.**
- **Before executing our code, JavaScript engine scans the code and creates a property for each variable or function in the code.**
- **For variable, It reserves space for them in memory and sets an initial value of undefined, and for functions it also reserves space but sets an initial value as a reference to the actual function in memory.**
- **That's why we can call a function, but if we try to access a variable, we will get undefined.**

# Setting up the scope chain, which initially contains only the global scope.

## Execution Phase:
- **After the creation phase, the actual code execution takes place. This is when the JavaScript engine goes through the code line by line.**
- **Variables are assigned their values, functions are executed, and the program's logic is carried out.**
# Synchronous and Asynchronous in JS
- **Synchronous code executes line by line, blocking further execution until each line is completed, while asynchronous code allows other code to continue executing while it waits for an asynchronous operation to complete.**
#### Synchronous Code
```
// const fun2 = () => {
//   console.log("fun2 starts and ends");
// };

// const fun1 = () => {
//   console.log("fun1 is start");
//   fun2();
//   console.log("fun1 ends");
// };

// fun1();
```
### Output:
```
fun1 is start
fun2 starts and ends
fun1 ends
```
#### Asynchronous Code
```
const fun2 = () => {
  setTimeout(() => {
    console.log("fun2 starts and ends");
  }, 2000);
};

const fun1 = () => {
  console.log("fun1 is start");
  fun2();
  console.log("fun1 ends");
};
fun1();
```
### Output:
```
fun1 is start
fun1 ends
fun2 starts and ends
```
![image](https://github.com/user-attachments/assets/fc2763c8-9089-425f-b646-d12d277f8d3a)
