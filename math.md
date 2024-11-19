# JAVASCRIPT MATH
## The JavaScript math object provides several constants and methods to perform mathematical operation. 
### Constants:
- **Math.PI: Represents the mathematical constant Pi (π).**
```
const piValue = Math.PI;
console.log(piValue);
Output:3.141592653589793
```
# Basic Operations:
### abs()
- It returns the absolute value of the given number or in simple, how far the number is from 0. It will be always positive.
```
console.log(Math.abs(-90))///==>90
console.log(Math.abs(5));///===>5
console.log(Math.abs(-115));///===>115
```
### max()
It returns maximum value of the given numbers.
```
console.log(Math.pow(2,3))////==>8
console.log(Math.sqrt(16))////==>8
console.log(Math.max(1,2,3))////==>3

```
### min()
It returns minimum value of the given numbers.
```
console.log(Math.min(1,2,3))////==>1
```
### random()
It returns random number between 0 (inclusive) and 1 (exclusive).
```
console.log((1000+Math.random()*9000))////4789.677353980265
```
### Generate Random number
- **`Math.random()`: Math.random() returns a random number between 0 (inclusive), and 1 (exclusive)**
```
console.log((Math.random() * 100).toFixed(3));
```
### round()
- **It returns closest integer value of the given number.**
- **Math.round(x): Rounds a number to the nearest integer.**
```
// const roundedValue = Math.round(3.7);
// console.log(roundedValue);
console.log(Math.round(4.7))////==>5
```
### pow(x, y):
- **`Math.pow(x, y)`: Returns the value of x to the power of y.**
```
console.log(Math.pow(2, 5));
console.log(2 ** 5);
//////Output:32
             32
```
### sqrt():
- **Math.sqrt(): Math.sqrt(x) returns the square root of x**
```
// let squareRoot = Math.sqrt(25);
// console.log(squareRoot);
```
### log(x)
- **`Math.log(x)`: returns the natural logarithm of x.**
```
// let logResult = Math.log(1);
// let logResult = Math.log(2);
// console.log(logResult);
//////Output: 0
              0.6931471805599453
```
### log2(x)
- **Math.log2(x) returns the base 2 logarithm of x.**
```
// let logResult = Math.log2(8);
// console.log(logResult);
//////Output:3
```
### ceil()
- **It returns a smallest integer value, greater than or equal to the given number.**
- **`Math.ceil(x)`: Returns the value of x rounded up to its nearest integer.**
```
// const ceilValue = Math.ceil(3.7);
// console.log(ceilValue);
console.log(Math.ceil(4.7))////==>5
```
### floor()
- **It returns largest integer value, lower than or equal to the given number.**
- **`Math.floor(x)`: Returns the value of x rounded down to its nearest integer.**
```
console.log(Math.floor(4.7))////==>4
// const floorValue = Math.floor(3.7);
// console.log(floorValue);
```
### trunc(x)
- `Math.trunc(x)`: Returns the integer part of x:
```
// const truncValue = Math.trunc(3.7);
// console.log(truncValue);
```
![image](https://github.com/user-attachments/assets/fe834d47-2625-4b9d-b88a-6b5dfc20ef67)
#### No matter how many chars are there after decimal, `trunc()` will always return only number before the decimal.
#### round rounds to the nearest integer.
#### floor always rounds down.
#### ceil always rounds up.
#### isFinite()
- It determines whether the given value is a finite number.
```
console.log(Number.isFinite(10)); // true
console.log(Number.isFinite(Infinity)); // false
```
### isInteger()
- It determines whether the given value is an integer.
```
console.log(Number.isInteger(10)); // true
console.log(Number.isInteger(10.5)); // false

```
### parseFloat()
- It converts the given string into a floating point number.
```
console.log(Number.parseFloat("10.5")); // 10.5
console.log(Number.parseFloat("10abc")); // 10
```
## parseInt()
- It converts the given string into an integer number.
```
console.log(Number.parseInt("10.5")); // 10
console.log(Number.parseInt("10abc")); // 10
```
## toFixed()
- It returns the string that represents a number with exact digits after a decimal point.
```
let num = 10.5678;
console.log(num.toFixed(2)); // "10.57"

```
## toString()
- It returns the given number in the form of string.This method converts a number into its string representation.
- It can also take a parameter to specify the base (radix) for the conversion (e.g., binary, hexadecimal).
```
let num = 10.12345;
console.log(num.toString());  // "10.12345"
let num = 255;
console.log(num.toString()); // "255"
console.log(num.toString(16)); // "ff" (hexadecimal)
let num = 123;
console.log(num.toString());  // "123"
////Binary (base 2)
let num = 10;
console.log(num.toString(2));  // "1010"
////Octal (base 8)
let num = 10;
console.log(num.toString(8));  // "12"
////Hexadecimal (base 16)
let num = 255;
console.log(num.toString(16));  // "ff"
```
