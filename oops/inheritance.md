# Inheritance
- a) Keyword "extends" is used to create inherit relationship between class
- b) For inherit relationship child class can use parent class properties
# Example-1
```
class Father{
    x=10
    y=20
    addTwo(){
        let sum=this.x+this.y;
        console.log(sum);
    }
}



class Son extends Father{

    // বাবার কাছে আছে মানে ছেলের কাছেও আছে

}
let son=new Son()
console.log(son.x)
console.log(son.y)
son.addTwo()


let father=new Father()
console.log(father.x)
console.log(father.y)
father.addTwo()
```
# Example-2
```
class Father {

    //Properties
     first_name='Jhon'
     last_name='Dee'
    //method
     getName() {
        return (`The name of the person is ${this.first_name} ${this.last_name}`)
    }
}
class Son extends Father{
}

const SonObj = new Son();
console.log(SonObj.getName());
```
# Example-3(Inheritance with super() keyword)
```
class Father{
    constructor(){
        console.log("Father constructor");
    }
}
class Son extends Father{
    constructor(){
        super() // Permission
        console.log("Son constructor");
    }
}
let father=new Father();
```
# Example-4(Inheritance with static keyword)
```
class Father{
    static addTwo(){
        let num1=10
        let num2=20
        let sum=num1+num2
        console.log(sum)
    }
}
class Son extends Father{
}
Son.addTwo();
Father.addTwo();
```
# Example-5(Inheritance with static keyword)
```
class Father{
    static greetParent(){
        return "Hello, I am the Father"
    }
}
class Son extends Father{
        static greetchild(){
        return "Hello, I am the Son"
    }
}
console.log(Son.greetParent());
console.log(Son.greetchild());
console.log(Father.greetParent());
```
