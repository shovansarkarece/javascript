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
