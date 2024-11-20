![image](https://github.com/user-attachments/assets/fafde96e-f866-4451-98b7-53a932bb0d2d)

## 1.setTimeout:
- **The setTimeout function is used to execute a function or code block after a specified delay in milliseconds.**
![image](https://github.com/user-attachments/assets/cef19315-cec8-4d3f-bd51-88461cacd7f2)
```
function delayedFunction(x) {
  console.log("This function was delayed by 2000 milliseconds (2 seconds).", x);
}
setTimeout(delayedFunction, 2000);
setTimeout(() => delayedFunction(5), 2000);
```
### Output:
![image](https://github.com/user-attachments/assets/a8077eb4-3de1-4ab5-85fe-2f562129ad05)

## 2. setInterval:
- **The setInterval function is used to repeatedly execute a function or code block at a specified interval in milliseconds.**

![image](https://github.com/user-attachments/assets/debc246f-cc56-4ed9-880a-a034ec56659d)

- **Example- mind game of counting seconds on mind and after every 5secs we need to draw a straight line on paper and it will continue till I told you to stop.**
```
// function repeatedFunction() {
//   console.log(
//     "This function will be repeated every 1000 milliseconds (1 second)."
//   );
// }
// setInterval(repeatedFunction, 1000);
```
### Output:
![image](https://github.com/user-attachments/assets/d734547d-e115-44af-acdf-bd62b01b212b)


