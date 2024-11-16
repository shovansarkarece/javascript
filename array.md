# Array
![image](https://github.com/user-attachments/assets/7b03e484-168d-4d02-b2b0-f93c69ca678e)

![image](https://github.com/user-attachments/assets/a5cb5357-b815-4a28-aca7-08b468fff80b)

![image](https://github.com/user-attachments/assets/4b3834ff-cee8-4e7a-a968-9c427f576637)

![image](https://github.com/user-attachments/assets/51e0dc93-a274-4e7b-948e-a9527b4b7fd3)

![image](https://github.com/user-attachments/assets/c1610464-081b-4d58-9fc4-128c6dd0cc79)

![image](https://github.com/user-attachments/assets/34ff553b-a507-4e31-a0f9-8ff19056d6ac)

![image](https://github.com/user-attachments/assets/96c51935-e5f5-47a8-92d6-50357ff3f98d)

### Arrays as Objects: 
- **Arrays in JavaScript are a specific type of object that has numeric keys (indices) and a length property. The indices are automatically maintained, and the length property is automatically updated when you add or remove elements from the array.**
- **typeof Operator: The typeof operator in JavaScript returns "object" for both arrays and regular objects.**
- **JavaScript Array is a data structure that allows you to store and organize multiple values within a single variable. It is a versatile and dynamic object. It can hold various data types, including numbers, strings, objects, and even other arrays. Arrays in JavaScript are zero-indexed i.e. the first element is accessed with an index 0, the second element with an index of 1, and so forth.**
# Creating Arrays:
- **Using Array constructor**
- `let fruits = new Array('apple', 'orange', 'banana')`
- **`console.log(fruits);`**
# Using array literal
- **`let fruits = ["apple", "orange", "banana"];`**
- **`console.log(fruits);`**
# We can also create an empty array
- **`let arr = [];`**
- **`console.log(typeof arr);`**

# Accessing Elements:
- **👉 Accessing Elements:  Array elements are accessed using zero-based indices.**
```
let fruits = ["apple", "orange", "banana"];
// console.log(fruits[0]);
// console.log(fruits[3]);
// console.log(fruits["apple"]);////undefined 
```
### Another Example
```
let App=["Android","IOS","Windows","Mac","Web"]
let city=["Dhaka","Rajshahi","Rangpur"]
let numbers=[1,40,50,40,3,2]
/////In js Array's index always start from 0
console.log(App)//-->Return whole array
console.log(App[0])//-->Aray's Index start from 0
console.log(App[1])//-->Aray's Index 1
console.log(city)//-->Return whole array
console.log(city[0])//-->Aray's Index start from 0 
console.log(city[1])//-->Aray's Index 1
console.log(numbers)//-->Return whole array
console.log(numbers[0])//-->Aray's Index start from 0 
console.log(numbers[1])//-->Aray's Index 1
```
![image](https://github.com/user-attachments/assets/05f415b2-07f8-4daa-9ab4-b65e0385f8f5)

### Modifying Elements:
- **👉  Modifying Elements: You can modify array elements by assigning new values to specific indices.**
```
let fruits = ["apple", "orange", "banana"];
// fruits[2] = "mango";
// console.log(fruits);
```
# Array Traversal / Iterating Over Arrays / Loop Over Array
### Loop Iteration 
```
let App=["Android","IOS","Windows","Mac","Web"]
for(i=0;i<App.length;i=i+1){
    console.log((i+1) +" "+App[i])
}
```
### Output:
![image](https://github.com/user-attachments/assets/58e63cda-e26f-409e-a518-7a80bb789e76)

## for of loop
- **Iterates over the values of an iterable object (such as arrays, strings, Maps, Sets, etc.).**
- **Does not give access to the index of the array or object keys; it gives only the values.**
- **When working with iterables (like arrays, strings, Sets, Maps, etc.).**
- **Allows the use of break, continue, and return (in a function context).When you want to use break or continue to control the flow of the loop.**
- **Syntax**
```
for (const value of iterable) {
//*  // code to execute on each element
//* }
```
### Example:
```
let fruits = ["apple", "orange", "mango", "grapes", "banana"];
for (const fruit of fruits) {
  console.log(fruit);  // logs 'apple', 'orange', 'mango'
}
```
### Output:
```
apple
orange
mango
grapes
banana
```
## for in loop
- **The for...in loop is used to iterate over the properties (including indices) of an object.**
- **Iterates over the keys (or property names) of an object or the indices of an array (or array-like objects).**
- **It works on objects (including arrays, but gives indices as strings) and other enumerable properties.**
- **The order of iteration is not guaranteed in all cases, especially for non-array objects.**
- **Not recommended for arrays if you need to access array elements directly (use for...of instead).**
- **Use for...in when you want to iterate over the keys of an object.When you need to iterate over the keys or properties of an object.**
- **When used with arrays, it will iterate over the array indexes (as strings), which is not the best practice for arrays since array indexes are numeric. Instead, use for...of to get the values directly.**
- **Syntax**
```
for (const value of Object) {
//*  // code to execute on each key
//* }
```
### Example:
```
let person = { name: "Alice", age: 25, city: "Wonderland" };
for (const key in person) {
  console.log(`Object's key/property is ${key},and Key's/Property's Value is ${person[key]}`);  // logs 'name Alice', 'age 25', 'city Wonderland'
}
```
### Output:
```
Object's key/property is name,and Key's/Property's Value is Alice
Object's key/property is age,and Key's/Property's Value is 25
Object's key/property is city,and Key's/Property's Value is Wonderland
```
## forEach Method
- **Array-specific method for iterating through array elements.**
- **Executes a provided function once for each element in the array (or array-like object).**
- **Provides access to both the element and the index (as the second argument).**
- **Does not return a value (always returns undefined), so it’s used primarily for side effects (e.g., logging, updating external variables).**
- **Does not support break, continue, or return within the callback function (it will not exit or skip iterations).**
- **forEach is array-specific, great for side effects like logging or modifying external state, but does not support early exits like break or continue.**
### Example:
```
// fruits.forEach((curElem, index, arr) => {
//    console.log(`Array is==> ${arr} Current Element is ==> ${curElem} and Index is ==>${index} `);
// });
```
### Output:
```
Array is==> apple,orange,mango,grapes,banana Current Element is ==> apple and Index is ==>0
Array is==> apple,orange,mango,grapes,banana Current Element is ==> orange and Index is ==>1
Array is==> apple,orange,mango,grapes,banana Current Element is ==> mango and Index is ==>2
Array is==> apple,orange,mango,grapes,banana Current Element is ==> grapes and Index is ==>3
Array is==> apple,orange,mango,grapes,banana Current Element is ==> banana and Index is ==>4
```
### Another Example
```
let App=["Android","IOS","Windows","Mac","Web"]
App.forEach((CurrentElement,index,array)=>{
  console.log(`Array is==> [${array}] Current Element is ==> ${CurrentElement} and Index is ==>${index} `);
})
```
### Output:
```
Array is==> [Android,IOS,Windows,Mac,Web] Current Element is ==> Android and Index is ==>0
Array is==> [Android,IOS,Windows,Mac,Web] Current Element is ==> IOS and Index is ==>1
Array is==> [Android,IOS,Windows,Mac,Web] Current Element is ==> Windows and Index is ==>2
Array is==> [Android,IOS,Windows,Mac,Web] Current Element is ==> Mac and Index is ==>3
Array is==> [Android,IOS,Windows,Mac,Web] Current Element is ==> Web and Index is ==>4
```
### write a program to Multiply each element with 2
```
const numbers = [1, 2, 3, 4, 5];
numbers.forEach((curElem) => {
  console.log(curElem * 2);
  //   Performs an action on each element
});
```
### Output:
```
2
4
6
8
10
```

# map()
>![image](https://github.com/user-attachments/assets/3066ec1d-34b4-4a55-af5d-f163be1108b0)
>>![image](https://github.com/user-attachments/assets/7c1dfe4f-4c8a-4f4a-a55b-c0f1a0bce4f1)
- **The map() method in JavaScript is used to create a new array by applying a callback function to each element of an existing array. It does not modify the original array but returns a new array with the results of the callback function.**
- **Parameters**
- **callback(currentValue, index, array):**
- **- **currentValue: The current element being processed.**
- **index (optional): The index of the current element.**
- **array (optional): The original array being traversed.**
- **thisArg (optional):**
- **A value to use as this inside the callback function.**
- **map() does not mutate the original array.**
- **It always returns a new array.The returned array will have the same length as the original array.**
- **Syntax:**
```array.map(callback(currentValue, index, array), thisArg)```
### Example
```
const numbers = [1, 2, 3, 4];
const squares = numbers.map(num => num * num);
console.log(`Mapped New Array is===> [${squares}]`); // [1, 4, 9, 16]
console.log(`Original Array is ===> [${numbers}]`); // [1, 2, 3, 4] (unchanged)
```
### Output:
```
Mapped New Array is===> [1,4,9,16]
Original Array is ===> [1,2,3,4]
```
### Another Example
```
const myMapArr = fruits.map((curElem, index, arr) => {
  return ` my fav fruit is ${curElem} `;
  //   console.log(arr);
});
console.log(myMapArr);
console.log(fruits);
```
### Output:
```
[
  ' my fav fruit is apple ',
  ' my fav fruit is orange ',
  ' my fav fruit is mango ',
  ' my fav fruit is grapes ',
  ' my fav fruit is banana '
]
[ 'apple', 'orange', 'mango', 'grapes', 'banana' ]
```
### Another Example
```
const fruits = ['apple', 'banana', 'cherry'];
const withIndex = fruits.map((fruit, index) => `Index is ${index}: and Value is ${fruit}`);
console.log(withIndex); // ["0: apple", "1: banana", "2: cherry"]
```
### Output:
```
[
  'Index is 0: and Value is apple',
  'Index is 1: and Value is banana',
  'Index is 2: and Value is cherry'
]
```
### Example of Using Object
```
const users = [
  { id: 1, name: 'Alice' },
  { id: 2, name: 'Bob' }
];
const userNames = users.map((user) => `Object Value is ${user.name}` );
console.log(userNames); // ['Alice', 'Bob']
```
### Output:
```
[ 'Object Value is Alice', 'Object Value is Bob' ]
```
### Write a program to Multiply each element with 2
```
const numbers = [1, 2, 3, 4, 5];
const doubleValue = numbers.map((curElem) => {
  return curElem * 2;
  //   Creates a new array with transformed elements
});
console.log(doubleValue);
```
# Key Differences between map() and forEach
- **Return Value:**
- **forEach: It doesn't return a value. The forEach method is used for iterating over the elements of an array and performing a side effect, such as modifying the array or performing a task for each element.**
- **map: It returns a new array containing the results of applying a function to each element in the original array. The original array remains unchanged.**
## Chaining:
- **forEach: It doesn't return a value, so it cannot be directly chained with other array methods.**
- **map: Since it returns a new array, you can chain other array methods after using map.**
## Use Case:
- **forEach: Used when you want to iterate over the array elements and perform an action on each element, but you don't need a new array.**
- **map: Used when you want to create a new array based on the transformation of each element in the original array.**
# Array Helping Methods
# How to Insert, Add, Replace and Delete Elements in Array(CRUD)
## PUSH()
  >The JavaScript array push() method adds one or more elements to the end of the given array.
![image](https://github.com/user-attachments/assets/67b0f992-779f-4715-92f3-5dfa3387c7fb)
![image](https://github.com/user-attachments/assets/65200d92-821c-4125-9711-a99f9b8c0541)

### Example
```
let ostadApp=["Android","IOS","Windows","Mac","Web"]
let res=ostadApp.push("Apple")
console.log(ostadApp)
```
### Output:
```
[ 'Android', 'IOS', 'Windows', 'Mac', 'Web', 'Apple' ]
```
### Another Example
```
let fruits = ["apple", "orange", "mango", "grapes", "banana"];
// console.log(fruits.push("guava"));
// console.log(fruits);
```
### Output:
```
[ 'apple', 'orange', 'mango', 'grapes', 'banana', 'guava' ]
```
## POP()
  >The JavaScript array pop() method removes the last element from the given array and return that element.
![image](https://github.com/user-attachments/assets/b47f621f-dd88-4087-8c47-9b83dafe8ef0)
![image](https://github.com/user-attachments/assets/a0c0f107-37a9-43e1-bd58-8ca62b37dc9d)


### Example 
```
let App=["Android","IOS","Windows","Mac","Web"]
let res=App.pop()
console.log(res)
```
### Output:
```
[ 'Android', 'IOS', 'Windows', 'Mac', 'Web' ]
Web
[ 'Android', 'IOS', 'Windows', 'Mac' ]
```
### Another Example 
```
let fruits = ["apple", "orange", "mango", "grapes", "banana"];
console.log(fruits);
// console.log(fruits.pop());
// console.log(fruits);
```
### Output:
```
[ 'apple', 'orange', 'mango', 'grapes', 'banana' ]
banana
[ 'apple', 'orange', 'mango', 'grapes' ]
```
# unshift(): Method that adds one or more elements to the beginning of an array
### Example:
```
let fruits = ["apple", "orange", "mango", "grapes", "banana"];
// console.log(fruits);
// console.log(fruits.unshift("guava"));
// console.log(fruits);
```
### Output:
```
[ 'apple', 'orange', 'mango', 'grapes', 'banana' ]
6
[ 'guava', 'apple', 'orange', 'mango', 'grapes', 'banana' ]
```
# shift(): Method that removes the first element from an array.
### Example:
```
let fruits = ["apple", "orange", "mango", "grapes", "banana"];
console.log(fruits);
console.log(fruits.shift());
console.log(fruits);
```
### Output:
```
[ 'guava', 'apple', 'orange', 'mango', 'grapes', 'banana' ]
guava
[ 'apple', 'orange', 'mango', 'grapes', 'banana' ]
```
# what if, we want to add or remove anywhere in an elements
# splice():
- **The splice() method of Array instances changes the contents of an array by removing or replacing existing elements and/or adding new elements in place**
- **Mutates the original array.The splice() method directly changes the array it is called on.**
- **`start (required)`:The index at which to begin changing the array. If negative, it indicates an offset from the end of the array.**
- **`deleteCount (optional)`:The number of elements to remove starting from the start index.**
- **If deleteCount is 0, no elements are removed.If omitted, all elements from start to the end of the array are removed.**
- **`item1, item2, ..., itemN (optional)`:Elements to add to the array starting at the start index. If no items are specified, the method only removes elements.**
- **syntax:`splice(start, deleteCount, item1, item2, /* …, */ itemN)`**
### 1.Removing elements:
```
let fruits = ["apple", "banana", "cherry", "date"];
let removed = fruits.splice(1, 2); // Removes 2 elements starting at index 1
console.log(fruits);  // Output: ["apple", "date"]
console.log(removed); // Output: ["banana", "cherry"]
```
### 2.Adding elements:
```
let fruits = ["apple", "date"];
fruits.splice(1, 0, "banana", "cherry"); // Adds "banana" and "cherry" at index 1
console.log(fruits);  // Output: ["apple", "banana", "cherry", "date"]
// let fruits = ["apple", "orange", "banana", "mango"];
// fruits.splice(1, 1, "grapes");
// console.log(fruits);
```
### 3.Replacing elements:
```
let fruits = ["apple", "banana", "cherry", "date"];
fruits.splice(1, 2, "grape", "kiwi"); // Removes 2 elements at index 1 and adds "grape" and "kiwi"
console.log(fruits);  // Output: ["apple", "grape", "kiwi", "date"]
```
### 4.Using negative indices:
```
let fruits = ["apple", "banana", "cherry", "date"];
fruits.splice(-2, 1); // Removes 1 element starting 2 places from the end
console.log(fruits);  // Output: ["apple", "banana", "date"]
```
### 5.Removing all elements after a certain index:
```
let fruits = ["apple", "banana", "cherry", "date"];
fruits.splice(2); // Removes everything from index 2 onward
console.log(fruits);  // Output: ["apple", "banana"]
```
### 6.Removing element at the end
```
// let fruits = ["apple", "orange", "banana", "mango"];
// fruits.splice(-1, 0, "grapes");
// fruits.splice(1, 0, "grapes");
// console.log(fruits);
```
- JAVASCRIPT ARRAY CONCAT()
  >The JavaScript array concat() method combines two or more arrays and returns a new string.
```
let first=['a','b','c']
let second=['d','e','f']
let res=first.concat(second)
console.log(res)
```
![image](https://github.com/user-attachments/assets/4181e9ed-b680-41cb-bb2e-4eb1c3cd9cf2)
- JAVASCRIPT ARRAY FROM()
>The from() method creates a new array that holds the shallow copy from an array or iterable object.
>>When applied to a string, each word gets converted to an array element in the new array
```
let nameString="Independence is the right of human being"
let nameArray=Array.from(nameString)
console.log(nameArray)
```
![image](https://github.com/user-attachments/assets/4af5c769-ef60-4d5e-bdd7-b6248d584296)
- **JAVASCRIPT ARRAY FILTER()**
>The JavaScript array filter() method filter and extract the element of an array that satisfying the provided condition.
```
let marks=[20,37,40,45,50,30,10,5]
function check(value){
    return value>30;
}
console.log(marks.filter(check));
```
![image](https://github.com/user-attachments/assets/a53ce305-e1f1-4c94-a53e-e258230ae00a)
- **JAVASCRIPT ARRAY FIND()**
>The JavaScript array find() method returns the first element of the given array that satisfies the provided function condition.
- **Example-1**
```
let ar=[5,22,19,25,34]
let res=ar.find(x=>x>20);
console.log(res);
////Output:22(Always first element will return)
```
- **Example-2**
```
let ar1=[5,25,19,22,34]
let res1=ar1.find(x=>x>20);
console.log(res1);
////Output:25(Always first element will return)
```
- **JAVASCRIPT ARRAY FINDINDEX()**
>The JavaScript array findIndex() method returns the index of first element of the given array that satisfies the provided function condition. 
>>It returns -1, if no element satisfies the condition.
- **Example-1**
```
let ar=[5,22,19,25,34]
let res=ar.findIndex(x=>x>20);
console.log(res);
////Output:1(Always first element's index will return)
```
- ***Example-2 ****
```
let ar1=[5,25,19,22,34]
let res1=ar1.findIndex(x=>x>20);
console.log(res1);
////Output:1(Always first element's index will return)
```
- JAVASCRIPT ARRAY INCLUDES()
  >The JavaScript array includes() method checks whether the given array contains the specified element. It returns true if an array contains the element, otherwise false.
```
let ostadApp=["Android","IOS","Windows","Mac","Web"]
let res=ostadApp.includes("Apple");
let res1=ostadApp.includes("WEB");
let res2=ostadApp.includes("WeB");
let res3=ostadApp.includes("Web");
console.log(res)
console.log(res1)
console.log(res2)
console.log(res3)
```
![image](https://github.com/user-attachments/assets/632ee5c5-5f11-4999-9134-cdcec1de9527)

- JAVASCRIPT ARRAY INDEXOF()
>The JavaScript array indexOf() method is used to search the position of a particular element in a given array. 
>>This method is case-sensitive.
```
let App=["Android","IOS","Windows","Mac","Web"]
let res=App.pop()
console.log(res)
let App=["Android","IOS","Windows","Mac","Web"]
let res=App.indexOf("Web")
console.log(res)
////Output:4
```


- JAVASCRIPT ARRAY REVERSE()
>The JavaScript array reverse() method changes the sequence of elements of the given array and returns the reverse sequence.
```
let App=["Android","IOS","Windows","Mac","Web"]
App.reverse();
console.log(App)
```
![image](https://github.com/user-attachments/assets/88bf640c-e7d7-4939-bcaa-75e42d2a5cdd)

- JAVASCRIPT ARRAY SLICE()
  >The JavaScript array slice() method extracts the part of the given array and returns it.
  >>This method doesn't change the original array

```
let ostadApp=["Android","IOS","Windows","Mac","Web"]
let res=ostadApp.slice(1,3); //// 1,2-->(n-1)-->(3-1)-->2
let res1=ostadApp.slice(1,4); //// 1,2,3-->(n-1)-->(4-1)-->3
let res2=ostadApp.slice(1,5); //// 1,2,3,4-->(n-1)-->(5-1)-->4
console.log(res);
console.log(res1);
console.log(res2);
```
![image](https://github.com/user-attachments/assets/9b67b325-ad30-46a2-876c-5280aa882205)
- JAVASCRIPT ARRAY SORT()
>The JavaScript array sort() method is used to arrange the array elements in some order.
>>By default, sort() method follows the ascending order.
```
let numbers=[30,55,44,20,77];
numbers.sort()////-->By default, sort() method follows the ascending order.
numbers.reverse()////-->But if we want to get the array in descending order then reverse it 
console.log(numbers);
```
![image](https://github.com/user-attachments/assets/05c1d3db-ea80-41e3-a86e-f5315e9d1f63)
# JAVASCRIPT ARRAY SPLICE()
>The JavaScript array splice() method is used to add/remove the elements to/from the existing array. 
>>It returns the removed elements from an array.
>>>*****The splice() method also modifies the original array.*****
- **Syntax:array.splice(index,removecount,item)**
```
let arr =["A","B","C","D","E"]
//////Example of Splice in terms of deletion
let res=arr.splice(2,2,"P","Q")////==>It means we can select from index 2 
////and susbstitute 2 elemenet at the place of C,D with P,Q
console.log(res);
console.log(arr);
```
![image](https://github.com/user-attachments/assets/9b3708eb-2d85-4afd-9f86-f9bf93640fa7)

#### Another Example of Splice in terms of deletion
```
let arr1 =["A","B","C","D","E"]
//////Example of Splice in terms of deletion
let res2=arr1.splice(2,2,)////==>It means we can select from index 2 
////and delete 2 elements from index 2
console.log(res2);
console.log(arr1);//////As we know splice() method, will change our main array.
```
![image](https://github.com/user-attachments/assets/da014796-5293-48df-8ff9-b566746f4d83)

