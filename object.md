![image](https://github.com/user-attachments/assets/0d50e463-70ba-41cc-818c-8e9f84100603)

```
let person={
    name:"Suva Sarkar",
    age:34,
    city:"Chattogram",
    isBangladeshi:true
}
console.log(person.name)
console.log(person.age)
console.log(person.city)
console.log(person.isBangladeshi)
```
![image](https://github.com/user-attachments/assets/c4e8d091-e73e-487d-bf4e-1afd41b40705)
# Object 
- **Objects are a fundamental part of JavaScript, providing a way to group related data and functions together.**
- **In JavaScript, an object is a collection of key-value pairs, where each key is a string (or a symbol) and each value can be any data type, including other objects.**
- **Objects can have properties and methods, making them versatile for various use cases.**
### Creating Objects:
- **There are several ways to create objects in JavaScript. The most common one is using object literals:**
```
// const product = {
//   id: 1,
//   pName: "laptop",
// };

// let person = {
//   name: "Vinod",
//   age: 30,
//   isStudent: false,
//   greet: function () {
//     console.log("Welcome to World Best CSS Course");
//   },
// };

let person = {
  name: "Vinod",
  age: 30,
  "is'Student": false,
  greet: function () {
    console.log("Welcome to World Best JavaScript Course");
  },
};
```
### Accessing Properties:
- **We can access object properties using dot notation or square bracket notation:**
```
let person = {
  name: "Vinod",
  age: 30,
  "is'Student": false,
  greet: function () {
    console.log("Welcome to World Best JavaScript Course");
  },
};
// console.log(person.age);
// console.log(person.name);
// console.log(person[`is'Student`]);
```
let person = {
  name: "Vinod",
  age: 30,
  "is'Student": false,
  greet: function () {
    console.log("Welcome to World Best JavaScript Course");
  },
};
### Adding and Modifying Properties:
- **We can add new properties or modify existing ones:**
```
let person = {
  name: "Vinod",
  age: 30,
  "is'Student": false,
  greet: function () {
    console.log("Welcome to World Best JavaScript Course");
  },
};
// person["job"] = "web dev";
// person.age = 18;
// person["age"] = 20;
// console.log(person);
```
### Output:
```
{
  name: 'Vinod',
  age: 20,
  "is'Student": false,
  greet: [Function: greet],
  job: 'web dev'
}
false
```
### Accessing Methods:
- **Methods in objects are functions associated with the object. They can be invoked using the same notation as properties:**
```
let person = {
  name: "Vinod",
  age: 30,
  "is'Student": false,
  greet: function () {
    console.log("Welcome to World Best JavaScript Course");
  },
};
 person.greet();
```
### Output:
```
Welcome to World Best JavaScript Course
```
### We can add dynamic keys in an object
- **useCase: when we want to get the user name and value in react.**
```
// let idType = "studentId";

// let student = {
//   [idType]: "A123456", // Dynamic key based on idType
//   sName: "Vinod",
//   sAge: 29,
//   isStudent: true,
//   greet: function () {
//     console.log(
//       `Hey, my ${idType} is ${student[idType]} and my name is ${student.sName}.`
//     );
//   },
// };
// student.greet();
```
### Output:
```
Hey, my studentId is A123456 and my name is Vinod.
```
### Data Modeling:
- **Data modeling is the process of creating a visual representation of either a whole information system or parts of it to communicate connections between data points and structures.**
- **The goal is to illustrate the types of data used and stored within the system, the relationships among these data types, the ways the data can be grouped and organized and its formats and attributes.**
- **Objects are excellent for modeling real-world entities. For instance, you might represent a car, a user, or a product as an object with properties like color, brand, username, etc.**
```
// let car = {
//   brand: "Toyota",
//   model: "Camry",
//   year: 2022,
//   start: function () {
//     console.log("Engine started!");
//   },
// };
```
# Pass by value and Pass by reference
### Pass by value 
- **In JavaScript, primitive data types like numbers and strings are passed by value, while objects are passed by reference.**
- **Passing by value: When passing by value, a copy of the primitive value is created and passed to the function or assigned to a variable.Any changes made to the copy do not affect the original value.**
```
// let a = 10;
// const modifyValue = (x) => (x = 20);

// console.log(modifyValue(a));
// console.log(a);
```
### Passing by reference: 
- **When passing by reference, a reference to the memory location of the object is passed to the function or assigned to a variable.**
- **Any changes made to the object through this reference will affect the original object.**
```
// let obj = { id: 5, name: "kodyfier" };

// let obj1 = obj;

// obj1.name = "thapa technical";
// console.log(obj1);
// console.log("original", obj);
```
### Output:
```
{ id: 5, name: 'thapa technical' }
original { id: 5, name: 'thapa technical' }
```
- **To avoid this behavior and create a true copy of the object, you can use methods like Object.assign() or the spread operator (...):**
### Object.assign()
- **`Object.assign()` is used to copy properties from one or more source objects to a target object.**
```
// let obj = { id: 5, name: "kodyfier" };
// let obj1 = {};
// let newObj = Object.assign(obj1, obj);

// newObj.name = "thapa technical";
// console.log(newObj);
// console.log("original", obj);
```
### Comparison by Reference:
- **Two objects are equal only if they refer to the same object.**
- **Independent objects (even if they look alike) are not equal:**
```
const obj1 = { name: "vinod" };
const obj2 = { name: "vinod" };
const obj3 = obj1;

const isEqual = obj1 == obj2 ? true : false; =====>false
const isEqual = obj1 == obj3 ? true : false; =====>true
console.log(isEqual);
```
# JSON (JavaScript Object Notation):
- **JSON is a data interchange format derived from JavaScript objects. Objects can be easily converted to JSON and vice versa.**
```
// let student = {
//   id: 1,
//   sName: "Vinod",
//   sAge: 29,
//   isStudent: false,
//   greet: function () {
//     console.log(
//       `hey my id is ${student.identity} & my name is ${student.sName}`
//     );
//   },
// };

// let jsonData = JSON.stringify(student);
// console.log(jsonData); ====> {"id":1,"sName":"Vinod","sAge":29,"isStudent":false}

// let parsedObject = JSON.parse(jsonData);
// console.log(parsedObject); ====> { id: 1, sName: 'Vinod', sAge: 29, isStudent: false }
```
## "this" Object

![image](https://github.com/user-attachments/assets/1cd01e6a-2e65-4b73-b702-83a42f1c1877)

- **In JavaScript, the this keyword refers to an object.**
- **Which object depends on how this is being invoked (used or called).**
- **The this keyword refers to different objects depending on how it is used:**
- **In an object method, this refers to the object.**
- **Alone, this refers to the global object.**
- **In a function, this refers to the global object.**
- **In a function, in strict mode, this is undefined.**
- **In an event, this refers to the element that received the event.**
- **Methods like call(), apply(), and bind() can refer this to any object.**

// Note
// this is not a variable. It is a keyword. You cannot change the value of this
```
// function callme() {
//   console.log(this);====>Refer to window object
// }

// callme(); // try to run on browser console
```
### Regular Function Expression:
```
// const obj = {
//   name: "Kodyfier",
//   greet: function () {
//     console.log(this);
//   },
// };
// obj.greet();
```
### Output:
![image](https://github.com/user-attachments/assets/405d6421-8635-4523-bda9-3e15781f21ac)

- **In this example, the greet method is defined using the "Method Shorthand" syntax. It's a more concise way to define methods in object literals.**
```
// const obj = {
//   name: "Kodyfier",
//   greet() {
//     console.log(this);
//   },
// };
// obj.greet();
```
### Output:
![image](https://github.com/user-attachments/assets/56a188b8-e167-42ad-bdc4-3571f5c4a552)

### Fat Arrow Function
```
// const obj = {
//   name: "thapa technical",
//   greet: () => {
//     console.log(this);
//   },
// };

// obj.greet();
```
### Output:
![image](https://github.com/user-attachments/assets/49eef950-8431-4e0d-96eb-261a17a3eb20)

# Objects Useful Methods


## 1: Object.keys(): 
- **Returns an array containing the names of all enumerable own properties of an object.**
```
// const product = {
//   id: 1,
//   name: "Laptop",
//   category: "Computers",
//   brand: "ExampleBrand",
//   price: 999.99,
//   stock: 50,
//   description:
//     "Powerful laptop with a quad-core i5 processor, 8GB RAM, 256GB SSD, and a 14-inch FHD display.",
//   image: "image link will be added during projects",
// };
// let keys = Object.keys(product);
// console.log(keys);
```
## 2: Object.values(): 
- **Returns an array containing the values of all enumerable own properties of an object.**
```
// const product = {
//   id: 1,
//   name: "Laptop",
//   category: "Computers",
//   brand: "ExampleBrand",
//   price: 999.99,
//   stock: 50,
//   description:
//     "Powerful laptop with a quad-core i5 processor, 8GB RAM, 256GB SSD, and a 14-inch FHD display.",
//   image: "image link will be added during projects",
// };
// let values = Object.values(product);
// console.log(values);
```
## 3: Object.entries(): 
- **Returns an array containing arrays of key-value pairs for each enumerable own property of an object.**
```
// const product = {
//   id: 1,
//   name: "Laptop",
//   category: "Computers",
//   brand: "ExampleBrand",
//   price: 999.99,
//   stock: 50,
//   description:
//     "Powerful laptop with a quad-core i5 processor, 8GB RAM, 256GB SSD, and a 14-inch FHD display.",
//   image: "image link will be added during projects",
// };
// let entries = Object.entries(product);
// console.log(entries);
```
## 4: Object.hasOwnProperty():
- **Returns a boolean indicating whether the object has the specified property as an own property.**
```
// const product = {
//   id: 1,
//   name: "Laptop",
//   category: "Computers",
//   brand: "ExampleBrand",
//   price: 999.99,
//   stock: 50,
//   description:
//     "Powerful laptop with a quad-core i5 processor, 8GB RAM, 256GB SSD, and a 14-inch FHD display.",
//   image: "image link will be added during projects",
// };
// console.log(product.hasOwnProperty("name")); // Output: true
// console.log(product.hasOwnProperty("isStudent")); // Output: false
```
## 5: Object.assign(): 
- **Copies the values of all enumerable own properties from one or more source objects to a target object.**
```
// const product = {
//   id: 1,
//   name: "Laptop",
//   category: "Computers",
//   brand: "ExampleBrand",
//   price: 999.99,
//   stock: 50,
//   description:
//     "Powerful laptop with a quad-core i5 processor, 8GB RAM, 256GB SSD, and a 14-inch FHD display.",
//   image: "image link will be added during projects",
// };
// const target = { a: 1, b: 5 };
// const source = { b: 3, c: 4 };
// const mergedObject = Object.assign(target, source);
// console.log(mergedObject); // Output: { a: 1, b: 3, c: 4 }
```
## 6: Object.freeze(): 
- **Freezes an object, preventing new properties from being added to it and existing properties from being modified or deleted.**
```
// const product = {
//   id: 1,
//   name: "Laptop",
//   category: "Computers",
//   brand: "ExampleBrand",
//   price: 999.99,
//   stock: 50,
//   description:
//     "Powerful laptop with a quad-core i5 processor, 8GB RAM, 256GB SSD, and a 14-inch FHD display.",
//   image: "image link will be added during projects",
// };
// Object.freeze(product);
// product.id = "5656";
// console.log(product);
```
# Interview Question - Objects

### 1.What will be the output?
```
// const target = { a: 1, b: 2 };
// const source = { b: 3, c: 4 };

// const mergedObject = Object.assign({}, target, source);
// console.log(mergedObject);
```
### Outpt:
```
{ a: 1, b: 3, c: 4 }
```
# Interview Question - Object Manipulation:

- **Given an object representing a student, write a function to add a new subject with its corresponding grade to the student's record. Also check if the grades property is present or not?**
```
// let student = {
//   name: "Bob",
//   age: 20,
//   grades: {
//     math: 90,
//     science: 85,
//     history: 88,
//   },
// };

// const addSubjectGrade = (student, subject, marks) => {
//   if (!student.grades) {
//     student.grades = {};
//   }

//   return (student.grades[subject] = marks);
// };

// addSubjectGrade(student, "computer", 92);
// console.log(student);
```
# Interview Question - Object Comparison:

- **Problem: Write a function that compares two objects to determine if they have the same properties and values.**
```
// const areObjectsEqual = (obj1, obj2) => {
//   //   if (obj1.length != obj2.length) {
//   //     console.log("hi");
//   //     return false;
//   //   }
//   let o1 = Object.keys(obj1);
//   let o2 = Object.keys(obj2);

//   if (o1.length != o2.length) {
//     console.log("There keys are not same");
//     return false;
//   }

//   for (let key in obj1) {
//     if (obj1[key] !== obj2[key]) {
//       return false;
//     }
//   }

//   return true;
// };

// // Example usage:
// let objA = { name: "Alice", age: 26, city: "New York" };
// let objB = { name: "Alice", age: 26, city: "New York" };
// let objC = { name: "Bob", age: 30, city: "San Francisco" };

// console.log(areObjectsEqual(objA, objB)); // Should return true
// console.log(areObjectsEqual(objA, objC)); // Should return false
```
# Interview Question - Object Transformation:
- **Problem: Write a function that transforms an array of an objects into an object where the keys are the objects' ids.**
```
// let inputArray = [
//   { id: 1, name: "Alice" },
//   { id: 2, name: "Bob" },
//   { id: 3, name: "Charlie" },
// ];

// const arrayToObj = (arr) => {
//   //   console.log(arr[2].id);
//   let obj = {};
//   for (let key of arr) {
//     console.log(key.id, key);
//     obj[key.id] = key;
//     // console.log(key);
//   }
//   return obj;
// };

// console.log(arrayToObj(inputArray));
// Should print: { '1': { id: 1, name: 'Alice' }, '2': { id: 2, name: 'Bob' }, '3': { id: 3, name: 'Charlie' } }
```
#### Output:
```
1 { id: 1, name: 'Alice' }
2 { id: 2, name: 'Bob' }
3 { id: 3, name: 'Charlie' }
{
  '1': { id: 1, name: 'Alice' },
  '2': { id: 2, name: 'Bob' },
  '3': { id: 3, name: 'Charlie' }
}
```

