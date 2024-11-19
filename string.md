# String
- **The JavaScript string is an object that represents a sequence of characters**
- **Strings in JavaScript are a fundamental data type that represents a sequence of characters.**
- **Strings created with single or double quotes works the same.**
## String Properties:
- **length: Property that returns the length of the string (number of characters).**
```
// const str = "Hello,    World!";
// console.log(str.length);
// including space and all
```
### Output:
```
16 ===>Means in this string there are 16 characters available.
```
## Escape Character: 
- **In JavaScript, the backslash \ is used as an escape character. It allows you to include special characters in a string.**
```
// Code	   Result	    Description
// \'	    '	        Single quote
// \"	    "	        Double quote
// \\	    \	        Backslash
// \n     new line  new line
// let text = "My name is ' Thapa Technical ' & \\ I am a \"Full Stack \" Developer. ";
//  let text = 'My name is " Thapa Technical " & I am a Full Stack Developer. ';
 let text = 'My name is " Thapa Technical " \n & I am a Full Stack Developer. ';
// console.log(text);
```
### Output:
```
My name is ' Thapa Technical ' & \ I am a "Full Stack " Developer.
My name is " Thapa Technical " & I am a Full Stack Developer.
My name is " Thapa Technical "
 & I am a Full Stack Developer.
```

# String Method()
## Extracting String Characters
## There are 3 methods for extracting string characters:

