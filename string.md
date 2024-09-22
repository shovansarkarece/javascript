# String
-The JavaScript string is an object that represents a sequence of characters
# String Method()
- **charAt()**
  >It provides the char value present at the specified index.
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
