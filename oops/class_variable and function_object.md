# Class Variable and Function Object
```
class Person={
  first_name:"Suva"
  last_name:"Sarkar"
  age:100
  isBangladesh:true
  getName:()=>{
    return `My First name is ${person.first_name} ${person.last_name}`
}
}
let Person= new Person();
console.log(Person.first_name)
console.log(Person.age)
```
# Redeclairing Class with same class name by using class expression
## creating class using class expression
- A class can be declared once only. If we try to declare class more than one time it throws an error.
```
let Person=class {
  first_name:"Suva"
  last_name:"Sarkar"
  age:100
  isBangladesh:true
  getName:()=>{
    return `My First name is ${person.first_name} ${person.last_name}`
}
}
let Person= new Person();
console.log(Person.first_name)
console.log(Person.age)
```
### Example-2(Impossible)
```
let Person=class {
  first_name:"Suva"
  last_name:"Sarkar"
  age:100
  isBangladesh:true
  getName:()=>{
    return `My First name is ${person.first_name} ${person.last_name}`
}
}
let Person= new Person();
console.log(Person.first_name)
console.log(Person.age)
```
