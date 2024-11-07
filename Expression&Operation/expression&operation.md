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

![image](https://github.com/user-attachments/assets/26e1d0b0-eb2e-4a09-8baa-e43128285983)

- **Example**
```
 var myFavNum = 15;
// Assigns the value 15 to the variable myFavNum
 var channelName = 'technical'
```
### 2)Arithmetic operators
- **Arithmetic operators in programming perform basic mathematical operations on variables or values. They include addition, subtraction, multiplication, division, and modulus.**
- **Addition (+): Adds two values or variables.**

![image](https://github.com/user-attachments/assets/0701e428-9927-4343-9aa4-15413288a3ca)

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

### 4) Comparison Operators
- **Comparison operators in JavaScript are used to compare values and return a Boolean result (true or false).**
- **Equal (==): Checks if two values are equal, performing type coercion if necessary.**
```console.log(5 == "5");```

![image](https://github.com/user-attachments/assets/0d161c2a-967f-436e-a7f6-9b37f571d763)

#### Output:true
### Strict Equal (===):
- **Checks if two values are equal without performing type coercion.**
```console.log(5 === "5");```
#### Output:false
### Not Equal (!=   👉 ! =):
- **Checks if two values are not equal, performing type coercion if necessary.**
```console.log(5 != 5);```
#### Output:false
### Greater Than (>):
- **Checks if the value on the left is greater than the value on the right.**
- **Example: 10 > 5 evaluates to true.**
```console.log(5 > 2);```
#### Output:true
### Less Than (<):
- **Checks if the value on the left is less than the value on the right.**
- **Example: 5 < 10 evaluates to true.- **
```console.log(5 < 10);```
#### Output:true
### Greater Than or Equal To (>=):
- **Checks if the value on the left is greater than or equal to the value on the right.**
- **Example: 10 >= 10 evaluates to true.**
```console.log(10 <= 10);```
#### Output:true
### Less Than or Equal To (<=):
- **Checks if the value on the left is less than or equal to the value on the right.**
- **Example: 5 <= 10 evaluates to true.**
```console.log(5 >= 10);```
#### Output:false
### InterView Question
#### What is the difference between == and === operators in JavaScript❓
- **The equality == operator is a comparison operator that compares two values and returns true if they are equal. The strict equality === operator is also a comparison operator, but it compares two values and returns true only if they are equal and of the same type.**
- **Example:**
```
 let num1 = 1;
 let num2 = "1";
 if (num1 === num2) {
   console.log("equal");
 } else {
   console.log("not equal");
 }
```
#### Output:
### 5)Logical operators in JavaScript
- **There are three main logical operators: && (logical AND), || (logical OR), and ! (logical NOT).**

![image](https://github.com/user-attachments/assets/70f62f01-7810-4d19-be65-bfc1c3abb1a9)

### Logical AND (&&): Returns true if both operands are true, otherwise, it returns false.
![image](https://github.com/user-attachments/assets/e007c4f0-1650-4174-9f66-5c5b2999f23e)
- **Example:**
```
 var x = 5;
 var y = 10;
 console.log(x > 0 && y < 0);
```
#### Output:false
### Logical OR (||): Returns true if at least one of the operands is true, otherwise, it returns false.
![image](https://github.com/user-attachments/assets/3a3562d0-682d-4a72-8ba0-cc3418ef1870)
- **Example:**
```
 var a = 15;
 var b = 0;
 console.log(a > 10 || b > 10);
```
#### Output:true
### Logical NOT (!):
- **Returns true if the operand is false, and false if the operand is true.**
- **Example:**
```
 var isOpen = false;
 console.log(!isOpen);
```
#### Output:true
###  InterView Question
#### Combining logical operators allows you to create complex conditions:
- **Write a program that determines if a person is eligible to drive based on their age being greater than or equal to 18 and having a valid driver's license❓**
```
 var age = 19;
 var hadDrivingLicense = false;
// // age > 18
// // age == 18
 console.log(age >= 18 && hadDrivingLicense);
```
#### Output:false
//! How would the result change if hasDriverLicense was set to false❓

### 6)Unary operator
- **Unary operators in JavaScript are operators that work with only one operand. They perform various operations such as negation, incrementing, decrementing, type conversion, and more.**
- **Unary Plus (+): Converts its operand into a number. If the operand is not already a number, it attempts to convert it.**
```
console.log(+3);
console.log(+"5");
```
#### Output:3 
#### Output:5
#### Unary Negation (-): Negates its operand, converting non-numbers into numbers and then negating them.
```
 console.log(-5);
 console.log(-"3");
```
#### Output:-5 
#### Output:-3
#### Prefix Increment (++x) and Prefix Decrement (--x): 
- **In prefix form, the value of the operand is first incremented or decremented, and then the result is returned.**
```
 var x = 5;
 var y = --x;
 console.log(y);
 console.log(x);
```
#### Output:4
#### Output:4
#### Postfix Increment (x++) and Postfix Decrement (x--): In postfix form, the value of the operand is first returned, and then it is incremented or decremented.
```
 var x = 5;
 var y = x++;
 console.log(y);
 console.log(x);
```
#### Output:5
#### Output:6
- **The current value of x (which is 5) is assigned to y. After the assignment, the value of x is then incremented by 1.**
#### 7)Conditional (ternary) operator
![image](https://github.com/user-attachments/assets/c783141e-f32e-4d05-98eb-82f7becfb5af)

![image](https://github.com/user-attachments/assets/87df19ba-9ca0-487d-9120-8611c81d56fe)

- **`syntax: condition ? expressionIfTrue : expressionIfFalse;`**
- **write a program to check if the candidates isEligibleForDrive or not? Age must be equal to or greater then 18.**
```
 var age = 19;
 var result = age >= 18 ? "Yes" : "No";
 console.log(result);
```
#### Output:Yes
##### Let say you have a variable score representing a student's exam score. If the score is greater than or equal to 60, the student passes; otherwise, they fail. Use the conditional (ternary) operator to determine the result and store it in a variable called result. Log the result to the console❓
```
 var score = 99;
 var result = score >= 60 ? "Pass" : "Fail";
 console.log(result);
```
#### Output:Pass
#### Combined Interview Questions
```
console.log(typeof ("5" - 3));
console.log(2 < 12 < 5);
///The main logic is from left to right which is 2<12-->true and true means 1 which is again compared to 1<5, Which is also true. Finally, the output will be 1.
console.log("20" + 10 + 10);
```
#### Output:

![image](https://github.com/user-attachments/assets/71adce63-66e8-4841-a2bc-a1a1f80b6fc2)





