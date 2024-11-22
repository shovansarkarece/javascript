# Event Propagation: 
- **Event propagation refers to the process of how events propagate or travel through the DOM (Document Object Model) hierarchy.** 
- **In JavaScript, there are two phases of event  propagation: capturing phase and bubbling phase.**
- **Understanding event propagation is crucial for managing and handling events in complex web applications.** 
# Phases of Event Propagation: 
## Capturing Phase:
- **The event starts from the root of the DOM and goes down to the target element.**
- **Handlers registered for the capturing phase are executed.**
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Event Propagation Example</title>
    <link rel="stylesheet" href="style.css" />
    <style>
      body {
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
      }
      section {
        width: 72rem;
        display: flex;
        justify-content: center;
        align-items: center;
      }
      div {
        padding: 6rem 10rem;
        border: 3px solid #1f2544;
        cursor: pointer;
        font-size: 2rem;
        text-transform: uppercase;
        background-color: #c7c8cc;
        color: #1f2544;
        box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px,
          rgb(51, 51, 51) 0px 0px 0px 3px;
      }

      #inner:hover {
        background-color: #d6417a;
        color: #000;
        z-index: 3;
        position: relative;
      }

      #middle:hover {
        background-color: #9f70fd;
        color: #000;
        z-index: 2;
        position: relative;
      }

      #outer:hover {
        background-color: #9bcf53;
        color: #000;
        position: relative;
        z-index: 1;
      }
    </style>
  </head>
  <body>
    <section>
      <div id="outer">
        Outer
        <div id="middle">
          Middle
          <div id="inner">Inner</div>
        </div>
      </div>
    </section>
    <script>
      const callOuter = (event) => {
        console.table([
          {
            Description: "I am the outer one",
            Target: event.target,
            CurrentTarget: event.currentTarget,
          },
        ]);
      };

      const callMiddle = () => {
        console.table([
          {
            Description: "I am the Middle one",
            Target: event.target,
            CurrentTarget: event.currentTarget,
          },
        ]);
      };

      const callInner = (event) => {
        console.table([
          {
            Description: "I am the Inner one",
            Target: event.target,
            CurrentTarget: event.currentTarget,
          },
        ]);
      };
      // To achieve event capturing, you can use the third parameter of the addEventListener method, which specifies whether the event should be captured during the capturing phase. Setting it to true will activate the capturing phase.
      document
        .getElementById("outer")
        .addEventListener("click", callOuter,true);
      document
        .getElementById("inner")
        .addEventListener("click", callInner,true);
      document
        .getElementById("middle")
        .addEventListener("click", callMiddle,true);
    </script>
  </body>
</html>

```
### Output:
![image](https://github.com/user-attachments/assets/e13fc207-ec7f-4ef8-b61f-de316ae4cc99)


## Target Phase:
- **The event reaches the target element.**
- **The handler registered for the target phase is executed.**

## Bubbling Phase:
- **The event starts from the target element and bubbles up to the root of the DOM.**
- **Handlers registered for the bubbling phase are executed.**
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Event Propagation Example</title>
    <link rel="stylesheet" href="style.css" />
    <style>
      body {
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
      }
      section {
        width: 72rem;
        display: flex;
        justify-content: center;
        align-items: center;
      }
      div {
        padding: 6rem 10rem;
        border: 3px solid #1f2544;
        cursor: pointer;
        font-size: 2rem;
        text-transform: uppercase;
        background-color: #c7c8cc;
        color: #1f2544;
        box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px,
          rgb(51, 51, 51) 0px 0px 0px 3px;
      }

      #inner:hover {
        background-color: #d6417a;
        color: #000;
        z-index: 3;
        position: relative;
      }

      #middle:hover {
        background-color: #9f70fd;
        color: #000;
        z-index: 2;
        position: relative;
      }

      #outer:hover {
        background-color: #9bcf53;
        color: #000;
        position: relative;
        z-index: 1;
      }
    </style>
  </head>
  <body>
    <section>
      <div id="outer">
        Outer
        <div id="middle">
          Middle
          <div id="inner">Inner</div>
        </div>
      </div>
    </section>
    <script>
      const callOuter = (event) => {
        console.table([
          {
            Description: "I am the outer one",
            Target: event.target,
            CurrentTarget: event.currentTarget,
          },
        ]);
      };

      const callMiddle = () => {
        console.table([
          {
            Description: "I am the Middle one",
            Target: event.target,
            CurrentTarget: event.currentTarget,
          },
        ]);
      };

      const callInner = (event) => {
        console.table([
          {
            Description: "I am the Inner one",
            Target: event.target,
            CurrentTarget: event.currentTarget,
          },
        ]);
      };
      //   By default is the bubbling phase
      document.getElementById("outer").addEventListener("click", callOuter);
      document.getElementById("middle").addEventListener("click", callMiddle);
      document.getElementById("inner").addEventListener("click", callInner);
    </script>
  </body>
</html>
```
### Output:

