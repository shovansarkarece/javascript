# Static
- a) The static keyword is used to define a static method or property of a class.
- b) To call the static method we do not need to create an instance or object of the class.
- c) We create a static variable in JavaScript to prevent replication
- d) Fixed configuration, and it is also useful for caches
```
class Person {

    //Properties
    static first_name='Jhon'
    static last_name='Dee'

    //method
    static getName() {
        return (`The name of the person is ${this.first_name} ${this.last_name}`)
    }

}

console.log(Person.getName());
```
