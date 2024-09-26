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
