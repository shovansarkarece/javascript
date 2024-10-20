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
//? If the person is younger than 18, not a citizen, or not registered to vote, display a message saying they are not eligible to vote.
//? If the person is 18 or older but not a citizen, display a message saying they are not eligible due to citizenship status.
//? If the person is 18 or older, a citizen, but not registered to vote, display a message saying they are not eligible due to registration status.
//? Extended voting eligibility checker with additional conditions

// Assume the user's age, citizenship status, and registration status as inputs
// let userAge = 19;
// let isCitizen = true; // Assume true for citizen, false for non-citizen
// let isRegistered = true; // Assume false for not registered, true for registered
// //! Check eligibility using if...else statements with multiple conditions

// if (userAge >= 18) {
//   if (isCitizen) {
//     if (isRegistered) {
//       console.log("You are eligible to vote");
//     } else {
//       console.log("You are not eligible due to registration status");
//     }
//   } else {
//     console.log("you are not eligible due to citizenship status");
//   }
// } else {
//   console.log("You are not eligible to vote (Younger)");
// }

//* ===============================
//* Interview Questions
//* ===============================
//! 1: Write a program to check if a number is even or odd.
var num = "7";
if (num % 2 === 0) {
  console.log("Num is even");
} else {
  console.log("Num is odd");
}

//! 2: Write a program to check if a number is prime.
//todo Prime numbers are numbers that have only 2 factors: 1 and themselves.
//? All prime numbers greater than 2 are odd.
//? However, not all odd numbers are prime.

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

//! 3: Write a program to check if a number is positive, negative, or zero.
var num = -10;
if (num === 0) {
  console.log("NUm is zero");
} else if (num > 0) {
  console.log("NUm is positive ");
} else {
  console.log("NUm is negative ");
}
