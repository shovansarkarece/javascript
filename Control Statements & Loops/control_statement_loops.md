# Control Statements & Loops
![image](https://github.com/user-attachments/assets/c4c04ee3-6e4c-43db-a955-8b79d4b9da04)
## If Statement

![image](https://github.com/user-attachments/assets/784e195f-2e85-434e-8654-9f1ee9af043a)


## If Else:
- **The if...else statement executes a statement if a specified condition is truthy. If the condition is falsy, another statement in the optional else clause will be executed.**

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

// var areaOfShapes = "square";
// var a = 5;
// var b = 10;
// var result;
// switch (areaOfShapes) {
//   case "square":
//     result = a * a;
//     console.log(result);
//     break;

//   case "rectangle":
//     result = a * b;
//     console.log(result);
//     break;

//   case "circle":
//     var r = 2;
//     result = 3.142 * (r * r);
//     console.log(result);
//     break;

//   default:
//     console.log("No shape matches");
// }

//! Question: Explain the purpose of the code. What is it calculating based on the values of areaOfShapes, a, and b?
//? The code calculates and logs the area of different shapes (rectangle, circle, square) based on the value of the areaOfShapes variable.

//! Question: What will be the output if areaOfShapes is set to "Square" and why?
//? The output will be the square of the variable a (25) since the case matches "Square."

//! Question: Why is there a break statement after each case in the switch statement?
//? The break statement is used to exit the switch statement after the corresponding case is executed, preventing fall-through to subsequent cases.

//! Question: If areaOfShapes is set to "Circle," what will be logged to the console, and why is the variable r defined within the case block?
//? The output will be the area of a circle with radius r (28.26) since the case matches "Circle," and r is defined within the case block.

//! Question: What will happen if areaOfShapes is set to a shape that is not covered by any of the existing case statements?
//? The default case logs "Sorry, the shape is not available" if areaOfShapes is set to a shape not covered by any existing case.

//! Question: How does the switch statement handle the flow of control based on the value of areaOfShapes?
//? The switch statement evaluates the value of areaOfShapes and executes the code block corresponding to the matching case. The break statements ensure that only the relevant code block is executed.

