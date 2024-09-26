# Object
- In JavaScript we can create object using
- **By object literal**
- **By creating instance of object**
- **By using an object constructor**
## Object creation by object Literal
```
let person={
  first_name:"Suva",
  last_name:"Sarkar",
  age:100,
  isBangladesh:true,
  getName:()=>{
    return `My First name is ${person.first_name} ${person.last_name}`
}
}
console.log(person.age)
```
# Creating instance of an Object
```
//let person = new Object();
let person = Object();
person.first_name:"Suva"
person.last_name:"Sarkar"
person.age:100
person.isBangladesh:true
person.getName:()=>{
    return `My First name is ${person.first_name} ${person.last_name}`
}
console.log(person.getName());
console.log(person.age)
```
# Object creation by using object constructor
```
function person(){
this.first_name="Suva"
this.last_name="Sarkar"
this.age=34,
this.city="Chattogram"
this.isBangladesh=true
this.getName:()=>{
    return `My First name is ${this.first_name} ${this.last_name}`
}
}
let PersonInstance=new Person();
console.log(PersonInstance.getName())
```
