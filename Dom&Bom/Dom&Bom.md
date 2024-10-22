# WIndow and Document
![image](https://github.com/user-attachments/assets/484e95df-c865-4f2e-99d3-9d15ef81b743)
# Window Global Object, Dom and Bom.
![image](https://github.com/user-attachments/assets/504febd4-1e06-4b68-854f-5ce76d2cc904)
# Bom and Dom
![image](https://github.com/user-attachments/assets/d65ce41b-ca84-447d-a2ee-8bb8b83b2742)

![image](https://github.com/user-attachments/assets/514ac0fd-295f-4a3c-968b-f4fcc16c14b4)

![image](https://github.com/user-attachments/assets/a2186138-534a-48d3-a0d1-32869a9d5cb5)
![image](https://github.com/user-attachments/assets/5530d92d-1393-4469-b60f-59c8c7289232)

![image](https://github.com/user-attachments/assets/155d7fee-2f69-480a-8b7f-0e75ac83573b)

![image](https://github.com/user-attachments/assets/f6314466-6bd6-4a43-9c69-777148bdd713)
![image](https://github.com/user-attachments/assets/57df4f04-6aa7-436c-8d7d-655e7ef8ed4c)
![image](https://github.com/user-attachments/assets/fac4fc14-114d-4ce4-9cd5-099482afea84)
![image](https://github.com/user-attachments/assets/066c3e99-8212-4957-8b72-b8dd19c8383e)
# window.any_property==anyproperty
- **It means if we don't write any property like window.property,which is exactly same as property means if we want we can ignore window.**
 
![image](https://github.com/user-attachments/assets/831f8351-f9cf-4000-aec9-1ac6c5aeb703)
### alert()
- **displays the alert box containing message with ok button.**
![image](https://github.com/user-attachments/assets/d1136e7e-dce4-49ca-8155-bc00d2fac132)
## confirm()
- **displays the confirm dialog box containing message with ok and cancel button.**
![image](https://github.com/user-attachments/assets/1c05794b-30d2-4e00-adc4-37403b4f525e)
## prompt()
- **displays a dialog box to get input from the user.**
![image](https://github.com/user-attachments/assets/a504cb46-5ae3-415d-9090-3968c56a4efa)
## open()
- **opens the new window.**
![image](https://github.com/user-attachments/assets/294f8205-22a9-4617-bc01-0a0693f082c4)

https://github.com/user-attachments/assets/fb5cd41b-f225-4822-b34b-70a8a470d5a5
## close()
- **closes the current window.**

https://github.com/user-attachments/assets/b8893843-3801-4f9f-8740-4ce5e1024450

### history Object:
- **Represents the session history, allowing navigation through the browser history.**
- **Example: window.history.back(), window.history.forward().**
- **Most of the cases we are using window.history.back(), window.history.forward(),window.history.go().**
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link
      href="https://fonts.googleapis.com/css2?family=Urbanist:wght@400;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="../style.css" />
  </head>
  <body>
    <h1>JS Window Obj</h1>
    <!--? ========== Start Window Property ========== -->
    <button
      onclick="window.open('https://thapatechnical.shop/courses', '_blank')">
      Navigate
    </button>
    <!--? ========== End Window Property ========== -->
    <!--? ========== Start History ========== -->
    <h1>JavaScript History Object</h1>
    <button onclick="history.back()">Go Back</button>
    <button onclick="history.forward()">Go Forward</button>
    <button onclick="history.go(-1)">Move Backward or forward</button>
    <!--? ========== End History ========== -->
    <!--? ========== Start Location ========== -->
    <h1>JavaScript Location Object</h1>
    <button onclick="location.reload()">Reload the Page</button>
    <button
      onclick="window.location.replace('https://www.thapatechnical.com/')">
      Navigate Page using replace
    </button>
    <!--* Purpose: Assigns a new URL to the current window, effectively navigating to a new page. -->
    <button onclick="location.assign('https://kodyfier.com/')">
      Navigate Page with Assign
    </button>
    <!--? ========== End Location ========== -->
    <!--? ========== Start Screen ========== -->
    <h1>JavaScript Screen Object</h1>
    <p>We will see in console.</p>
    <!--? ========== End Screen ========== -->
    <script>
      window.alert("welcome to the js course ");
    </script>
  </body>
</html>
////index.js
```
https://github.com/user-attachments/assets/2d5211ac-134c-453e-80d3-b81331cb715b

### location Object:

#### window.location.href (Property):
- **Returns or sets the complete URL of the current page.**
- **Example: ```console.log(window.location.href).```**
#### Output:
![image](https://github.com/user-attachments/assets/8e6d66bb-969d-4730-bbf8-25490e513735)

#### window.location.hostname (Property):
- **Returns the domain name of the web host.**
- **Example: ```console.log(window.location.hostname).```**
#### Output:
![image](https://github.com/user-attachments/assets/0f10f816-a560-49e5-8a37-a855056400c6)

#### window.location.assign(url) (Method):
- **Navigates to the specified URL.**
- **Assigns a new URL to the current window, effectively navigating to a new page.**
- **Example: ```window.location.assign("https://www.example.com").```**

#### window.location.reload(forceReload) (Method):
- **Reloads the current page.**
- **Syntax: ```window.location.reload(true).```**
#### window.location.replace()(Method):
- **It will replace the existing page and we are unable to back that page.
- - **Syntax: ```window.location.replace()```
#### window.location.search (Property):
- **Returns the query string part of the URL.**
- **Example: ```console.log(window.location.search)```**
- **o/p = "?name=John&age=25"**
#### Combined Example
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link
      href="https://fonts.googleapis.com/css2?family=Urbanist:wght@400;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="../style.css" />
  </head>
  <body>
    <h1>JS Window Obj</h1>
    <!--? ========== Start Window Property ========== -->
    <button
      onclick="window.open('https://thapatechnical.shop/courses', '_blank')">
      Navigate
    </button>
    <!--? ========== End Window Property ========== -->
    <!--? ========== Start History ========== -->
    <h1>JavaScript History Object</h1>
    <button onclick="history.back()">Go Back</button>
    <button onclick="history.forward()">Go Forward</button>
    <button onclick="history.go(-1)">Move Backward or forward</button>
    <!--? ========== End History ========== -->
    <!--? ========== Start Location ========== -->
    <h1>JavaScript Location Object</h1>
    <button onclick="location.reload()">Reload the Page</button>
    <button
      onclick="window.location.replace('https://www.thapatechnical.com/')">
      Navigate Page using replace
    </button>
    <!--* Purpose: Assigns a new URL to the current window, effectively navigating to a new page. -->
    <button onclick="location.assign('https://kodyfier.com/')">
      Navigate Page with Assign
    </button>
    <!--? ========== End Location ========== -->
    <!--? ========== Start Screen ========== -->
    <h1>JavaScript Screen Object</h1>
    <p>We will see in console.</p>
    <!--? ========== End Screen ========== -->
    <script>
      window.alert("welcome to the js course ");
    </script>
  </body>
</html>
////index.js
```

https://github.com/user-attachments/assets/fe86f69a-817c-4e50-9fa0-1cfc3ac68274

### 4)screen Object:
#### window.screen.width and window.screen.height (Properties):
- **Represent the width and height of the user's screen.**
- **Example: console.log(window.screen.width).**

#### window.screen.availWidth and window.screen.availHeight (Properties):
- **Represent the available width and height of the user's screen (excluding taskbars).**
- **Example: console.log(window.screen.availWidth).**

#### window.screen.colorDepth (Property):
- **Returns the number of bits used to represent the color of each pixel.**
- **Example: console.log(window.screen.colorDepth).**

#### window.screen.orientation (Property):
- **Returns the current orientation of the user's screen.**
- **Example: console.log(window.screen.orientation).**

#### window.screen.pixelDepth (Property):
- **Returns the number of bits used to represent each pixel.**
- **Example: console.log(window.screen.pixelDepth).**
#### Combined Example
![image](https://github.com/user-attachments/assets/0314a0b8-d3a0-4371-8fa7-205b03a8accb)

# DOM(Document Object Module)
- **When a web browser loads an HTML document, it parses the HTML source code and creates a tree-like structure known as the Document Object Model (DOM). This DOM tree represents the structure of the HTML document, with each HTML element being a node in the tree.**
- ** This entire DOM tree is then accessible to JavaScript as an object. JavaScript can interact with this object to manipulate the content, structure, and style of the document dynamically.**
- **The DOM essentially serves as an interface between the HTML document and JavaScript, providing a way for scripts to access and modify the document's structure and content.**
- **The Document Object Model (DOM) is an Application Programming Interface (API). The DOM Tree is the structure of your HTML document, as represented by the DOM API. As stated, this API then gives us many methods and properties that we can use to manipulate the Tree, and therefore, by extension, the document.**

- **Here is a types of nodes in js:**

- **Element node:  An HTML tag, the tree building blocks.**

- **Text node:  In the DOM tree, text content, including new lines, spaces, and tabs, is treated as text nodes.**

- **Attribute node: An attribute of an element.**

- **Comment node: Represent comments within the HTML document.**

- **Processing instruction node:  A processing instruction node, such as <? xml-stylesheet … ?>.**

- **Document node:  A document node.**

- **Document type node: A document type node, such as <! DOCTYPE html>.**

 # DOM Properties and Methods

##  DOM Properties:
### 1)document
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Best JS Course</title>
    <!-- <link
      href="https://fonts.googleapis.com/css2?family=Urbanist:wght@400;800&display=swap"
      rel="stylesheet"
    /> -->
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h1>Best JS Course</h1>
    <p>Understanding The DOM Tree Structure</p>
    <hr />
    <p>It's easy. Helps JS to communicate with HTML</p>

    <!-- * Let's see DOM Navigation -->
    <script>
     ////Example of document
      let parent = document;
      console.log(parent);
      ////Example of document.body
      let htmlBody = document.body;
      //console.log(htmlBody);
      ////Example of document.head
      let htmlHead = document.head;
      //console.log(htmlHead);
      ////Example of document.childNodes-->return NodeList
      // let bodyChild = htmlBody.childNodes;
      // console.log(bodyChild);
      ////Example of document.children-->return HTML Collection
      let bodyChild = htmlBody.children;
      //console.log(bodyChild);
      let firstChild = htmlBody.firstElementChild;
       console.log(firstChild);
       let firstChild = htmlBody.firstChild;
       console.log(firstChild);
       let lastChild = htmlBody.lastChild;
      // let lastChild = htmlBody.lastElementChild;
      console.log(lastChild);
       let nextSibling = firstChild.nextElementSibling;
      console.log(nextSibling);
      let previousSibling = nextSibling.previousElementSibling;
      console.log(previousSibling)
      let parentNode = previousSibling.parentElement;
      console.log(parentNode);
    </script>
  </body>
</html>
```
# DOM Navigation
### document:document represents the entire document
- **Syntax:`console.log(document);`**
#### Output:document
![image](https://github.com/user-attachments/assets/7a77d321-5b04-43ce-a897-047ef42d1cf7)
### Document.documentElement returns the Element that is the root element of the document (for example, the <html> element for HTML documents).
#### Output:document.body
![image](https://github.com/user-attachments/assets/6ceef7d8-944d-40a6-b340-28df144172ca)
#### Output:document.head
![image](https://github.com/user-attachments/assets/45835947-aae3-4d70-8d4d-8e2e949f1770)
#### childNodes / children:
- **Navigate to child nodes or elements.**
- **childNodes is a property that returns a NodeList containing all child nodes of a given element, including text nodes and comment nodes.**
#### Output:document.body.childNodes-->return NodeList
- **childNodes is a property that returns a NodeList containing all child nodes of a given element, including text nodes and comment nodes.**
![image](https://github.com/user-attachments/assets/0f139190-11fc-4eba-8c2c-e47fd7a26f3c)
#### Output:document.body.children-->return HTML Collection
![image](https://github.com/user-attachments/assets/ce5a4bb6-15ff-4ea4-a826-927a30df1db5)
### firstChild / firstElementChild:
- **Navigate to the first child node or element.**
- **todo The Element suffix in firstElementChild and similar properties signifies that only element nodes are considered.**
#### firstChild / firstElementChild:
- **Navigate to the first child node or element.**
#### Output:document.body.firstElementChild;
![image](https://github.com/user-attachments/assets/ae905242-3fa7-48ae-adce-debec5c8cd76)
#### lastChild / lastElementChild:
- **Navigate to the last child node or element.**
#### Output:document.body.lastChild/lastElementChild
![image](https://github.com/user-attachments/assets/8042512d-f7e6-4cd8-945d-cf3abc890e40)
## Filtering Siblings:
#### nextSibling / nextElementSibling:
- **Navigate to the next sibling node or element.**
#### previousSibling / previousElementSibling:
- **Navigate to the previous sibling node or element.**
#### Output: nextSibling,previousElementSibling,parentNode,parentElement
- **Navigate to the parent node or element.**
- **Document and DocumentFragment nodes can never have a parent, so parentNode will always return null. It also returns null if the node has just been created and is not yet attached to the tree.**
![image](https://github.com/user-attachments/assets/b99c55b3-c283-40ef-b8d9-ac217271d26c)
#### closest(selector):
- **Find the closest ancestor of the current element that matches a given selector.**
- **The closest(selector) method is used to find the closest ancestor of an element that matches a specified CSS selector. This method traverses up the DOM tree, starting from the current element, and returns the first ancestor that matches the provided selector. If no matching ancestor is found, it returns null.**
### All together example
![image](https://github.com/user-attachments/assets/7a5a3eec-b3eb-4876-bde3-a333db295873)


# DOM Searching
- **These following 3 property always create confusion that's why we get clear idea from this 3 following property
- **The `innerHTML` property returns the complete content, including all HTML tags, inside the `ul` elements and their text content.**
- **Example using `innerText`: Prints text as it appears on screen, considering styling and excluding hidden text.**
- **Example using `textContent`: Prints text as it is in the markup, including hidden text and without considering styling.
- **Above 3 property(**`innerHTML`, `innerText`,`textContent`**) will be using every time when we use dom.
### getElementById(id):Find an element by its ID.

![image](https://github.com/user-attachments/assets/80c42be5-161b-4dba-8ee2-c5d89c4bc5a9)

### getElementsByClassName(className):Find elements with a specific class name.

![image](https://github.com/user-attachments/assets/95ef16a7-834f-4211-b4ac-a88301ca9566)

### getElementsByTagName(tagName): Find elements with a specific tag name.

![image](https://github.com/user-attachments/assets/3da7dada-abb7-4c42-bccd-7cf0e2895cb3)

### querySelector(selector):Find the first element that matches the specified CSS selector.

![image](https://github.com/user-attachments/assets/9bc778fa-ff18-44ee-a4cf-c1e7b4274d15)

### querySelectorAll(selector):Find all elements that match the specified CSS selector.

![image](https://github.com/user-attachments/assets/71b0bdcb-2303-4cd3-ae21-3f2503260909)

### innerHTML
### textContent
### style

# DOM Methods:
### createElement(tagName)
### appendChild(node)
### removeChild(node)
### addEventListener(event, function)
### removeEventListener(event, function)
### setAttribute(name, value)
### getAttribute(name)
### parentNode / parentElement
### childNodes / children
### firstChild / firstElementChild
### lastChild / lastElementChild
### nextSibling / nextElementSibling
### previousSibling / previousElementSibling
### closest(selector)
### forEach (Array.from)

# DOM - CRUD (Create, Read, Update, Delete):

#### createElement(tagName): Create a new HTML element.

#### appendChild(node): Append a node as the last child of a parent node.

#### removeChild(node): Remove a child node from its parent.

#### addEventListener(event, function): Create an event listener to handle events.

#### removeEventListener(event, function): Remove an event listener.

#### setAttribute(name, value): Set the value of an attribute on an element.

#### getAttribute(name): Get the value of a specific attribute on an element.

#### innerHTML: Read or update the HTML content of an element.

#### textContent: Read or update the text content of an element.

# DOM - Iteration

### Iteration:
- **forEach (Array.from): Iterate through NodeList or convert to an array for more flexible manipulation.**
### Very important
- **When you use the browser's developer tools console to select an element and change its text content using JavaScript, you are directly manipulating the DOM object in memory. Since the DOM is a live representation of the document, any changes you make to the DOM objects are immediately reflected in the rendered web page.**

- **However, these changes are typically temporary and exist only in the current session. When you refresh the page or navigate away, the browser reloads the original HTML document from the server, and the DOM is reconstructed during the parsing process. Any modifications made to the DOM objects during the previous session are lost, and the page reverts to its original state.**

