# Concatenation in JavaScript
- **In JavaScript, the + sign is not only used for arithmetic addition but also for string concatenation.**
- **When the + operator is used with strings, it concatenates the strings together.**
- **It's important to note that if any operand of the + operator is a string, JavaScript will treat the other operands as strings as well, resulting in string concatenation.**
- **If both operands are numbers, the + operator performs numeric addition.**
#### Example
```
const str = "Hello " + "World";
console.log(str);
```
#### Output:Hello World
- **Type coercion is the automatic conversion of "values" from one data type to another.**
- **It is a fundamental part of JavaScript and can be used to make code more readable and efficient.**
- **There are two types of coercion in JavaScript: implicit and explicit. Implicit coercion happens automatically, while explicit coercion is done manually by the programmer.**
- **It's worth noting that type coercion can lead to unexpected results, so it's essential to be aware of how JavaScript handles these situations.**
#### Example
```
 let sum = "5" + 10;
 console.log(sum);
```
#### Output:510

# Tricky Interview Questions
```
console.log(10 + "20");
//Output:1020
console.log(9 - "5");
//Output:4
console.log("Java" + "Script");
//Output:JavaScript
console.log(" " + " ");
//Output:
let sum = " " + 0;
//Output:
console.log(typeof sum);
//Output:string
console.log("vinod" - "thapa");
//Output:NaN
console.log(true + true);
//Output:2
console.log(true + false);
//Output:1
console.log(false + true);
//Output:1
console.log(false - true);
//Output:-1
```