![image](https://github.com/user-attachments/assets/592eaee8-0973-48e6-9e4d-5a366775bbe6)

# `event.stopPropagation()`:
- **The stopPropagation() method of the Event interface prevents further propagation of the current event in the capturing and bubbling phases.**
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Event Propagation Example</title>
    <link rel="stylesheet" href="style.css" />
    <style>
      body {
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
      }
      section {
        width: 72rem;
        display: flex;
        justify-content: center;
        align-items: center;
      }
      div {
        padding: 6rem 10rem;
        border: 3px solid #1f2544;
        cursor: pointer;
        font-size: 2rem;
        text-transform: uppercase;
        background-color: #c7c8cc;
        color: #1f2544;
        box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px,
          rgb(51, 51, 51) 0px 0px 0px 3px;
      }
      #inner:hover {
        background-color: #d6417a;
        color: #000;
        z-index: 3;
        position: relative;
      }
      #middle:hover {
        background-color: #9f70fd;
        color: #000;
        z-index: 2;
        position: relative;
      }
      #outer:hover {
        background-color: #9bcf53;
        color: #000;
        position: relative;
        z-index: 1;
      }
    </style>
  </head>
  <body>
    <section>
      <div id="outer">
        Outer
        <div id="middle">
          Middle
          <div id="inner">Inner</div>
        </div>
      </div>
    </section>
    <script>
      const callOuter = (event) => {
        console.table([
          {
            Description: "I am the outer one",
            Target: event.target,
            CurrentTarget: event.currentTarget,
          },
        ]);
      };
      const callMiddle = () => {
        console.table([
          {
            Description: "I am the Middle one",
            Target: event.target,
            CurrentTarget: event.currentTarget,
          },
        ]);
      };
      const callInner = (event) => {
        console.table([
          {
            Description: "I am the Inner one",
            Target: event.target,
            CurrentTarget: event.currentTarget,
          },
        ]);
         event.stopPropagation();
      };
      //   By default is the bubbling phase
      document.getElementById("outer").addEventListener("click", callOuter);
      document.getElementById("middle").addEventListener("click", callMiddle);
      document.getElementById("inner").addEventListener("click", callInner);
    </script>
  </body>
