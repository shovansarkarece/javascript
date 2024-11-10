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
