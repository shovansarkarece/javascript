# Constructor
## Classes constructor is a magic method
- a) Constructor execute automatically when object is created
- b) Constructor can take parameter
- c) Constructor method can't return any result
# Example-1(Default Constructor)
```
class Person {
    constructor() {
        console.log('I am a constructor')
    }
}
const person1 = new Person();
```
# Example-2(Parameterized Constructor)
```
class Person {
    constructor(msg) {
        console.log(msg)
    }
}
const person1 = new Person('I am a constructor');
```
# Example-3(Parameterized Constructor)
```
class MyClass{
        constructor(a,b){
            console.log(a+b)
}
}
const myclass=new MyClass(50,50)
```
