# Method Overloading
- a) Method overloading allows you to define multiple methods with the same name but different parameter lists
- b) JavaScript does not natively support method overloading
- c) Yet we can simulate method overloading by examining the number of arguments
```
getName(a) {
}
getName(a,b) {
}
```
# Example-2
```
class MyClass{
  myMethod(p1,p2,p3){
  if(arguments.length===1){
    console.log("Recieved one argument:",p1)
}
}
}

```
