![image](https://github.com/user-attachments/assets/fafde96e-f866-4451-98b7-53a932bb0d2d)

## 1.setTimeout:
- **The setTimeout function is used to execute a function or code block after a specified delay in milliseconds.**
- **setTimeout() is a method in JavaScript that allows you to execute a function or piece of code after a specified delay. It is often used for scheduling tasks or delaying actions.**
- **syntax:`setTimeout(function, delay, param1, param2, ...)`**
#### Parameters:
- **`function`: The function you want to execute after the delay.**
- **`delay`: The time to wait before executing the function, in milliseconds.**
- **`param1, param2, ... (optional)`: Arguments that will be passed to the function when it's executed.**
![image](https://github.com/user-attachments/assets/cef19315-cec8-4d3f-bd51-88461cacd7f2)
```
///// Example-1
function delayedFunction(x) {
  console.log("This function was delayed by 2000 milliseconds (2 seconds).", x);
}
setTimeout(delayedFunction, 2000);
setTimeout(() => delayedFunction(5), 2000);
///// Example-2
setTimeout(() => {
    console.log("Hello after 2 seconds!");
}, 2000);
This will print "Hello after 2 seconds!" to the console after a 2-second delay.
////// Example-3
function greet(name) {
    console.log(`Hello, ${name}!`);
}
setTimeout(greet, 3000, "Alice");
This will print "Hello, Alice!" to the console after 3 seconds.
```
### Output:
![image](https://github.com/user-attachments/assets/a8077eb4-3de1-4ab5-85fe-2f562129ad05)

## 2. setInterval:
- **The setInterval function is used to repeatedly execute a function or code block at a specified interval in milliseconds.**
- **Syntax:`setInterval(repeatedFunction, 1000)`**

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
## 3.clearTimeout(timeoutID);Canceling a setTimeout():
- **Canceling a setTimeout():.You can cancel a scheduled setTimeout() by using clearTimeout().**
- **If you want to cancel a scheduled timeout before it occurs, you can use the clearTimeout function.**
- **The global clearTimeout() method cancels a timeout previously established by calling setTimeout().Cancel the timeout before it occurs**
- **setTimeout() is asynchronous, meaning it doesn't block the execution of subsequent code.**
- **It returns a unique timeout ID, which is used to cancel the timeout if needed.**
- **If you need a function to run repeatedly, consider using setInterval() instead.**
- **Syntax:`clearTimeout(timeoutID)`**
```
//////Exmple-1
function delayedFunction() {
  console.log("This function was delayed by 2000 milliseconds (2 seconds).");
}
const myWork = setTimeout(delayedFunction, 2000);
clearTimeout(myWork);
//////Exmple-2
const timeoutId = setTimeout(() => {
    console.log("This will not run.");
}, 5000);
clearTimeout(timeoutId);
/////In this example, the clearTimeout(timeoutId) prevents the scheduled function from executing.
```
## 4.Clearing Interval with clearInterval:
- **If you want to cancel a scheduled interval before it occurs, you can use the clearInterval function.**
- **The global clearInterval() method cancels a timeout previously established by calling setInterval().**
- **Syntax:`clearInterval(intervalID)`
```
// function repeatedFunction() {
//   console.log("This function repeats every 1000 milliseconds (1 second).");
// }

// const intervalID = setInterval(repeatedFunction, 1000);

// clearInterval(intervalID)
```
## Interview Question
>Write a JavaScript program that defines a function called repeatedFunction.This function should log the message "This function repeats every 1000 milliseconds (1 second)" to the console. Then, set up an interval >>using setInterval() to call repeatedFunction every 1000 milliseconds.  Additionally, after 5 seconds have elapsed, use setTimeout() to clear the interval previously set up. Make sure to log the message >>>"Interval cleared after 5 seconds." when the interval is cleared.
```
const repeatedFunction = () => {
  console.log("This function repeats every 1000 milliseconds (1 second)");
};

repeatedFunction();

const intervalID = setInterval(repeatedFunction, 1000);

setTimeout(() => {
  clearInterval(intervalID);
}, 5000);
```
### Output:
![image](https://github.com/user-attachments/assets/f3ebb826-42ce-40eb-9f23-cefb857e0a0e)

