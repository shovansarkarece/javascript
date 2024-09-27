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
# Change class properties value using constructor
```
class Person{
    num1=10;
    num2=20;
    constructor(a,b){
    this.num1=a;
    this.num2=b;
}
    addTwoNumber(){
    return this.num1+this.num2
}
}
let PersonObj=new Person();
console.log(PersonObj.addTwoNumber())
```
### Execution flow of constructor
![image](https://github.com/user-attachments/assets/d229b6ba-6e1c-451f-ad8d-c994d1d18aca)
![image](https://github.com/user-attachments/assets/fbafdb4c-1e46-4801-9ee7-ceacb1ce1351)
