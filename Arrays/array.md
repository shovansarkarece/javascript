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
### Another Example
```
const months = ['January', 'February', 'March', 'April', 'May', 'December']
const capitalMonths = months.forEach((month, index) => {
    console.log(index + 1, month)
    return month.toUpperCase()
  })
console.log(capitalMonths);
```
### Output:
```
1 January
2 February
3 March
4 April
5 May
6 December
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
- **currentValue: The current element being processed.**
- **index (optional): The index of the current element.**
- **array (optional): The original array being traversed.**
- **thisArg (optional):**
- **A value to use as this inside the callback function.**
- **map() does not mutate the original array.**
- **It always returns a new array.The returned array will have the same length as the original array.**
- **Syntax:**
```array.map(callback(currentValue, index, array), thisArg)```
>![image](https://github.com/user-attachments/assets/db60e037-fabb-4764-be31-a63d297ed2e0)
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
### Another Example
```
const months = ['January', 'February', 'March', 'April', 'May', 'December']
const capitalMonths = months.map((month, index, array) => {
    console.log(index + 1, month)
    console.log(array);
    return month.toUpperCase()
  })
console.log(capitalMonths);
```
### Output:
```
1 January
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
2 February
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
3 March
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
4 April
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
5 May
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
6 December
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
[ 'JANUARY', 'FEBRUARY', 'MARCH', 'APRIL', 'MAY', 'DECEMBER' ]
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
# Interview Question for map()
### Using map to square each number and create a new array
```
// const numbers = [1, 2, 3, 4, 5];
// let result = numbers.map((curElem) => curElem * curElem);
// console.log(result);
```
### Using the map method, write a function that takes an array of strings and returns a new array where each string is capitalized.
```
// Original array of strings
// const words = ["APPLE", "banana", "cherry", "date"];

// const result = words.map((curElem) => {
//   return curElem.toLowerCase();
// });
// console.log(result);
```
### Using the map method, write a function that takes an array of numbers and returns a new array where each number is squared, but only if it's an even number.
```
// Original array of numbers
// const numbers = [1, 2, 3, 4, 5];

// const result = numbers
//   .map((curElem) => {
//     if (curElem % 2 === 0) {
//       return curElem * curElem;
//     }
//   })
//   .filter((curElem) => curElem !== undefined);
// console.log(result);
```
## Using Ternary Operator
```
// const evenSquare = numbers
//   .map((curNum) => (curNum % 2 === 0 ? curNum * curNum : undefined))
//   .filter((curElem) => curElem !== undefined);
// console.log(evenSquare);
```
### Using the map method, write a function that takes an array of names and returns a new array where each name is prefixed with "Mr. ".
```
// const names = ["ram", "vinod", "laxman"];
// const prefixName = names.map((curName) => `Mr. ${curName}`);
// console.log(prefixName);
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
# Filter in an array( Search + Filter )
## filter()
- **The JavaScript array `filter()` method filter and extract the element of an array that satisfying the provided condition.**
- **The `filter()` method in JavaScript is used to create a new array with elements that pass a specific test implemented by a provided callback function.**
- **It does not modify the original array.**
- **Does not mutate the original array.Unlike splice(), the filter() method creates a new array without altering the original array.**
- **Returns an empty array if no elements match.**
- **Syntax:`array.filter(callback(element, index, array), thisArg)`**
## Parameters:
### `callback (required)`:
- **A function that tests each element. It should return true to keep the element and false to exclude it.**
- **The callback function has three arguments:**
###`element`:
- **The current element being processed in the array.**
###`index (optional)`:
- **The index of the current element.**
###`array (optional)`: The array filter() was called on.
###`thisArg (optional)`:Value to use as this when executing the callback.
### Return Value:
- **A new array containing the elements that satisfy the condition.**
Examples:
### 1. Filtering numbers:
```
const numbers = [10, 20, 30, 40, 50];
const result = numbers.filter(num => num > 25); // Keep numbers greater than 25
console.log(result); 
```
### Output:
```
[30, 40, 50]
```
### 2.Filtering strings:
```
const fruits = ["apple", "banana", "cherry", "date"];
const result = fruits.filter(fruit => fruit.startsWith("b")); // Keep fruits starting with 'b'
console.log(result);
```
### Output: 
```
["banana"]
```
### 3.Using index in the callback:
```
const numbers = [5, 10, 15, 20, 25];
const result = numbers.filter((num, index) => index % 2 === 0); // Keep elements at even indices
console.log(result);
```
### Output: 
```
[5, 15, 25]
```
### 4.Filtering objects in an array:
```
const people = [
    { name: "Alice", age: 25 },
    { name: "Bob", age: 30 },
    { name: "Charlie", age: 22 }
];
const result = people.filter(person => person.age >= 25); // Keep people aged 25 or older
console.log(result);
```
### Output:
```
[{ name: "Alice", age: 25 }, { name: "Bob", age: 30 }]
```
### 5. Using thisArg:
```
const threshold = { limit: 15 };
const numbers = [10, 20, 30, 5];
const result = numbers.filter(function(num) {
    return num > this.limit;
}, threshold);
console.log(result);
```
### Output: 
```
[20, 30]
```
### 6.Returns an empty array if no elements match.
```
const nums = [1, 2, 3];
const result = nums.filter(n => n > 10);
console.log(result); 
```
### Output: 
```
 []
