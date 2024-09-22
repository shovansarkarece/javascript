# Array
>JavaScript array is an object that represents a collection of similar type of elements
```
let App=["Android","IOS","Windows","Mac","Web"]
let city=["Dhaka","Rajshahi","Rangpur"]
let numbers=[1,40,50,40,3,2]
/////In js Array's index always start from 0
console.log(App)//-->Return whole array
console.log(App[0])//-->Aray's Index start from 0
console.log(App[1])//-->Aray's Index 1
console.log(city)//-->Return whole array
console.log(city[0])//-->Aray's Index start from 0 
console.log(city[1])//-->Aray's Index 1
console.log(numbers)//-->Return whole array
console.log(numbers[0])//-->Aray's Index start from 0 
console.log(numbers[1])//-->Aray's Index 1
```
![image](https://github.com/user-attachments/assets/05f415b2-07f8-4daa-9ab4-b65e0385f8f5)

# Loop Over Array
- For Each Loop
```
let App=["Android","IOS","Windows","Mac","Web"]
App.forEach((item)=>{
    console.log(item)
})
```
![image](https://github.com/user-attachments/assets/73d46218-074d-4f5d-8ec6-ad17b781f250)
# Loop Iteration 
```
let App=["Android","IOS","Windows","Mac","Web"]
for(i=0;i<App.length;i=i+1){
    console.log((i+1) +" "+App[i])
}
```
![image](https://github.com/user-attachments/assets/58e63cda-e26f-409e-a518-7a80bb789e76)
# Array Helping Methods
- JAVASCRIPT ARRAY CONCAT()
  >The JavaScript array concat() method combines two or more arrays and returns a new string.
```
let first=['a','b','c']
let second=['d','e','f']
let res=first.concat(second)
console.log(res)
```
![image](https://github.com/user-attachments/assets/4181e9ed-b680-41cb-bb2e-4eb1c3cd9cf2)
- JAVASCRIPT ARRAY FROM()
>The from() method creates a new array that holds the shallow copy from an array or iterable object.
>>When applied to a string, each word gets converted to an array element in the new array
```
let nameString="Independence is the right of human being"
let nameArray=Array.from(nameString)
console.log(nameArray)
```
![image](https://github.com/user-attachments/assets/4af5c769-ef60-4d5e-bdd7-b6248d584296)
- JAVASCRIPT ARRAY INCLUDES()
  >The JavaScript array includes() method checks whether the given array contains the specified element. It returns true if an array contains the element, otherwise false.
```
let ostadApp=["Android","IOS","Windows","Mac","Web"]
let res=ostadApp.includes("Apple");
let res1=ostadApp.includes("WEB");
let res2=ostadApp.includes("WeB");
let res3=ostadApp.includes("Web");
console.log(res)
console.log(res1)
console.log(res2)
console.log(res3)
```
![image](https://github.com/user-attachments/assets/632ee5c5-5f11-4999-9134-cdcec1de9527)

- JAVASCRIPT ARRAY INDEXOF()
>The JavaScript array indexOf() method is used to search the position of a particular element in a given array. 
>>This method is case-sensitive.
```
let App=["Android","IOS","Windows","Mac","Web"]
let res=App.pop()
console.log(res)
let App=["Android","IOS","Windows","Mac","Web"]
let res=App.indexOf("Web")
console.log(res)
////Output:4
```
- JAVASCRIPT ARRAY POP()
  >The JavaScript array pop() method removes the last element from the given array and return that element.
```
let App=["Android","IOS","Windows","Mac","Web"]
let res=App.pop()
console.log(res)
////Output:Web
```
