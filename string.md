# String
- **The JavaScript string is an object that represents a sequence of characters**
- **Strings in JavaScript are a fundamental data type that represents a sequence of characters.**
- **Strings created with single or double quotes works the same.**
# String Method()
- **charAt()**
- **It provides the char value present at the specified index.**
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
  >It provides the position of a char value present in the given string.
```
let text="Hello world"
let res=text.indexOf("H")
let res1=text.indexOf("e")
let res2=text.indexOf("o")
let res3=text.indexOf("w")
let res4=text.indexOf("d")
console.log(res)
console.log(res1)
console.log(res2)
console.log(res3)
console.log(res4)
//////Output: 0
//////        1
//////        4
//////        6
//////        10
```
- **lastIndexOf()**
  >It provides the position of a char value present in the given string by searching a character from the last position.
```
let text="Hello world"
let res=text.lastIndexOf("l")
let res1=text.lastIndexOf("o")
console.log(res)
console.log(res1)
//////Output: 9
//////        7
```
- **replace()**
  >It replaces a given string with the specified replacement.
```
let text="Hello world"
let res=text.replace("Hello","JavaScript")
let res1=text.replace("world","Java")
console.log(res)
console.log(res1)
/////Output:JavaScript world
/////       Hello Java
```
- **substr()**
  >substr()==>It is used to fetch the part of the given string on the basis of the specified starting position and length.
  >substring()==>It is used to fetch the part of the given string on the basis of the specified index.
   >>substring()==>substr and substring() both the method are same but substring() method first index where we want to cut
    >>>till the last index.Assume we have a String "Hello world" which consist of 12 charecter.Now we want "world" which starts
     >>>>from 6th index and it up to the 10th index then we pass substring(6,10)==> which return world but in substr(6,5) because
       world consist of 5 charecter that's the main difference.
#### **Both substr and substring() will change the main string**
```
// let text="Hello world"
// let res=text.substr(0,5)/////Here we want to fetch 5 character from 0th index
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
- **slice()**
  >It is used to fetch the part of the given string. It allows us to assign positive as well negative index.
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
````
- **toLowerCase()**
- >It converts the given string into lowercase letters.
```
const sentence = 'The quick brown fox jumps over the lazy dog.';
console.log(sentence.toLowerCase());
//// Expected output: "the quick brown fox jumps over the lazy dog."
```
- **toUpperCase()**
  >It converts the given string into the uppercase letter.
```
 const sentence = 'The quick brown fox jumps over the lazy dog.';

 console.log(sentence.toUpperCase());
//// Expected output: "THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG."
```
- **trim()**
 >It trims the white space from the left and right sides of the string.
```
const greeting = '   Hello world!   ';
console.log(greeting);
// Expected output: "   Hello world!   ";
console.log(greeting.trim());
// Expected output: "Hello world!";
```
