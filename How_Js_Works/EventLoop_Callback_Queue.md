#### In JavaScript, the event loop is a fundamental mechanism that enables asynchronous programming, allowing JavaScript to handle tasks like running code, collecting and processing events, and executing queued sub-tasks.
![image](https://github.com/user-attachments/assets/fc2763c8-9089-425f-b646-d12d277f8d3a)
### Key Components of the Event Loop
### Call Stack:
- **This is where JavaScript keeps track of function calls. When a function is invoked, it’s added to the call stack. When the function completes, it’s removed from the stack.**
- **JavaScript is single-threaded, so only one task is executed at a time in the call stack.**
### Web APIs:
- **These are browser-provided APIs like setTimeout, DOM events, fetch, etc., which handle tasks asynchronously.**
- **When a function interacts with a Web API, like calling `setTimeout`, the Web API handles the task and waits for its completion.**
### Task Queue (Callback Queue):
- **This is where asynchronous tasks (e.g., setTimeout callbacks, fetch responses) are queued after the Web API completes its job.**
- **The event loop checks this queue and moves tasks to the call stack when it's empty.**
### Microtask Queue:
- **This is a special, high-priority queue for microtasks like Promise callbacks and MutationObserver.**
- **Microtasks are executed before tasks in the task queue.**
## How the Event Loop Works
- **The JavaScript runtime starts by executing code on the call stack.**
- **When asynchronous operations (like setTimeout, fetch) are encountered, they're handed off to Web APIs.**
- **Once the Web API finishes its work, the callback associated with the asynchronous task is placed in the task queue or microtask queue.**
### The event loop continuously monitors the call stack:
- **If the call stack is empty, it checks the microtask queue and executes all the microtasks.**
- **After all microtasks are handled, it processes the next task in the task queue.**
### Visualizing the Event Loop
```
console.log("Start");

setTimeout(() => {
  console.log("Timeout");
}, 0);

Promise.resolve().then(() => {
  console.log("Promise");
});

console.log("End");
```
#### Output:
```
sql
Copy code
Start
End
Promise
Timeout
```
### Explanation
- **console.log("Start") and console.log("End") run first as they are in the call stack.setTimeout is sent to the Web API, and its callback is queued in the task queue.**
- **Promise.resolve() adds its callback to the microtask queue.The microtask queue is processed before the task queue, so "Promise" is logged before "Timeout".**
### Summary
- **Call Stack: Executes functions sequentially.**
- **Microtask Queue: Executes promises and other microtasks before tasks in the task queue.**
- **Task Queue: Executes callbacks from Web APIs (e.g., setTimeout).**
- **The Event Loop ensures that tasks and microtasks are executed in the correct order, maintaining JavaScript’s non-blocking nature.**
## Another Example
```
console.log('Start script...');
setTimeout(() => {
    task('Download a file.');
}, 1000);
console.log('Done!');
```
- **In our example, when calling the setTimeout() function, the JavaScript engine places it on the call stack, and the Web API creates a timer that expires in 1 second.**
![image](https://github.com/user-attachments/assets/09426d6c-4f4d-49c3-ab7f-6e55bca82d68)

![image](https://github.com/user-attachments/assets/0872bf1a-9473-4a5d-a5a9-ed425884a809)

- **The event loop is a constantly running process that monitors both the callback queue and the call stack.**
- **If the call stack is not empty, the event loop waits until it is empty and places the next function from the callback queue to the call stack. If the callback queue is empty, nothing will happen:**

![image](https://github.com/user-attachments/assets/c0ce38cd-9bc6-4af2-ab4e-24115abca9da)
