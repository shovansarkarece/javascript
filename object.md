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
![image](https://github.com/user-attachments/assets/405d6421-8635-4523-bda9-3e15781f21ac)

//* In this example, the greet method is defined using the "Method Shorthand" syntax. It's a more concise way to define methods in object literals.
// const obj = {
//   name: "Kodyfier",
//   greet() {
//     console.log(this);
//   },
// };

// obj.greet();

//* Fat Arrow Function
// const obj = {
//   name: "thapa technical",
//   greet: () => {
//     console.log(this);
//   },
// };

// obj.greet();