```
### 7.User wants to delete value 6.
```
let value = 6;
const numbers = [1, 2, 3, 4, 6, 5, 6, 7, 8, 9];

let updatedCart = numbers.filter((curElem) => {
  return curElem !== value;
});
console.log(updatedCart);
```
### Output:
```
[
  1, 2, 3, 4,
  5, 7, 8, 9
]
```
### 8.Filtering Products by Price
```
const products = [
  { name: "Laptop", price: 1200 },
  { name: "Phone", price: 800 },
  { name: "Tablet", price: 300 },
  { name: "Smartwatch", price: 150 },
];
//? Filter products with a price less than or equal to 500
const filterProducts = products.filter((curElem) => {
  //   console.log(curElem.price <= 500);
  return curElem.price <= 500;
});
console.log(filterProducts);
```
### output:
```
[ { name: 'Tablet', price: 300 }, { name: 'Smartwatch', price: 150 } ]
```
### 9.Filter unique values
```
const numbers = [1, 2, 3, 4, 6, 5, 6, 7, 8, 9];
let uniqueValues = numbers.filter((curElem, index, arr) => {
    // console.log(index);
    console.log(arr.indexOf(curElem));
//   return arr.indexOf(curElem) === index;
});
// console.log(uniqueValues);
// console.log([...new Set(numbers)]);
console.log(marks.filter(check));
```
```
console.log(index);
1
2
3
4
5
6
7
8
9
console.log(arr.indexOf(curElem));
0
1
2
3
4
5
4 here index 4 is coming as Output because element 6 is available in the 4th index as well as the 6th index. Because the indexof() always returns first index that's why it is updated 6th  index as the 4th index.
7
8
9
return arr.indexOf(curElem) === index;
[
  1, 2, 3, 4, 6,
  5, 7, 8, 9
]
```
### Another Example
```
const months = ['January', 'February', 'March', 'April', 'May', 'December']
const filteredMonths = months.filter((month, index, array) => {
    console.log(month.toLocaleLowerCase().includes('m'))
    console.log(array);
    return month.toLocaleLowerCase().includes('m')
  })
