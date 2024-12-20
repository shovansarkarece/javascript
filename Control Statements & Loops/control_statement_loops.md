# Control Statements & Loops
![image](https://github.com/user-attachments/assets/c4c04ee3-6e4c-43db-a955-8b79d4b9da04)
## If Statement
![image](https://github.com/user-attachments/assets/33947c91-84bf-4c8c-839a-6a805c92a24c)

## If Else Statement:
- **The if...else statement executes a statement if a specified condition is truthy. If the condition is falsy, another statement in the optional else clause will be executed.**
#### Example-1
![image](https://github.com/user-attachments/assets/784e195f-2e85-434e-8654-9f1ee9af043a)
#### Example-1
![image](https://github.com/user-attachments/assets/b591dab4-c6cc-449d-afb5-6309bab76d06)
### Syntax
```
 if (condition) {
   // Code to be executed if the condition is true
 } else {
   // Code to be executed if the condition is false
 }
```
#### Example-1
- **Let's check the temperature**
```
  var temperature = 25;
  if (temperature > 30) {
   console.log("lets go to beach");
   } else {
   console.log("tv dekhte hai yr");
 }
```
## else - if Statement:
![image](https://github.com/user-attachments/assets/55c68fcd-967e-480a-949c-f3d5625ffb5f)

#### Example-2
- **We can also use an else if clause to check additional conditions:**
```
   var temperature = 15;
     if (temperature >= 30) {
   console.log("lets go to beach");
 } else if (temperature >= 20 && temperature < 30) {
   console.log("tv dekhte hai yr");
 } else {
   console.log("kambhal oodo so jawo");
 }
```

### Interview Question
- **If the person is 18 years or older, a citizen, and registered to vote, display a message saying they are eligible to vote.**
- **If the person is younger than 18, not a citizen, or not registered to vote, display a message saying they are not eligible to vote.**
- **If the person is 18 or older but not a citizen, display a message saying they are not eligible due to citizenship status.**
- **If the person is 18 or older, a citizen, but not registered to vote, display a message saying they are not eligible due to registration status.**
- **Extended voting eligibility checker with additional conditions**
#### Solution
```
 ////Assume the user's age, citizenship status, and registration status as inputs
 let userAge = 19;
 let isCitizen = true; // Assume true for citizen, false for non-citizen
 let isRegistered = true; // Assume false for not registered, true for registered
 ////! Check eligibility using if...else statements with multiple conditions
 if (userAge >= 18) {
   if (isCitizen) {
     if (isRegistered) {
       console.log("You are eligible to vote");
     } else {
       console.log("You are not eligible due to registration status");
     }
   } else {
     console.log("you are not eligible due to citizenship status");
   }
 } else {
   console.log("You are not eligible to vote (Younger)");
 }
```
#### Interview Questions
##### 1)Write a program to check if a number is even or odd.**
```
var num = "7";
if (num % 2 === 0) {
  console.log("Num is even");
} else {
  console.log("Num is odd");
}
```
##### 2)Write a program to check if a number is prime.**
- **Prime numbers are numbers that have only 2 factors: 1 and themselves.**
- **All prime numbers greater than 2 are odd.**
- **However, not all odd numbers are prime.**
```
var num = 13;
var isPrime = true;

for (var i = 2; i < num; i++) {
  if (num % i === 0) {
    isPrime = false;
    break;
  }
}

if (isPrime) {
  console.log("Num is prime");
} else {
  console.log("Num is not prime");
}
```
##### 3)Write a program to check if a number is positive, negative, or zero.**
```
var num = -10;
if (num === 0) {
  console.log("NUm is zero");
} else if (num > 0) {
  console.log("NUm is positive ");
} else {
  console.log("NUm is negative ");
}
```
# Switch Statement
![image](https://github.com/user-attachments/assets/57540f35-a3b5-460f-a3c8-b056b4bf8301)

#### Switch Statement: The switch statement is used to perform different actions based on different conditions.
- **Syntax:**
```
 switch (expression) {
   case value1:
     //   Code to be executed if expression === value1
     break;

   case value2:
     //   Code to be executed if expression === value2
     break;

//   //  More cases can be added as needed

   default:
   //  Code to be executed if none of the cases match
 }
```
#### Explain how the switch statement works and what will be the output when the variable day is set to different values.
```
 var day = "Friday";

 switch (day) {
   case "Monday":
     console.log("today is monday");
     break;

   case "Friday":
     console.log("omg lets have party today");
     break;

   case "Sunday":
     console.log("Lets go to movie");
     break;

   default:
     console.log("no condition match");
 }
```
### Challenge time
> Write a JavaScript switch statement that takes a variable areaOfShapes representing different shapes, and based on its value, calculates and logs the area of the corresponding shape. Consider three shapes: >>'Rectangle,' 'Circle,' and 'Square.' For 'Rectangle,' use variables a and b as the sides; for 'Circle,' use a variable r as the radius; and for 'Square,' use variable a as the side length. If the provided >>>shape is not recognized, log a message saying, 'Sorry the shape is not available.' Test your switch statement with areaOfShapes set to 'Square' and sides a and b set to 5 and 10, respectively. Ensure that >>>>the correct area (25 in this case) is logged to the console.
#### Solution
```
 var areaOfShapes = "square";
 var a = 5;
 var b = 10;
 var result;
 switch (areaOfShapes) {
   case "square":
     result = a * a;
     console.log(result);
     break;

   case "rectangle":
     result = a * b;
     console.log(result);
     break;

   case "circle":
     var r = 2;
     result = 3.142 * (r * r);
     console.log(result);
     break;

   default:
     console.log("No shape matches");
 }
```
- **Question: Explain the purpose of the code. What is it calculating based on the values of areaOfShapes, a, and b?**
- **The code calculates and logs the area of different shapes (rectangle, circle, square) based on the value of the areaOfShapes variable.**

- **Question: What will be the output if areaOfShapes is set to "Square" and why?**
- **The output will be the square of the variable a (25) since the case matches "Square."**

- **Question: Why is there a break statement after each case in the switch statement?**
- **The break statement is used to exit the switch statement after the corresponding case is executed, preventing fall-through to subsequent cases.**

- **Question: If areaOfShapes is set to "Circle," what will be logged to the console, and why is the variable r defined within the case block?**
- **The output will be the area of a circle with radius r (28.26) since the case matches "Circle," and r is defined within the case block.**

- **Question: What will happen if areaOfShapes is set to a shape that is not covered by any of the existing case statements?**
- **The default case logs "Sorry, the shape is not available" if areaOfShapes is set to a shape not covered by any existing case.**

- **Question: How does the switch statement handle the flow of control based on the value of areaOfShapes?**
- **The switch statement evaluates the value of areaOfShapes and executes the code block corresponding to the matching case. The break statements ensure that only the relevant code block is executed.**
# Loops in JavaScript
![image](https://github.com/user-attachments/assets/cab03e68-ed4b-4605-8ae4-091644f3a255)

# While Loop
![image](https://github.com/user-attachments/assets/ab861d8b-f5a9-463b-98c5-9daab05ea25f)
#### Syntax of While Loop
![image](https://github.com/user-attachments/assets/fc455d14-c0b1-4af0-bf0b-532740a44e4b)
#### While Loop: 
 - **A while loop in JavaScript is a control structure that repeatedly executes a block of code as long as a specified condition remains true. The loop continues iterating while the condition is true, and it terminates when the condition becomes false.**
```
 while (condition) {
//   // Code to be executed as long as the condition is true
// }
```
##### Simple while loop to count from 1 to 10 🧑‍💻
```
 var num = 1;
 while (num <= 10) {
   console.log(num);
   num++;
 }
```
##### let's create a table of 5
 - **5*1 = 5**
 - **5*2 = 10**
 - **5*2 = 10**
```
 var num = 1;
 while (num <= 10) {
   console.log("5 * " + num + " = " + 5 * num);
      console.log(`5 * ${num} = ${5 * num}`);
   num++;
 }
```
# Do-While Loop
![image](https://github.com/user-attachments/assets/1c42d384-8048-470a-9ba1-d4bb2926f506)

### Syntax of Do-While Loop
![image](https://github.com/user-attachments/assets/adf25d3e-dadb-4044-a196-ceb98bd742e9)

#### Do-While Loop: 
- **A do-while loop in JavaScript is similar to a while loop, but it guarantees that the loop body will be executed at least once before checking the loop condition.**
- **The loop continues to execute while the specified condition is true, and it terminates when the condition becomes false.**
#### Syntax: 
```
do {
   // Code to be executed at least once
 } while (condition);
```
#### Simple do...while loop to count from 1 to 10 🧑‍💻**
```
 var num = 1;
 while (num <= 10) {
   console.log(num);
   num++;
 }
```
#### Another Example
```
// var num = 1;
// do{
//     console.log(num);
//     num++;
// }while (num <= 10)
```
## Common Use Cases:
- **When we want to guarantee the execution of the loop body at least once.**
- **When the number of iterations is not known beforehand, and you want to validate the condition after the first iteration.**

- **Example: Validating User Input with a Do...While Loop(user need to write a valid number) 🧑‍💻**
```
// let userInput;
// let positiveNumber;
// do {
//   userInput = prompt("enter any positive number");
//   positiveNumber = parseFloat(userInput);
// } while (isNaN(positiveNumber) || positiveNumber < 0);
// console.log("You entered a valid positive number:", positiveNumber);
```
# For Loop

![image](https://github.com/user-attachments/assets/fe4ccbe3-be19-4db5-9c9e-a33e3b284788)

![image](https://github.com/user-attachments/assets/07ea0e59-89eb-4f1c-b4ab-af0f7d5bab12)

- **For Loop: A for loop in JavaScript is a control flow statement that allows you to repeatedly execute a block of code a specified number of times.**
- **It's particularly useful when you know the exact number of iterations needed.**

#### Example: 
```
for (initialization; condition; iteration) {
//   // Code to be executed in each iteration
// }
```
- **Initialization: Executed before the loop starts. Often used to initialize a counter variable.**
- ** Condition: Evaluated before each iteration. If false, the loop terminates.**
- ** Iteration: Executed after each iteration. Typically used to update the loop control variable.**
#### Simple for loop to count from 1 to 10
```
 var num = 1;
 do {
   console.log(num);
   num++;
 } while (num <= 10);
 for (var num = 1; num <= 10; num++) {
   console.log(num);
 }
```
#### Key Point:
- **The initialization, condition, and iteration expressions are optional. You can omit any or all of them, but you must include the semicolons.**
- **The code for (;;) {} represents an infinite loop in JavaScript. This construct is commonly used when you want a loop to run indefinitely or until a break statement is encountered within the loop.**
- **It's equivalent to while (true) {}.**
- **use case: Game Development:**
- **In game development, an infinite loop can be used to continuously update and render game frames until a specific condition (e.g., game over) is met.**
#### Example: 
```
// for (;;) {
//   // Update game logic and render frames
// }
```
#### Common Use Cases:
- **When you know the exact number of iterations needed.**
- **Iterating over elements in an array.**
- **Performing a task a specific number of times.**
#### Practice :
- **Calculate the sum of numbers from 1 to 10 using a for loop 🧑‍💻**
```
 var sum = 0;
 debugger;
 for (var num = 1; num <= 10; num++) {
   var sum = sum + num;
 }
 console.log(sum);
```
- **Generating a Times Table:🧑‍💻**
- **Example 3: Generating a times table of 5 with a for loop.**
```
 var num = 1;
 while (num <= 10) {
   console.log("5 * " + num + " = " + 5 * num);
//   //   console.log(`5 * ${num} = ${5 * num}`);
   num++;
 }
/////Using for loop
 for (var num = 1; num <= 10; num++) {
   console.log("5 * " + num + " = " + 5 * num);
 }
```
#### ➡️ JavaScript program to print table for given number (8,9,12,15) using for Loop?
- **1)Program To check if a year is a leap year🧑‍💻**
- **If a year is divisible by 4 and not divisible by 100, or**
- **If a year is divisible by 400,**
- **then it is a leap year. Otherwise, it is not a leap year.**
```
 var year = 2020;
 if ((year % 4 === 0 && year % 100 !== 0) || year % 400 === 0) {
   console.log(year, "it's a leap year");
 } else {
   console.log(year, "it's not a leap year");
 }
```
- **2)Drawing Patterns with Asterisks: 🧑‍💻**

- **i\j  1    2    3    4    5**
- **----------------------------**
- **1    *    -    -    -    -**
- **2    *    *    -    -    -**
- **3    *    *    *    -    -**
- **4    *    *    *    *    -**
- **5    *    *    *    *    \***
#### Solution:
- **Step-1**

![image](https://github.com/user-attachments/assets/2a2580c5-ac27-4074-bfad-58755ef2786d)

- **Step-2**

![image](https://github.com/user-attachments/assets/61ccc075-4cd1-4fc0-bb9e-0bd917e1d60d)

- **Step-3**

![image](https://github.com/user-attachments/assets/9e6b0319-aed8-4b70-8299-51300511581b)

- **Step-4**

![image](https://github.com/user-attachments/assets/ce307082-a01e-4581-bdf6-32da2c50182c)

- **Step-5**

![image](https://github.com/user-attachments/assets/c8ba2e89-efbb-408c-a4de-6f9b907a9f0b)

### Pattern COde Below:
```
 for (var i = 1; i <= 5; i++) {
   var pattern = "";
   for (var j = 1; j <= i; j++) {
     pattern = pattern + " *";
   }
   console.log(pattern);
 }
```
# Advanced Loops
## for_in loop
- **Use for...in when you need to iterate over the keys or indices (e.g., object properties or array indices).**
- **Purpose:The for...in loop is used to iterate over the keys or properties of an object (or the indices of an array).**
- **Works With: Objects, arrays, and other enumerable properties.**
- **What It Accesses: It iterates over the keys (or property names) in an object or the indices (or array indices) in an array.**
![image](https://github.com/user-attachments/assets/8eb2c06d-8cc3-45e0-bd7f-f2a1ddd10fdb)
### Example
```
const phone = {
    brand:'iphone',
    modal:'iphone - 16',
    price:75000,
    camera:'20 MP',
    ram :'2 GB',
    rom : '16 GB'
}
// brand,modal,price,camera,ram,rom
// USing for loop without using Template literal 
for(let key in phone){
    console.log(key, phone[key])
}
// USing for_in loop without using Template literal 
for(let key in phone){
    console.log(`${key}: ${phone[key]}`)
}
```
### Output:
```
brand: iphone
modal: iphone - 16
price: 75000
camera: 20 MP
ram: 2 GB
rom: 16 GB
```
### Another Example
```
const person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 50,
    eyeColor: 'blue',
    city: 'Bangalore',
}
// for(const key in person) {
//     console.log(key, ': ' ,person[key]);
// }
const personKeys = Object.keys(person)
const personValues = Object.values(person)
const personEntries = Object.entries(person)
// for (const key of personKeys) {
//     console.log(person[key]);
// }
```

## for_of  loop
- **It simplifies iterating over iterable objects such as arrays, strings, and sets.**
- **Purpose: The for...of loop is used to iterate over the values of an iterable (like an array, string, or other iterable objects).**
- **Works With: Arrays, strings, maps, sets, and other iterable objects.**
- **What It Accesses: It iterates directly over the values of the iterable, not the keys or indices.**
- **Use for...of when you need to iterate over the values in an iterable (e.g., array elements, string characters).**
![image](https://github.com/user-attachments/assets/b233c5fd-eb4f-450a-8fdc-70c809dc67e1)
### Example
```
// for of
let arr = [1,2,3,4,5]

for(let value of arr){
    console.log(value)
    console.log(`${value}`) // USing for_of loop without using Template literal 
}
```
### Output:
```
1
2
3
4
5
```
### Another Example
```
const fruits = ['banana', 'apple', 'peach', 'mango', 'grapes']
// console.log('*');
// for(const fruit of fruits) {
//     console.log(fruit);
// }
// const user = 'Anurag Singh'
// for(const letter of user) {
//     console.log(letter);
// }
```

## for_Each  loop
![image](https://github.com/user-attachments/assets/03b12dab-a455-48d2-8bed-a99590d72600)
### Example-1
```
let arr = [10,20,30];
arr.forEach((value,index,arr)=>console.log(value,index,arr))
```
### Output:
```
10 0 [ 10, 20, 30 ]
20 1 [ 10, 20, 30 ]
30 2 [ 10, 20, 30 ]
```

### Example-2
```
let arr = [10,20,30];
arr.forEach((value,index,arr)=>console.log(
    `The given array is ${arr}
     The arrays's index is ${index} 
     The arrays's value is ${value}
     `))
```
### Output:
```
The given array is 10,20,30
     The arrays's index is 0
     The arrays's value is 10

The given array is 10,20,30
     The arrays's index is 1
     The arrays's value is 20

The given array is 10,20,30
     The arrays's index is 2
     The arrays's value is 30
```
### Example-3
```
const fruits = ['banana', 'apple', 'peach', 'mango', 'grapes']

// for(const fruit of fruits) {
//     console.log(fruit);
// }

// fruits.forEach(function(fruit) {
//     console.log(fruit);
// })

// fruits.forEach((fruit) => {
//     console.log(fruit);
// })

// function abc(el) {
//     console.log(el);
// }

// fruits.forEach(abc)
```