</html>
```
### Output:
![image](https://github.com/user-attachments/assets/474c0bcd-4134-411c-b770-5664b3b418ad)
# Event Delegation: 
- **একাধিক এলিমেন্টের জন্য একটাই ইভেন্ট লিসেনার রাখা এবং নতুন এলিমেন্ট যোগ করলেও যেন লিসেনার কাজ করে।**
- **Event delegation is a concept in JavaScript where instead of attaching event listeners to individual elements, you attach a single event listener to a common ancestor of those elements.**
- **This is particularly useful when you have a large number of similar elements and want to reduce the number of event listeners, improve performance, and simplify code.**
## Example: List with Delegation -->
- **Consider a scenario where you have an unordered list (<ul>) with multiple list items (<li>), and you want to handle click events on each list item.Instead of adding a separate event listener to each list item, you can use event delegation.**
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Event Delegation Example</title>
    <link rel="stylesheet" href="style.css" />
    <style>
      body {
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-family: Arial, sans-serif;
      }

      #myList {
        list-style: none;
        padding: 0;
      }

      #myList li {
        padding: 10px;
        border: 1px solid #ccc;
        margin: 5px;
        cursor: pointer;
        transition: transform 0.3s ease-in-out;
      }

      #myList li:hover {
        transform: scale(1.1);
        background-color: #f0f0f0;
        color: #333;
      }

      #listValue {
        margin-top: 20px;
        font-size: 20px;
        color: #f5ee62;
      }
    </style>
  </head>
  <body>
    <p>Which programming Language you like the most?</p>
    <br />
    <ul id="myList">
      <li>🎉 JavaScript 🎉</li>
      <li>🎈 React 🎈</li>
      <li>🎊 Next 🎊</li>
      <li>🎁 HTML/CSS 🎁</li>
    </ul>
    <p id="listValue"></p>

    <script>
      const getListDetails = (event) => {
        const listItem = event.target;
        listItem.style.transform = "rotateY(360deg)"; // Add a rotation animation
        setTimeout(() => {
          listItem.style.transform = "rotateY(0deg)"; // Reset rotation after a delay
        }, 500);

        document.getElementById(
          "listValue"
        ).innerText = `You fav programming language is: ${listItem.innerText}`;
      };
      document
        .getElementById("myList")
        .addEventListener("click", getListDetails);
    </script>
  </body>
</html>
```
# Another Example of Event Delegation
```
/////Index.html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Event Delegation</title>
        <link rel="preconnect" href="https://fonts.googleapis.com" />
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
        <link
            href="https://fonts.googleapis.com/css2?family=Anek+Bangla:wght@400;600&display=swap"
            rel="stylesheet"
        />
        <link rel="stylesheet" href="./style.css" />
    </head>
    <body>
        <div class="container">
            <h1>ইভেন্ট ডেলিগেশন কি?</h1>

            <p>
                একাধিক এলিমেন্টের জন্য
                <span class="highlight">একটাই ইভেন্ট লিসেনার রাখা</span> এবং
                <span class="highlight">নতুন এলিমেন্ট</span> যোগ করলেও যেন
                লিসেনার কাজ করে।
            </p>

            <div class="languages">
                <ul id="list">
                    <li>জাভাস্ক্রিপ্ট</li>
                    <li>পিএইচপি</li>
                    <li>জাভা</li>
                    <li>পাইথন</li>
                    <li>টাইপস্ক্রিপ্ট</li>
                </ul>

                <div>
                    <button onclick="addElement()">
                        নতুন এলিমেন্ট যোগ করুন
                    </button>
                </div>
            </div>
        </div>

        <script src="./script.js"></script>
    </body>
</html>
///////style.css
* {
    font-family: "Anek Bangla", sans-serif;
}

.container {
    margin: 50px;
}

.languages {
    margin-top: 50px;
}

.highlight {
    background-color: aquamarine;
}

h1 {
    border-bottom: 1px solid gray;
}

ul {
    list-style-type: square;
}

li {
    margin-bottom: 10px;
}
/////script.js
const list = document.getElementById("list");

list.addEventListener("click", (e) => {
    if (e.target.matches("li")) {
        if (e.target.innerText === "জাভাস্ক্রিপ্ট") {
            e.target.style.backgroundColor = "yellow";
        } else {
            e.target.style.backgroundColor = "blue";
        }
    }
});

function addElement() {
    const newElement = document.createElement("li");
    newElement.textContent = "ডট নেট";
    list.appendChild(newElement);
}
```
