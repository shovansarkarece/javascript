# Class
## Classes are blueprints of an Object
- a) A class can have many Objects because
- b) Class is a template while Objects are instances of the class
- c) Using let or var to declare variables inside a class is unnecessary because class
     properties are automatically scoped to the class instance and don't require explicit variable declarations.
```
class Person {

    //Properties
    first_name='Jhon'
    last_name='Dee'

    //method
    getName() {
        return (`The name of the person is ${this.first_name} ${this.last_name}`)
    }
}

const person1 = new Person();
console.log(person1.getName());
```