- **The charAt(position) Method**
- **The charCodeAt(position) Method**
- **The at(position) Method**
# charAt()
![image](https://github.com/user-attachments/assets/99ff37a7-c677-4ac1-8a4f-dae2fcd8549c)
- **It provides the char value present at the specified index. It provides an empty string when there is no specified character available in that specified index.**
```
////*******String Method *************/
////charAt()==>It provides the char value present at the specified index.
let text="Hello world"
let res=text.charAt("3")
console.log(res)
/////Output:l
```
- **concat()**
  >It provides a combination of two or more strings.
```
let text="Hello world"
let res=text.concat(" JavaScript Developer ")
console.log(res)
/////Output:Hello world JavaScript Developer 
```
- **indexOf()**
![image](https://github.com/user-attachments/assets/2b8630f0-700d-4b19-8ee7-237d9b0c752a)
- **The indexOf() method is case sensitive.**
- **The indexOf() method returns the index (position) of the first occurrence of a string in a string, or it returns -1 if the string is not found.**
- **syntax:`indexOf(searchString, position)`**
```
let text = "Vinod Thapa";
// console.log(text.indexOf("thapa"));
console.log(text.indexOf("Thapa"));
```
### Output:
```
-1
6
```
## from()
- **The from() method is not directly associated with strings in JavaScript. However, it is a static method of the Array class, used to create arrays from iterable or array-like objects (e.g., strings).**
- **If you're working with strings, you might use Array.from() to convert a string into an array of its characters.**
### Example:
```
let text = "Vinod Thapa";
let strArr = Array.from(text);
console.log(strArr);
```
### Output:
```
[
  'V', 'i', 'n', 'o',
  'd', ' ', 'T', 'h',
  'a', 'p', 'a'
]
```
### Another Example:
```
const str = "hello";
const arr = Array.from(str);
console.log(arr); 

```
### Output:
```
['h', 'e', 'l', 'l', 'o']
```
# Using Array.from() with a Mapping Function:
### Example
```
const str = "hello";
const upperCaseArr = Array.from(str, char => char.toUpperCase());
console.log(upperCaseArr); 
```
### Output:
```
 ['H', 'E', 'L', 'L', 'O']
```
### Another Example
```
let text = "Vinod Thapa";
let strArr = Array.from(text);
let strMap = strArr.map((curElem, index) => `${curElem} - ${index}`);
console.log(strMap);
```
### Output:
```
[
  'V - 0',  'i - 1',
  'n - 2',  'o - 3',
  'd - 4',  '  - 5',
  'T - 6',  'h - 7',
  'a - 8',  'p - 9',
  'a - 10'
]
```
# lastIndexOf()**
- **It provides the position of a char value present in the given string by searching a character from the last position.**
- **The lastIndexOf() method returns the index of the last occurrence of a specified text in a string:**
- **It always works index from left to right means backwards**
- **syntax:`lastIndexOf(searchString, position)`**
### Example:
```
let text = "Hello JavaScript, welcome to our world best JavaScript course";
// let index = text.indexOf("JavaScript");
// let index = text.lastIndexOf("JavaScript");
let index = text.lastIndexOf("JavaScript", 40);
console.log(index);
```
### Output:
```
44 ==>It is searching That string from last not from fast
6 ==>As per syntax we are searching that string from the 40th index but as we know lastIndexOf() works from left to right, that's why it will return 6th index.Because it works from left to right and 2nd
JavaScript string is available at the 44th index.
```
### Another Example
```
let text="Hello world"
let res=text.lastIndexOf("l")
let res1=text.lastIndexOf("o")
console.log(res)
console.log(res1)
```
### Output:
```
 9
 7
```
# search(): 
- **The search() method searches a string for a string (or a regular expression) and returns the position of the match.**
- **Returns the index number where the first match is found. Returns -1 if no match is found.**
- **but as it is working as a case-sensitive that's why we use i flag to ignore case sensitivity**
- **👉 Important Tips**
- **The search() method cannot take a second start position argument.**
- **The indexOf() method cannot take powerful search values (regular expressions).**
- **They accept the same arguments (parameters), and return the same value.**
```
let text = "Hello JavaScript, welcome to our world best JavaScript course";
let result = text.search(/Javascript/i);
console.log(result);
```
### Output:
```
6
```
# match(): 
- **Returns an array of the matched values or null if no match is found.**
- **here the js converts the normal text into regular expression text.match(/JavaScript/); without the g flag**
```
let text = "Hello JavaScript, welcome to our world best JavaScript course";
let result = text.match("Javascript");
 let result = text.match("JavaScript");
 let result = text.match(/Javascript/gi);
console.log(result);
```
### Output:
```
null

[
  'JavaScript',
  index: 6,
  input: 'Hello JavaScript, welcome to our world best JavaScript course',
  groups: undefined
]

[ 'JavaScript', 'JavaScript' ]
```
# matchAll() : 
- **Returns an iterator of all matches, providing detailed information about each match. Returns an empty iterator if no match is found.**
- **here the js converts the normal text into regular expression text.match(/JavaScript/g); also adds the g flag at the end.**
- **Returns an iterator: The method returns an iterator, not an array.We can convert it to an array using the spread operator ([...]) or Array.from().**
- **Requires g flag: The regular expression should have the g flag for global matches.**
```
// let text = "Hello JavaScript, welcome to our world best JavaScript course";
// // let matchResult = text.matchAll("javascript");
// let matchResult = text.matchAll("JavaScript");
// //todo  here the js converts the normal text into regular expression text.match(/JavaScript/g); also adds the g flag at the end
// console.log(matchResult);
// console.log(...matchResult);
// for (let item of matchResult) {
//   console.log(item[0]);
// }

// for (let index of matchResult) {
//   console.log(index.index);
// }

// for (let { index } of matchResult) {
//   console.log(index);
// }
```
### Output:
```
Object [RegExp String Iterator] {}
////When we use only spread operator then we will get such kind of output
[
  'JavaScript',
  index: 6,
  input: 'Hello JavaScript, welcome to our world best JavaScript course',
  groups: undefined
] [
  'JavaScript',
  index: 44,
  input: 'Hello JavaScript, welcome to our world best JavaScript course',
  groups: undefined
]

JavaScript
JavaScript

6
44
```
# includes(): 
- **Returns true if the string contains the specified value, and false otherwise.**
- **Note: `includes()` is case sensitive. `includes()` is an ES6 feature.**
- **String.prototype.includes must not be a regular expression.Means we unable to use  `includes() with regular expression.`**
```
// let text = "Hello JavaScript, welcome to our world best JavaScript course";
// let includeResult = text.includes(/java/i); ////doesn't support regex
// let includeResult = text.includes("J");
// console.log(includeResult);
```
### Output:
```
true
```
# startsWith(): 
- **The startsWith() method returns true if a string begins with a specified value.Otherwise it returns false:**
```
let text = "Hello JavaScript, welcome to our world best JavaScript course";
// let result = text.startsWith("Helcome");
// let result = text.startsWith("Hello");
// console.log(result);
```
### Output:
```
false
true
```
- **start position for the search can be specified**
```
let result = text.startsWith("welcome", 18);
// let result = text.startsWith("welcome", 17);
console.log(result);
```
### Output:
```
true
false 
```
# endsWith(): 
- **The endsWith() method returns true if a string ends with a specified value. Otherwise it returns false:**
```
// let text = "Hello JavaScript, welcome to our world best JavaScript course";
// let result = text.endsWith("welcome");
// let result = text.endsWith("course");
// console.log(result);
```
### Output:
```
false
true
```
# slice():
![image](https://github.com/user-attachments/assets/a81f17c3-5237-4778-bcba-8d2300a9d960)
- **Extracts a part of a string and returns the extracted part in a new string.**
- **syntax:`slice(start, end);`**
- **JavaScript counts positions from zero.**
- **First position is 0. Second position is 1.**
### Example
```
let text = "Hello JavaScript, welcome to our world best JavaScript course";
let result = text.slice(6);===>6=(n-1)=6-1=5
let result = text.slice(6, 15);===>6=(n-1)=6-1=5 and ===>15=(n-1)=(15-1)=14
console.log(result);
```
### Output:
```
JavaScript, welcome to our world best JavaScript course
JavaScrip
```
### Another Example
```
const str = 'The quick brown fox jumps over the lazy dog.';

console.log(str.slice(31));
// Expected output: "the lazy dog."

console.log(str.slice(4, 19));
// Expected output: "quick brown fox"

console.log(str.slice(-4));
// Expected output: "dog."

console.log(str.slice(-9, -5));
// Expected output: "lazy"

let text = "Hello JavaScript, welcome to our world best JavaScript course";
// let result = text.slice(1);
console.log(result); ====>ello JavaScript, welcome to our world best JavaScript course
````
# substr()
![image](https://github.com/user-attachments/assets/a578d897-44ed-4cd6-b0d8-68bcb0d69fb7)
- **substr()==>It is used to fetch the part of the given string on the basis of the specified starting position and length.**
- **substring: Extracts a portion of the string based on starting and ending indices.**
- **substring()==>substr and substring() both the method are same but substring() method first index where we want to cut till the last index.**
- **String.prototype.substr() it is deprecated  ❌**
- **Both substr and substring() will change the main string**
- **substring() is similar to slice(). The difference is that start and end values less than 0 are treated as 0 in substring().**
- **syntax:`substring(indexStart, indexEnd)`**
```
// let text="Hello world"
// let res=text.substr(0,5)/////Here we want to fetch 5 character from 0th index
we have a String "Hello world" which consist of 12 charecter.Now we want "world" which starts.From 6th index and it up to the 10th index then we
pass substring(6,10)==> which return world but in substr(6,5) because world consist of 5 charecter that's the main difference.
// let res1=text.substr(6,5)/////Here we want to fetch 5 character from 6th index
// console.log(res)
// console.log(res1)
// console.log(res)
```
![image](https://github.com/user-attachments/assets/63b0dd27-a415-4517-bc00-c37121b32fa4)
```
let text="Hello world"
let res=text.substring(0,5)/////Here we want to fetch 5 character from 0th index
let res1=text.substring(6,11)/////Here we want to fetch 5 character from 6th index
console.log(res)
console.log(res1)
console.log(res)
```
![image](https://github.com/user-attachments/assets/ac141468-21b0-4ba0-acd4-4a7782ce7108)
```
let text = "Hello JavaScript, welcome to our world best JavaScript course";
// let result = text.substring(0); ====>Hello JavaScript, welcome to our world best JavaScript course
// let result = text.substring(1); ====>ello JavaScript, welcome to our world best JavaScript course
let result = text.substring(-5); ====>Hello JavaScript, welcome to our world best JavaScript course
console.log(result);
let text = "Hello JavaScript, welcome to our world best JavaScript course";
// let result = text.substring(1);
console.log(result); ====> ello JavaScript, welcome to our world best JavaScript course
```
- **replace()**
- **It replaces a given string with the specified replacement.**
```
let text="Hello world"
let res=text.replace("Hello","JavaScript")
let res1=text.replace("world","Java")
console.log(res)
console.log(res1)
/////Output:JavaScript world
/////       Hello Java
```
## Interview Question
- **What is the output for the following code**
```
let text = "Hello JavaScript, welcome to our world best JavaScript course";
let result = text.replace("H", ""); ====>ello JavaScript, welcome to our world best JavaScript course
// let result = text.replace("JavaScript", "Vinod");  ====>Hello Vinod, welcome to our world best JavaScript course
// let result = text.replaceAll("JavaScript", "Vinod"); ====>Hello Vinod, welcome to our world best Vinod course
console.log(result);
```

### toLowerCase()
- **It converts the given string into lowercase letters.**
```
const sentence = 'The quick brown fox jumps over the lazy dog.';
console.log(sentence.toLowerCase());
//// Expected output: "the quick brown fox jumps over the lazy dog."
```
### toUpperCase()
- **It converts the given string into the uppercase letter.**
```
 const sentence = 'The quick brown fox jumps over the lazy dog.';

 console.log(sentence.toUpperCase());
//// Expected output: "THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG."
```
### trim()
- **It trims the white space from the left and right sides of the string.**
```
const greeting = '   Hello world!   ';
console.log(greeting);
// Expected output: "   Hello world!   ";
console.log(greeting.trim());
// Expected output: "Hello world!";
```
