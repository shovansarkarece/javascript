# JAVASCRIPT MATH
## The JavaScript math object provides several constants and methods to perform mathematical operation. 
### abs()
- It returns the absolute value of the given number.
```
console.log(Math.abs(-90))///==>90
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
### round()
It returns closest integer value of the given number.
```
console.log(Math.round(4.7))////==>5
```
### ceil()
- It returns a smallest integer value, greater than or equal to the given number.
```
console.log(Math.ceil(4.7))////==>5
```
### floor()
- It returns largest integer value, lower than or equal to the given number.
```
console.log(Math.floor(4.7))////==>4
```
### isFinite()
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
parseInt()
- It converts the given string into an integer number.
```
console.log(Number.parseInt("10.5")); // 10
console.log(Number.parseInt("10abc")); // 10
```
toFixed()
- It returns the string that represents a number with exact digits after a decimal point.
```
let num = 10.5678;
console.log(num.toFixed(2)); // "10.57"

```
toString()
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