console.log(filteredMonths);
```
### Output:
```
false
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
false
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
true
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
false
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
true
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
true
[ 'January', 'February', 'March', 'April', 'May', 'December' ]
[ 'March', 'May', 'December' ]
```
### Combined example of map() and filter() method
```
const students = [
    {
        name: 'Akash',
        age: 21,
    },
    {
        name: 'Adarsh',
        age: 17,
    },
    {
        name: 'Amir',
        age: 18,
    },
    {
        name: 'Raman',
        age: 23,
    },
    {
        name: 'Nidhi',
        age: 16,
    },
]
const adultStudents = students.filter((student) => {
    return student.age >= 18
}).map((student) => {
    return student.name
}).filter((student) => {
    return student.includes('A')
})
console.log(adultStudents)
```
### Outpt:
```
[ 'Akash', 'Amir' ]
```
# reduce() method
- **The reduce method in JavaScript is used to accumulate or reduce an array to a single value.**
- **It iterates over the elements of an array and applies a callback function to each element, updating an accumulator value with the result.**
- **The reduce method takes a callback function as its first argument and an optional initial value for the accumulator as the second argument.**
- **syntax:**
```
array.reduce(function callback(accumulator, currentValue, index, array) {
//   // Your logic here
//   // Return the updated accumulator value
// }, initialValue);
```
- **`callback`: A function that is called once for each element in the array.**
- **`accumulator`: The accumulated result of the previous iterations.**
- **`currentValue`: The current element being processed in the array.**
- **`index (optional)`: The index of the current element being processed.**
- **`array (optional)`: The array reduce was called upon.**
- **`initialValue (optional)`: An initial value for the accumulator. If not provided, the first element of the array is used as the initial accumulator value.**
### Example
```
// const productPrice = [100, 200, 300, 400, 500];
// const totalPrice = productPrice.reduce((accum, curElem) => {
//   return accum + curElem;
// }, 0);
// console.log(totalPrice);
```
### Output:
```
1500
```
### Another Example
```
const nums = [1, 2, 3, 4, 5]
const sum = nums.reduce((accumulator, current, i) => {
    console.log(Index is ${i}, and element is ${current});
    console.log(Accumulator is ${accumulator});
    // return accumulator * current
    return accumulator + current
}, 0)
```
### Output:
```
Index is 0, and element is 1
Accumulator is 0
Index is 1, and element is 2
Accumulator is 1
Index is 2, and element is 3
Accumulator is 3
Index is 3, and element is 4
Accumulator is 6
Index is 4, and element is 5
Accumulator is 10
```
# Combined example of map(),filter() and reduce()
### When to Use:
- **Use map() when you want to transform each element.**
- **Use filter() when you want to extract a subset of elements.**
- **Use reduce() when you want a single, cumulative result.**
```
const numbers = [1, 2, 3, 4, 5, 6];
// 1. Filter even numbers
const evens = numbers.filter(num => num % 2 === 0); // [2, 4, 6]
// 2. Square the even numbers
console.log(evens);
const squaredEvens = evens.map(num => num * num); // [4, 16, 36]
// 3. Sum the squared even numbers
console.log(squaredEvens);
const sumOfSquares = squaredEvens.reduce((acc, num) => acc + num, 0); // 56
console.log(sumOfSquares); // Output: 56
```
### Output:
```
[2, 4, 6]
[4, 16, 36]
56
```
# Difference between map(),filter() and reduce()
![image](https://github.com/user-attachments/assets/e7521f18-3e3b-41d9-91a3-05e8c2c2ca6e)
# find()
- **syntax:`array.find(callback(element, index, array), thisArg)`**
- **`callback (required)`:A function to test each element of the array.It takes three arguments**
- **`element`: The current element being processed.**
- **`index (optional)`: The index of the current element.**
- **`array (optional)`: The array find() was called on.**
- **`thisArg (optional)`:A value to use as this when executing the callback function.**
- **Returns the first element that satisfies the condition specified in the callback.**
- **Returns undefined if no elements match the condition.**
- **The find() method is non-destructive and leaves the original array unchanged.**
- **Once the find() method finds a matching element, it stops processing the rest of the array.**
- **If you need the index, consider using the findIndex() method.**
### 1.Finding an element in an array:
```
let numbers = [10, 20, 30, 40];
let result = numbers.find(num => num > 25);
console.log(result); // Output: 30 (first number greater than 25)
```
### Output:
```
30
```
### Another Example
```
const numbers = [1, 2, 3, 4, 5, 4, 6, 7, 8, 6, 9];
const result = numbers.find((curElem) => {
  return curElem > 6;
});
console.log(result);
```
### Output:
```
7
```
### 2.Using find() with objects:**
```
let users = [
  { id: 1, name: "Alice" },
  { id: 2, name: "Bob" },
  { id: 3, name: "Charlie" }
];
let user = users.find(user => user.name === "Bob");
console.log(user); // Output: { id: 2, name: "Bob" }
```
### Output:
```
{ id: 2, name: 'Bob' }
```
### 3. No match found:**
```
let numbers = [1, 2, 3, 4];
let result = numbers.find(num => num > 5);
console.log(result); // Output: undefined
```
### Output:
```
undefined
```
### 4. Using thisArg:**
```
let obj = {
  threshold: 15
};
let numbers = [10, 20, 30];
let result = numbers.find(function(num) {
  return num > this.threshold;
}, obj);
console.log(result); // Output: 20
```
### Output:
```
20
```
### Another Example:
```
let ar=[5,22,19,25,34]
let res=ar.find(x=>x>20);
console.log(res);
```
### Output:
```
22
```
### Another Example:
```
let ar1=[5,25,19,22,34]
let res1=ar1.find(x=>x>20);
console.log(res1);
```
### Output:
```
25
```
# some()
- **In JavaScript, the some() and every() methods are array methods that test elements of an array against a condition specified in a callback function. Here's how they work:**
- **Purpose: Tests whether at least one element in the array passes the test implemented by the provided function.**
- **Returns: A boolean (true or false).**
- **Syntax:`array.some(callback(element, index, array), thisArg)`**
### Parameters:
- **callback: A function that is executed for each element in the array. It takes three arguments:**
- **element: The current element being processed.**
- **index (optional): The index of the current element.**
- **array (optional): The array some() was called on.**
- **thisArg (optional): An optional object to use as this inside the callback function.**
### Example:
```
const numbers = [1, 2, 3, 4, 5];
// Check if there is at least one number greater than 3
const hasNumberGreaterThanThree = numbers.some(num => num > 3);
console.log(hasNumberGreaterThanThree); // Output: true
```
# every()
- **Purpose: Tests whether all elements in the array pass the test implemented by the provided function.**
- **Returns: A boolean (true or false).**
- **Syntax:`array.every(callback(element, index, array), thisArg)`
### Parameters:
- **callback: A function that is executed for each element in the array. It takes three arguments:**
- **element: The current element being processed.**
- **index (optional): The index of the current element.**
- **array (optional): The array every() was called on.**
- **thisArg (optional): An optional object to use as this inside the callback function.**
### Example:
```
const numbers = [1, 2, 3, 4, 5];
// Check if all numbers are less than 6
const allLessThanSix = numbers.every(num => num < 6);
console.log(allLessThanSix); // Output: true
```
### Key Differences
- **Logic:**
- **some() returns true if any element satisfies the condition.**
- **every() returns true only if all elements satisfy the condition.**
### Early Exit:
- **Both methods stop iterating as soon as the result is determined:**
- **some() stops on the first true.**
- **every() stops on the first false.**
- **Return Value:Both methods return a boolean value (true or false).**
### Combined Example:
```
const numbers = [10, 15, 20, 25, 30];

// Check if at least one number is even
console.log(numbers.some(num => num % 2 === 0)); // Output: true

// Check if all numbers are greater than 5
console.log(numbers.every(num => num > 5)); // Output: true
These methods are very useful for quickly testing array contents against specific conditions!
```
### Another Combined Example:
```
const evenNumbers = [0, 2, 10, 4, 61, 8]
const result = evenNumbers.some((num, i) => {
    if(num % 2 === 1) {
        console.log(i);
    }
    return num % 2 === 1
})
console.log(result);
// const result = evenNumbers.every((num) => {
//     debugger
//     return num % 2 === 0
// })
// console.log(result);
```
# findIndex()
- **findIndex Method: The findIndex() method of TypedArray instances returns the index of the first element in a typed array that satisfies the provided testing function. If no elements satisfy the testing function, -1 is returned.**
- **synax:`array.findIndex(callback(element, index, array), thisArg)`**
- **`callback (required)`:A function that tests each element of the array. It is called with the following arguments:**
- **`element`: The current element being processed.**
- **`index`: The index of the current element.**
- **`array`: The entire array being traversed.**
- **`thisArg (optional)`:An object to use as this when executing the callback. Defaults to undefined.**
- **Does not mutate the array.The findIndex() method does not change the original array.**
- **Stops at the first match.Once a matching element is found, the method stops further iteration.**
### Return Value:
- **The index of the first element that satisfies the condition.-1 if no elements satisfy the condition.**
- **Example Use Cases:**
### 1. Finding the index of a number in an array:**
```
const numbers = [10, 20, 30, 40];
const index = numbers.findIndex(num => num > 25); // Finds the first number greater than 25
console.log(index);  // Output: 2
```
### Output:
```
2
```
### Another Example
```
let ar=[5,22,19,25,34]
let res=ar.findIndex(x=>x>20);
console.log(res);
```
### Output:
```
1 =====>(Always first element's index will return)
```
### Another Example
```
let ar1=[5,25,19,22,34]
let res1=ar1.findIndex(x=>x>20);
console.log(res1);
```
### Output:
```
1   =====>(Always first element's index will return)
```
### 2. Finding the index of an object in an array:
```
const users = [
  { id: 1, name: "Alice" },
  { id: 2, name: "Bob" },
  { id: 3, name: "Charlie" }
];
const index = users.findIndex(user => user.name === "Bob");
console.log(index); 
```
### Output:
```
1
```
### 3. Checking for non-existent conditions:
```
const numbers = [10, 20, 30, 40];
const index = numbers.findIndex(num => num > 50); // No number greater than 50
console.log(index);
```
### Output:
```
-1
```
### 4. Using thisArg:
```
const threshold = { limit: 15 };
const numbers = [10, 20, 30, 40];
const index = numbers.findIndex(function(num) {
  return num > this.limit;
}, threshold);
console.log(index);
```
### Output: 
```
1
```
# Array Helping Methods
# How to Insert,Add,Replace and Delete Elements in Array(CRUD)
## push()
- **The JavaScript array `push()` method adds one or more elements to the end of the given array.**
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
## pop()
- **The JavaScript array pop() method removes the last element from the given array and return that element.**
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
# shift():Method that removes the first element from an array.
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
# What if, we want to add or remove anywhere in an elements
# splice():
- **The splice() method of Array instances changes the contents of an array by removing or replacing existing elements and/or adding new elements in place**
- **Mutates the original array.The splice() method directly changes the array it is called on.**
- **`start (required)`:The index at which to begin changing the array. If negative, it indicates an offset from the end of the array.**
- **`deleteCount (optional)`:The number of elements to remove starting from the start index.**
- **If deleteCount is 0, no elements are removed.If omitted, all elements from start to the end of the array are removed.**
- **`item1, item2, ..., itemN (optional)`:Elements to add to the array starting at the start index. If no items are specified, the method only removes elements.**
- **syntax:`splice(start, deleteCount, item1, item2, /* …, */ itemN)`**
- **What is the return value of splice method?==>When used to add elements, the splice method returns an empty array ([]).**
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
console.log(fruits);  
```
### Output: 
```
["apple", "grape", "kiwi", "date"]
```
### Another example of Replacing elements:
```
let arr =["A","B","C","D","E"]
//////Example of Splice in terms of deletion
let res=arr.splice(2,2,"P","Q")////==>It means we can select from index 2 
////and susbstitute 2 elemenet at the place of C,D with P,Q
console.log(res);
console.log(arr);
```
### Output: 
![image](https://github.com/user-attachments/assets/9b3708eb-2d85-4afd-9f86-f9bf93640fa7)

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
#### Another Example of Splice in terms of deletion
```
let arr1 =["A","B","C","D","E"]
//////Example of Splice in terms of deletion
let res2=arr1.splice(2,2,)////==>It means we can select from index 2 and delete 2 elements from index 2
console.log(res2);
console.log(arr1);//////As we know splice() method, will change our main array.
```
### Output: 
![image](https://github.com/user-attachments/assets/da014796-5293-48df-8ff9-b566746f4d83)
### 6.Removing element at the end
```
// let fruits = ["apple", "orange", "banana", "mango"];
// fruits.splice(-1, 0, "grapes");
// fruits.splice(1, 0, "grapes");
// console.log(fruits);
```
### Delete June from an array?
```
const months = ["Jan", "march", "April", "June", "July"];
const indexToDelete = months.indexOf("June");
months.splice(indexToDelete, 1);
console.log(months);
```
### Output:
```
[ 'Jan', 'march', 'April', 'July' ]
```
### Add Dec at the end of an array?
```
const months = ["Jan", "march", "April", "June", "July"];
months.splice(months.length, 0, "Dec");
console.log(months);
```
### Output:
```
[ 'Jan', 'march', 'April', 'June', 'July', 'Dec' ]
```
### Update march to March (update)?
```
const months = ["Jan", "march", "April", "June", "July"];
const indexToUpdate = months.indexOf("march");
months.splice(indexToUpdate, 1, "March");
console.log(months);
```
### Output:
```
[ 'Jan', 'March', 'April', 'June', 'July' ]
```
## concat()
- **The JavaScript array concat() method combines two or more arrays and returns a new string.**
```
let first=['a','b','c']
let second=['d','e','f']
let res=first.concat(second)
console.log(res)
```
### Output:
![image](https://github.com/user-attachments/assets/4181e9ed-b680-41cb-bb2e-4eb1c3cd9cf2)
## from()
- **The from() method creates a new array that holds the shallow copy from an array or iterable object.**
- **When applied to a string, each word gets converted to an array element in the new array**
```
let nameString="Independence is the right of human being"
let nameArray=Array.from(nameString)
console.log(nameArray)
```
![image](https://github.com/user-attachments/assets/4af5c769-ef60-4d5e-bdd7-b6248d584296)
# includes()
![image](https://github.com/user-attachments/assets/3b89d799-bf00-419f-8278-0ee2f82f2790)
- **The JavaScript array includes() method checks whether the given array contains the specified element. It returns true if an array contains the element, otherwise false.**
- **Syntax:`includes(searchElement, fromIndex)`**
### Example
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
### Another Example
```
const numbers = [1, 2, 3, 6, 4, 5, 6, 7, 8, 9];
const result = numbers.includes(5);
const result = numbers.includes(5,2);
console.log(result);
```
### Output:
```
true
true
```
# indexOf()
![image](https://github.com/user-attachments/assets/d57b971e-5f99-4867-8d8b-74344dcffa11)
- **indexOf Method: The indexOf method returns the first index at which a given element can be found in the array, or -1 if it is not present.**
- **syntax:`indexOf(searchElement, fromIndex)`
### Example:
```
const numbers = [1, 2, 3, 4, 6, 5, 6, 7, 8, 4, 10];
console.log(numbers.indexOf(4, 5));
```
### Output:
![image](https://github.com/user-attachments/assets/60713001-75d7-4540-bf94-96a88aa57f7f)
```
9
10
```
### Another Example
```
let App=["Android","IOS","Windows","Mac","Web"]
let res=App.indexOf("Web")
console.log(res)
```
### Output:
```
4
```
# lastIndexof()
- **lastIndexOf Method: The lastIndexOf() method of Array instances returns the last index at which a given element can be found in the array, or -1 if it is not present.**
- **The array is searched backwards(from ledt to right), starting at fromIndex.**
### Example
```
const numbers = [1, 2, 3, 6, 4, 5, 6, 7, 8, 9];
// const result = numbers.lastIndexOf(6);
// console.log(result);
```
### Output:
```
3
```
### Another Example
```
const numbers = [1, 2, 3, 6, 4, 5, 6, 7, 8, 9];
const result = numbers.lastIndexOf(6, 5);
console.log(result);
```
### Output:
```
3
```
### Another Example
```
const numbers = [1, 2, 3, 6, 4, 5, 6, 7, 8, 9];
const result = numbers.lastIndexOf(6, 8);
console.log(result);
```
### Output:
```
6
```
![image](https://github.com/user-attachments/assets/f8abdc97-582a-4dfc-983d-c0ed619828ab)
# reverse()
- **The JavaScript array reverse() method changes the sequence of elements of the given array and returns the reverse sequence.**
```
let App=["Android","IOS","Windows","Mac","Web"]
App.reverse();
console.log(App)
```
![image](https://github.com/user-attachments/assets/88bf640c-e7d7-4939-bcaa-75e42d2a5cdd)
# slice()
- **The JavaScript array slice() method extracts the part of the given array and returns it.**
- **This method doesn't change the original array**
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
# sort()
- **The JavaScript array sort() method is used to arrange the array elements in some order.**
- **By default, sort() method follows the ascending order.**
- **Sorting an Array: The sort method sorts the elements of an array in place and returns the sorted array. By default, it sorts elements as strings.**
```
let numbers=[30,55,44,20,77];
numbers.sort()////-->By default, sort() method follows the ascending order.
numbers.reverse()////-->But if we want to get the array in descending order then reverse it 
console.log(numbers);
```
![image](https://github.com/user-attachments/assets/05c1d3db-ea80-41e3-a86e-f5315e9d1f63)
### For ascending order in terms of sort
```
// const numbers = [1, 2, 4, 3, 6, 5, 6, 7, 4, 8, 9];
// const sortedNumbers = numbers.sort((a, b) => {
//   if (a > b) {
//     return 1;
//   } else if (b > a) {
//     return -1;
//   }
// });
// console.log(numbers);
```
### Output:
```
[
  1, 2, 3, 4, 4,
  5, 6, 6, 7, 8,
  9
]
```
### For descending order in terms of sort
```
// const sortedNumbers = numbers.sort((a, b) => {
//   if (a > b) {
//     return -1;
//   } else if (b > a) {
//     return 1;
//   }
// });
// console.log(numbers);
```
### Output:
```
[
  9, 8, 7, 6, 6,
  5, 4, 4, 3, 2,
  1
]
```
# Default Parameters
- **Functions can define default values for parameters, which are used if no argument (or undefined) is passed.**
### Example:
```
function greet(name = "Guest") {
    console.log("Hello, " + name + "!");
}

greet();           // Output: Hello, Guest!
greet("Alice");    // Output: Hello, Alice!

function multiply(a, b = 1) {
  return a * b
}

function rollADie(numberOfSides = 6) {
  return Math.floor(Math.random() * numberOfSides) + 1
}
```
# The arguments Object
- **In non-arrow functions, arguments is an array-like object that contains all the arguments passed to the function.**
- **It's useful when the number of arguments is not fixed or exceeds the defined parameters.**
### Key Characteristics:
- **It's not a real array (no array methods like .map() or .filter()), but it can be converted to an array using Array.from() or the spread operator (...).**
- **Accessible only in traditional (non-arrow) functions.**
- **Arrow functions do not have arguments, so rely on rest parameters for dynamic argument handling.**
### Example:
```
function sum() {
    let total = 0;
    for (let i = 0; i < arguments.length; i++) {
        total += arguments[i];
    }
    return total;
}

console.log(sum(1, 2, 3, 4));
// Output: 10

///Convert arguments to an Array:
javascript
Copy code
function listArguments() {
    const args = Array.from(arguments); // Convert to a real array
    return args.join(", ");
}

console.log(listArguments("a", "b", "c"));
// Output: a, b, c

function add1(){
    let sum=0;
    for(let i=0;i<arguments.length;i++){
        sum = sum+arguments[i];
    }
    return sum;
}
console.log(add1(10,20,30,40,50))
// Output:150

const add2=function(){
    let sum=0;
    for(let i=0;i<arguments.length;i++){
        sum = sum+arguments[i];
    }
    return sum;
}
console.log(add2(10,20,30,40,50))
// Output:150
```

# In JavaScript, `spread (...)` and `rest (...)` are represented by the same syntax (...), but they serve very different purposes based on where and how they are used:

# Spread Operator
- **The spread operator (...) is used to expand or "spread" elements of an iterable (like arrays, objects, or strings) into individual elements.**

## Use Cases:
### 1.Expanding Arrays: Spread an array into individual elements.
```
const numbers = [1, 2, 3];
console.log(...numbers);
// Output: 1 2 3
```
### 2.Copying Arrays: Create a shallow copy of an array.
```
const original = [1, 2, 3];
const copy = [...original];
console.log(copy); // Output: [1, 2, 3]
```
### 3.Merging Arrays: Combine arrays into a new array.
```
const arr1 = [1, 2];
const arr2 = [3, 4];
const merged = [...arr1, ...arr2];
console.log(merged);
// Output: [1, 2, 3, 4]
/////Another Example
const nums1 = [1, 2, 3, 4]
const nums2 = [5, 6, 7, 8, 9]

const myName = 'Anurag'

const joinedArray = [...nums1, ...nums2, 10, 11, 12, ...myName]
////Outpt:
[
  1,   2,   3,   4,   5,  6,   7,
  8,   9,   10,  11,  12, 'A', 'n',
  'u', 'r', 'a', 'g'
]
```
### 4.Passing Elements to Functions: Spread array elements as arguments to a function.
```
const nums = [1, 2, 3];
const sum = (a, b, c) => a + b + c;
console.log(sum(...nums));
// Output: 6
```
### 5.Copying or Merging Objects: Spread properties of objects into a new object.
```
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };
const merged = { ...obj1, ...obj2 };
console.log(merged);
// Output: { a: 1, b: 2, c: 3, d: 4 }
/////Another Example
const user = {
    name: 'Anurag',
    age: 25,
}
const updatedUser = {...user, city: 'Bangalore'}
console.log(updatedUser);
// Output:{ name: 'Anurag', age: 25, city: 'Bangalore' }
```
# Rest Parameter
- **The rest operator (...) is used to collect multiple elements or properties into a single array or object. It is typically used in function parameters or destructuring assignments.**
- **A rest parameter must be last in a parameter list.If in rest parameter we are passing nothing then it will return empty array[]**
# Use Cases:
### Function Parameters: 
- **Gather all remaining arguments into a single array.**
```
function sum(...nums) {
    return nums.reduce((total, num) => total + num, 0);
}
console.log(sum(1, 2, 3, 4));
// Output: 10
```
### Destructuring Arrays: 
- **Collect the "rest" of the elements into a new array during array destructuring.**
```
const [first, second, ...rest] = [1, 2, 3, 4, 5];
console.log(first);
// Output: 1
console.log(second);
// Output: 2
console.log(rest);
// Output: [3, 4, 5]
```
### Destructuring Objects: 
- **Collect the "rest" of the properties into a new object during object destructuring.**
```
const { a, b, ...rest } = { a: 1, b: 2, c: 3, d: 4 };
console.log(a); // Output: 1
console.log(b); // Output: 2
console.log(rest); // Output: { c: 3, d: 4 }
```
# Key Differences Between Spread and Rest
![image](https://github.com/user-attachments/assets/34e7f1f1-9c3f-4c8f-a83a-180881b844d6)
### Combined example of rest and spread
```
// Using Rest in function parameters
function greet(greeting, ...names) {
    return `${greeting} ${names.join(", ")}`;
}
console.log(greet("Hello", "Alice", "Bob", "Charlie"));
// Output: Hello Alice, Bob, Charlie

// Using Spread to pass arguments
const numbers = [1, 2, 3];
console.log(Math.max(...numbers));
// Output: 3

// Destructuring with Rest and using Spread to merge arrays
const [first, ...rest] = [1, 2, 3, 4];
const newArray = [0, ...rest];
console.log(newArray);
// Output: [0, 2, 3, 4]

function add(a, b, c, ...nums) {
    console.log(a, b, c);
    console.log('nums:', nums);
}
add(100,200,300,400,500,600,700,800,900)
//// Output:
100 200 300
nums: [ 400, 500, 600, 700, 800, 900 ]
```
### Combined example of rest,spread and reduce
```
const nums1 = [1, 2, 3, 4]
function add() {
  return [...arguments].reduce((acc, curr) => acc + curr)
}
const result = add(...nums1)
console.log(result);
//// Output:10
const nums1 = [1, 2, 3, 4]
function add(...nums) {
  return nums.reduce((acc, curr) => acc + curr)
}
const result = add(...nums1)
console.log(result);
//// Output:10
const nums1 = [1, 2, 3, 4]
// function add() {
//   return Array.from(arguments).reduce((acc, curr) => acc + curr)
// }
//// Output:10
```
### Destructuring in JavaScript 
- **Destructuring in JavaScript is a convenient way to unpack values from arrays or properties from objects into distinct variables. It was introduced in ECMAScript 2015 (ES6) and provides a concise syntax for extracting data, improving readability and efficiency.**
- **Destructuring simplifies code and is widely used in modern JavaScript programming!**

### Array Destructuring
- **We can extract values from an array and assign them to variables:**
```
const numbers = [1, 2, 3];

// Destructuring assignment
const [a, b, c] = numbers;

console.log(a); // 1
console.log(b); // 2
console.log(c); // 3
/////Another Example
const colors = ['red', 'green', 'yellow', 'pink', 'black', 'white']

// const color1 = colors[0]
// const color2 = colors[1]
// const color3 = colors[2]
/////Another way of array destructuring
const [color1, color2, color3] = colors
/////Another way of array destructuring
// const [,,,color4] = colors
/////Another way of array destructuring
const { 3: color4, 5: color5 } = colors
```
### Skipping Values
 - **We can skip elements by leaving a blank space:**
```
const numbers = [1, 2, 3, 4];

const [first, , third] = numbers;

console.log(first); // 1
console.log(third); // 3
```
### Default Values
- **If a value is undefined, you can specify a default:**
```
const numbers = [1];

const [a, b = 10] = numbers;

console.log(a); // 1
console.log(b); // 10
```
# Object Destructuring
- **For objects, you can extract properties by matching variable names to property names:**
- **In case of object destructuring if there is no property available then we will get undefined.**
```
const person = { name: 'Alice', age: 25 };

// Destructuring assignment
const { name, age } = person;

console.log(name); // Alice
console.log(age); // 25
////// Another Example
const user = {
  name: 'Anurag',
  age: 25,
  address: {
    city: 'Bangalore',
    state: 'Karnataka',
  },
}

// const name = user.name
// const age = user.age

const { name, age } = user

// const { name: username, age: userAge } = user

// const { address: {city} } = user
// const { address } = user
// const { city } = address
```
# Renaming Variables
- **You can rename variables during destructuring:**
```
const person = { name: 'Alice', age: 25 };

const { name: fullName, age: years } = person;

console.log(fullName); // Alice
console.log(years); // 25
```
# Default Values
- **Provide a default for missing properties:**
```
const person = { name: 'Alice' };

const { name, age = 30 } = person;

console.log(name); // Alice
console.log(age); // 30
```
# Nested Destructuring
- **We can destructure nested arrays or objects:**
```
const numbers = [1, [2, 3]];

const [a, [b, c]] = numbers;

console.log(a); // 1
console.log(b); // 2
console.log(c); // 3
```
# Nested Objects
```
const person = { name: 'Alice', address: { city: 'Wonderland', zip: 12345 } };

const { address: { city, zip } } = person;

console.log(city); // Wonderland
console.log(zip); // 12345
```
# Rest Pattern
- **We can use the rest pattern to gather remaining elements or properties:**
```
const numbers = [1, 2, 3, 4];

const [a, b, ...rest] = numbers;

console.log(a); // 1
console.log(b); // 2
console.log(rest); // [3, 4]
```
# Objects
```
const person = { name: 'Alice', age: 25, profession: 'Engineer' };

const { name, ...rest } = person;

console.log(name); // Alice
console.log(rest); // { age: 25, profession: 'Engineer' }
```
# Practical Applications
### Function Arguments:
```
//////Object  Destructuring using Function 
///// Example
const user = {
  name: 'Anurag',
  age: 25,
  address: {
    city: 'Bangalore',
    state: 'Karnataka',
  },
}
// Function that destructures all properties
function getUserDetails({ name, age, address: { city, state } }) {
  return Name: ${name}, Age: ${age}, City: ${city}, State: ${state};
}
// Call the function
console.log(getUserDetails(user));
////// Output: "Name: Anurag, Age: 25, City: Bangalore, State: Karnataka"
//////? If you need all properties but don't want to list them explicitly:
function getUserDetails(user) {
  const { name, age, address: { city, state } } = user;
  return { name, age, city, state }; // Return as an object if needed
}
console.log(getUserDetails(user));
////// Output: { name: 'Anurag', age: 25, city: 'Bangalore', state: 'Karnataka' }

//////Array Destructuring using Function 
function greet({ name, age }) {
  console.log(`Hello, ${name}. You are ${age} years old.`);
}

const person = { name: 'Alice', age: 25 };
greet(person); // Hello, Alice. You are 25 years old.

const colors = ['red', 'green', 'yellow', 'pink', 'black', 'white']
function printColor([a, b,,,,g]) {
  console.log(a, b, g);
}
printColor(colors)

const { 0:colour1,1:colour2,2:colour3,3:colour4,4:colour5,5:colour6 } = colors

function printColor1({ 0:colour1,1:colour2,2:colour3,3:colour4,4:colour5,5:colour6 } = colors) {
  console.log(Colour 1 is:${colour1} ,Colour 2 is:${colour2},Colour 3 is:${colour3},Colour 4 is:${colour4},Colour 5 is:${colour5},Colour 6 is:${colour6});
}

printColor1(colors)
```
# Swapping Variables:
```
let a = 1, b = 2;

[a, b] = [b, a];

console.log(a); // 2
console.log(b); // 1
```
