# Constructor
## Classes constructor is a magic method
- a) Constructor execute automatically when object is created
- b) Constructor can take parameter
- c) Constructor method can't return any result
# Example-1(Default Constructor)
### Constructor inside only parent class
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
## Constructor inside only parent class pass parameters
```
class Father{
    constructor(msg){
    console.log(msg)
}
}
class Son extends Father{    
}
new Father("This is constructor parameter from Father")
new Son("This is constructor parameter from Son")
```
# Example-4(Parameterized Constructor)
```
class MyClass{
        constructor(a,b){
            console.log(a+b)
}
}
const myclass=new MyClass(50,50)
```
# Example-5
## Constructor inside only child class(super() method required)
```
class Father{
}
class Son extends Father{    
        constructor(){
        super();
        console.log("I am constructor of Son Class")
}
}
new Son()
```
# Example-6
## Constructor inside only child class pass parameter
```
class Father{
}
class Son extends Father{    
        constructor(msg){
        super();
        console.log(msg)
}
}
new Son("This is constructor parameter from Son")
```
# Example-7
## Constructor inside both parent and child class 
> IF both have constructor then according to call of class constructor will be called
>> But in this case,if the child constructor called then only child able to call both the parent class and it's own class using super() method
>>> Finally as per the rule, the parent is unable to access child class which is the principle of oops methodology.
```
class Father{
    constructor(){
    console.log("I am Father Constructor")
}
}
class Son extends Father{    
        constructor(){
        super();
        console.log("I am a Son constructor")
}
}
new Son()
new Father()
```
# Example-7
## Constructor inside both parent and child classes both are passing parameter
```
class Father{
    constructor(msg_parent){
    console.log("I am Father Constructor")
}
}
class Son extends Father{    
        constructor(msg_child){
        super();
        console.log("I am a Son constructor")
}
}
new Son("This is constructor parameter from Son")
new Father("This is constructor parameter from Father")
```
# Example-8
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
