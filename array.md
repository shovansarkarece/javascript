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
- **JAVASCRIPT ARRAY FILTER()**
>The JavaScript array filter() method filter and extract the element of an array that satisfying the provided condition.
```
let marks=[20,37,40,45,50,30,10,5]
function check(value){
    return value>30;
}
console.log(marks.filter(check));
```
![image](https://github.com/user-attachments/assets/a53ce305-e1f1-4c94-a53e-e258230ae00a)
- **JAVASCRIPT ARRAY FIND()**
>The JavaScript array find() method returns the first element of the given array that satisfies the provided function condition.
- **Example-1**
```
let ar=[5,22,19,25,34]
let res=ar.find(x=>x>20);
console.log(res);
////Output:22(Always first element will return)
```
- **Example-2**
```
let ar1=[5,25,19,22,34]
let res1=ar1.find(x=>x>20);
console.log(res1);
////Output:25(Always first element will return)
```

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
- JAVASCRIPT ARRAY  PUSH()
  >The JavaScript array push() method adds one or more elements to the end of the given array.
```
let ostadApp=["Android","IOS","Windows","Mac","Web"]
let res=ostadApp.push("Apple")
console.log(ostadApp)
```
![image](https://github.com/user-attachments/assets/0ca87219-e9e1-424d-b444-cbe2ae134b48)

- JAVASCRIPT ARRAY REVERSE()
>The JavaScript array reverse() method changes the sequence of elements of the given array and returns the reverse sequence.
```
let App=["Android","IOS","Windows","Mac","Web"]
App.reverse();
console.log(App)
```
![image](https://github.com/user-attachments/assets/88bf640c-e7d7-4939-bcaa-75e42d2a5cdd)

- JAVASCRIPT ARRAY SLICE()
  >The JavaScript array slice() method extracts the part of the given array and returns it.
  >>This method doesn't change the original array

```
let ostadApp=["Android","IOS","Windows","Mac","Web"]
let res=ostadApp.slice(1,3); //// 1,2-->(n-1)-->(3-1)-->2
let res1=ostadApp.slice(1,4); //// 1,2,3-->(n-1)-->(4-1)-->3
let res2=ostadApp.slice(1,5); //// 1,2,3,4-->(n-1)-->(5-1)-->4
console.log(res);
console.log(res1);
console.log(res2);
```
![image](https://github.com/user-attachments/assets/9b67b325-ad30-46a2-876c-5280aa882205)
- JAVASCRIPT ARRAY SORT()
>The JavaScript array sort() method is used to arrange the array elements in some order.
>>By default, sort() method follows the ascending order.
```
let numbers=[30,55,44,20,77];
numbers.sort()////-->By default, sort() method follows the ascending order.
numbers.reverse()////-->But if we want to get the array in descending order then reverse it 
console.log(numbers);
```
![image](https://github.com/user-attachments/assets/05c1d3db-ea80-41e3-a86e-f5315e9d1f63)
# JAVASCRIPT ARRAY SPLICE()
>The JavaScript array splice() method is used to add/remove the elements to/from the existing array. 
>>It returns the removed elements from an array.
>>>*****The splice() method also modifies the original array.*****
- **Syntax:array.splice(index,removecount,item)**
```
let arr =["A","B","C","D","E"]
//////Example of Splice in terms of deletion
let res=arr.splice(2,2,"P","Q")////==>It means we can select from index 2 
////and susbstitute 2 elemenet at the place of C,D with P,Q
console.log(res);
console.log(arr);
```
![image](https://github.com/user-attachments/assets/9b3708eb-2d85-4afd-9f86-f9bf93640fa7)

#### Another Example of Splice in terms of deletion
```
let arr1 =["A","B","C","D","E"]
//////Example of Splice in terms of deletion
let res2=arr1.splice(2,2,)////==>It means we can select from index 2 
////and delete 2 elements from index 2
console.log(res2);
console.log(arr1);//////As we know splice() method, will change our main array.
```
![image](https://github.com/user-attachments/assets/da014796-5293-48df-8ff9-b566746f4d83)

