# Expression & Operation

![image](https://github.com/user-attachments/assets/ffe09cfd-8101-4857-8437-a89ab23689e3)
### Graphical representation operator, operand, and expression
![image](https://github.com/user-attachments/assets/980501fc-8e7d-44bf-9209-093465ee8af2)

### Types of Operators in JS
- **Assignment operators**
- **Arithmetic operators**
  - **In the arithmetic operator we have increment and decrement operators.**
- **Comparison operators**
- **Logical operators**
- **String operators**
- **Conditional (ternary) operator**

![image](https://github.com/user-attachments/assets/1ae216ff-9f37-4003-871e-901329f9d78c)

### 1)Assignment operators
- **Assignment operators in programming are symbols used to assign values to variables. They take the value on the right side of the operator and assign it to the variable on the left side.**
- **Example**
```
 var myFavNum = 15;
// Assigns the value 15 to the variable myFavNum
 var channelName = 'technical'
```
### 2)Arithmetic operators
- **Arithmetic operators in programming perform basic mathematical operations on variables or values. They include addition, subtraction, multiplication, division, and modulus.**
- **Addition (+): Adds two values or variables.**
- **Example:**
```
var x = 5;
var y = 10;
var sum = x + y;
console.log(sum);
```
#### Output:15
- **Subtraction (-): Subtracts the right operand from the left operand.**
- **Example:**
```
// var a = 10;
// var b = 7;
// var difference = a - b;
// console.log(difference);
```
#### Output:3
- **Multiplication (*): Multiplies two values or variables.**
- **Example:**
```
// Example:
// var p = 4;
// var q = 6;
// var product = p * q;
// console.log(product);
```
#### Output:24
- **Division (/): Divides the left operand by the right operand.**
- **Example:**
```
// var m = 15;
// var n = 3;
// var quotient = m / n;
// console.log(quotient);
```
#### Output:5
- **Modulus (%): Returns the remainder when the left operand is divided by the right operand.**
- **Example:**
```
// var c = 17;
// var d = 5;
// var remainder = c % d;
// console.log(remainder);
```
#### Output:2
#### Interview Question
- **What will be the Output 🤔💭**
- **Example:**
```
var result = "hello" / 2 ❓
var result = "hello" / 2;
console.log(result);
```
#### Output:NaN
- **Example:**
```
 var result = 0.1 + 0.2 ❓ 🤔💭
 var result = 0.1 + 0.2;
 console.log(result.toFixed(2));
```
#### When working with floating-point numbers in JavaScript, consider using methods like toFixed() when precise decimal representation is necessary.
- **Example:**
```
const result = 55 * "hello" ❓
// var result = 55 * "hello";
//console.log(result);
```
#### Output: NaN
### String Operators
- **There are a few ways to concatenate strings in JavaScript. The most common way is to use the + operator. For example, to concatenate the strings "Hello" and "World", you would use the following code:**
- **Example:**
```
 var str1 = "Hello";
 var str2 = "World ";
 var str3 = str1 + Str2;
 console.log(str3);
```
#### Output: HelloWorld
####  InterView Question
- **Example:**
``` console.log("5" + 3);```
#### Output: 53
