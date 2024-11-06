# DOM
### Very important
- **When you use the browser's developer tools console to select an element and change its text content using JavaScript, you are directly manipulating the DOM object in memory. Since the DOM is a live representation of the document, any changes you make to the DOM objects are immediately reflected in the rendered web page.**

- **However, these changes are typically temporary and exist only in the current session. When you refresh the page or navigate away, the browser reloads the original HTML document from the server, and the DOM is reconstructed during the parsing process. Any modifications made to the DOM objects during the previous session are lost, and the page reverts to its original state.**

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
- **It will replace the existing page and we are unable to back that page.**
- - **Syntax: ```window.location.replace()```**
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
- **This entire DOM tree is then accessible to JavaScript as an object. JavaScript can interact with this object to manipulate the content, structure, and style of the document dynamically.**
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

#### firstChild / firstElementChild:
- **Navigate to the first child node or element.**
- **The firstChild property returns the first child node of a node.**
- **The firstChild property returns a node object.**
- **The firstChild property is read-only.**
- **The firstChild property is the same as childNodes[0].**
- **Navigate to the first child node or element.**
#### Output:document.body.firstElementChild;
![image](https://github.com/user-attachments/assets/ae905242-3fa7-48ae-adce-debec5c8cd76)

### lastChild / lastElementChild:
- **The lastChild property returns the last child node of a node.**
- **The lastChild property returns returns a node object.**
- **The lastChild property is read-only.**
- **Navigate to the last child node or element.**
#### Output:document.body.lastChild/lastElementChild
![image](https://github.com/user-attachments/assets/8042512d-f7e6-4cd8-945d-cf3abc890e40)
### Combined Example of firstChild / firstElementChild  and lastChild / lastElementChild
#### Example:
![image](https://github.com/user-attachments/assets/68779b28-f74e-4033-b359-4ecf6ad5eb1e)

## Filtering Siblings:
#### nextSibling / nextElementSibling:
- **Navigate to the next sibling node or element.**
- **The nextSibling property returns the next node on the same tree level.**
- **The nextSibling returnes a node object.**
- **The nextSibling property is read-only.**
#### previousSibling / previousElementSibling:
- **Navigate to the previous sibling node or element.**
- **The previousSibling property returns the previous node on the same tree level.**
- **The previousSibling property returns a node object.**
- **The previousSibling property is read-only.**
#### Output: nextSibling,previousElementSibling,parentNode,parentElement
- **Navigate to the parent node or element.**
- **Document and DocumentFragment nodes can never have a parent, so parentNode will always return null. It also returns null if the node has just been created and is not yet attached to the tree.**
#### Example:
![image](https://github.com/user-attachments/assets/b99c55b3-c283-40ef-b8d9-ac217271d26c)

### Combined Example of nextSibling / nextElementSibling and previousSibling / previousElementSibling
#### Example:
![image](https://github.com/user-attachments/assets/a873ab6b-314f-4226-b8aa-3eeb4afb16b9)

#### closest(selector):
- **Find the closest ancestor of the current element that matches a given selector.**
- **The closest(selector) method is used to find the closest ancestor of an element that matches a specified CSS selector. This method traverses up the DOM tree, starting from the current element, and returns the first ancestor that matches the provided selector. If no matching ancestor is found, it returns null.**
### All together example
![image](https://github.com/user-attachments/assets/7a5a3eec-b3eb-4876-bde3-a333db295873)

# DOM Searching
- **These following 3 property always create confusion that's why we get clear idea from this 3 following property.**
- **The `innerHTML` property returns the complete content, including all HTML tags, inside the `ul` elements and their text content.Read or update the HTML content of an element.**
- **Example using `innerText`: Prints text as it appears on screen, considering styling and excluding hidden text.**
- **Example using `textContent`: Prints text as it is in the markup, including hidden text and without considering styling.Read or update the text content of an element.**
- **Above 3 property(**`innerHTML`, `innerText`,`textContent`**) will be using every time when we use dom.**
### getElementById(id):Find an element by its ID.

![image](https://github.com/user-attachments/assets/80c42be5-161b-4dba-8ee2-c5d89c4bc5a9)

#### Another Example

![image](https://github.com/user-attachments/assets/0901542c-e7b5-4991-a352-6c5f317846b5)


#### Another Example

![image](https://github.com/user-attachments/assets/ff73e3ec-8b11-4806-acba-435795a48e7e)

### getElementsByClassName(className):Find elements with a specific class name.

![image](https://github.com/user-attachments/assets/95ef16a7-834f-4211-b4ac-a88301ca9566)

### getElementsByTagName(tagName): Find elements with a specific tag name.

![image](https://github.com/user-attachments/assets/3da7dada-abb7-4c42-bccd-7cf0e2895cb3)

### querySelector(selector):Find the first element that matches the specified CSS selector.

![image](https://github.com/user-attachments/assets/9bc778fa-ff18-44ee-a4cf-c1e7b4274d15)

### querySelectorAll(selector):Find all elements that match the specified CSS selector.

![image](https://github.com/user-attachments/assets/71b0bdcb-2303-4cd3-ae21-3f2503260909)

### innerHTML

![image](https://github.com/user-attachments/assets/3dd7ba44-468a-422c-8794-127d0779b1b1)

### All code together example
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Document</title>
    <link
      href="https://fonts.googleapis.com/css2?family=Urbanist:wght@400;800&display=swap"
      rel="stylesheet"
    />
    <style>
      body,
      button,
      input {
        font-family: "Urbanist", sans-serif;
      }
    </style>
  </head>
  <!-- it's a comment node  -->
  <body>
    <div>
      <h1 id="heading">DOM API</h1>
      <ul class="list-of--nodes">
        <li>1 node</li>
        <li>2 node</li>
        <li>3 node</li>
        <!-- <li>4th node </li> -->
        <li>4 node</li>
        <li style="display: none">5 node</li>
      </ul>
    </div>
    <div>
      <h1>DOM API 2</h1>
      <input type="text" />
      <button>click me</button>
      <div class="value"></div>
    </div>
    <script>
//////////////// getElementById Example
      // let findElementById = document.getElementById("heading");
      // let findElementById = document.getElementById("#heading"); ❌
      ////////////getElementsByClassName Example
      // const findElementByClassName =
      //   document.getElementsByClassName("list-of--nodes");

      // console.log(...findElementByClassName);

      // for (let elem of findElementByClassName) {
      //   console.log(elem.innerHTML);
      //   console.log(elem.innerText);
      //   console.log(elem.textContent);
      // }
//////////////// getElementById Example
      // console.log(findElementById.innerHTML);
      // console.log(findElementById.innerText);
      // console.log(findElementById.textContent);

      // The `innerHTML` property returns the complete content, including all HTML tags, inside the `ul` elements and their text content.

      // Example using `innerText`: Prints text as it appears on screen, considering styling and excluding hidden text.

      // Example using `textContent`: Prints text as it is in the markup, including hidden text and without considering styling.
//////////////// getElementByTagName Example
      // const getElementsByTagName = document.getElementsByTagName("li");
      // console.log(getElementsByTagName);
      // console.log(...getElementsByTagName);
      // for (let name of getElementsByTagName) {
      //   console.log(name);
      // }
//////////////querySelector Example
      // const findElementByQuerySelector = document.querySelector("#heading");
      // console.log(findElementByQuerySelector);
      // console.log(findElementByQuerySelector.innerText);
      // console.log(findElementByQuerySelector.innerHTML);
      // console.log(findElementByQuerySelector.textContent);
      // console.log(
      //   (findElementByQuerySelector.innerText = "innerText added by the help of QuerySelector")
      // );
//////////////querySelectorAll Example
      const findElementByQuerySelectorAll = document.querySelectorAll("li");
      console.log(findElementByQuerySelectorAll);
      findElementByQuerySelectorAll.forEach((curElem) => console.log(curElem));
    </script>
  </body>
</html>
```

### Style:To style any element we use style 
- But in css property we use `background-color` but in dom styling we will use `backgroundColor`.That is the main difference.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* h1{
            color: red;
            font-size:50px;
        } */
    </style>
</head>
<body>
    <section id="s1">
        <h1 id="heading1">This is section one</h1>
        <p>Paragraph one in section one</p>
        <p>Paragraph two in section one</p>
        <p>Paragraph three in section one</p>
    </section>

    <section id="s2" style="background-color: red; color:white; padding: 10px; width:250px">
        <h2 id="heading2">This is section two</h2>
        <p>Paragraph one in section two</p>
        <p>Paragraph two in section two</p>
        <p>Paragraph three in section two</p>
    </section>

    <button style="margin-top:10px;" id="click">Modify</button>

    <script>
        const button  = document.getElementById('click')
        button.addEventListener('click',function(){
            const h1 = document.getElementById('heading1')
            h1.style.color = 'red'
            h1.style.fontSize = '50px'

            const s2 = document.getElementById('s2')
            s2.style.backgroundColor = 'green'
            s2.style.borderRadius = '20px'
        })
    </script>
</body>
</html>
```
#### Output
![image](https://github.com/user-attachments/assets/3e444d7c-ff68-41cc-ba51-6b67558a0657)
#### Another Example
![image](https://github.com/user-attachments/assets/ea05c339-0cc6-4ffc-bb86-67dd02b3e95b)


# DOM Methods:
### createElement(tagName): 
## Example
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div>
        <ul>
            <li class="hero">Andrew Tale</li>
            <li class="hero">Keanu Reeves</li>
            <li id="hero1">Johnny Bravo</li>
            <li>Johnny Depp</li>
            <li>shinchan</li>
        </ul>
    </div>
    <script>
    //////createElement
    let elem=document.querySelector("ul");
    let createElem=document.createElement("li");
    // Set content for the new 'li' element
    createElem.textContent="New Hero"
    // Append the new 'li' to the 'ul'
    elem.appendChild(createElem);
    // Log the new element
    console.log(createElem);
    </script>
</body>
</html>
```
### Output:
![image](https://github.com/user-attachments/assets/af1e544e-b744-4f28-81f4-bb4f5579f118)

#### appendChild(node): Append a node as the last child of a parent node.
insertAdjacentElement() insertAdjacentHTML() cloneNode()  contains()  hasAttribute() hasChildNodes() isEqualNode() 

![image](https://github.com/user-attachments/assets/3e2b205b-1241-44db-ab96-d68ce9f302bb)

# insertBefore()
- **The insertBefore() method inserts a child node before an existing child.**
- **Syntax:`element.insertBefore(new, existing) or node.insertBefore(new, existing)`**
- **The node (element) to insert before.If null, it will be inserted at the end.**

![image](https://github.com/user-attachments/assets/ba76b2bb-38b9-4930-b329-297f9e25d424)

# replaceChild()
- **The `replaceChild()` method replaces a child node with a new node.**
### Example
![image](https://github.com/user-attachments/assets/d9316a49-4772-4632-98f4-9df6ed7400f8)

### removeChild(node)
- **The removeChild() method removes an element's child.**
### Example
![image](https://github.com/user-attachments/assets/b17966b4-c5b8-47ba-a02f-64ec25c82a79)

### Another Example
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <section id="s1">
        <h1>This is section one</h1>
        <p>Paragraph one in section one</p>
        <p>Paragraph two in section one</p>
        <p>Paragraph three in section one</p>
    </section>
    <section id="s2">
        <h2>This is section two</h2>
        <p>Paragraph one in section two</p>
        <p>Paragraph two in section two</p>
        <p>Paragraph three in section two</p>
    </section>
    <button style="margin-top:10px;" id="click">Modify</button>
    <script>
        const button = document.getElementById('click')
        button.addEventListener('click', function () {
            const s1 = document.getElementById('s1')
            const paragraphs = s1.querySelectorAll('p')
            paragraphs.forEach(p=>{
                p.remove()
            })
        })
    </script>
</body>
</html>
```
#### Output
![image](https://github.com/user-attachments/assets/cb1a6ec6-8756-4449-aa97-d690e2c44a88)

#### setAttribute(name, value): Set the value of an attribute on an element.
### Example of setAttribute()
![image](https://github.com/user-attachments/assets/1eebfb8e-9a00-4928-8009-a69ec486a7cb)

### getAttribute(name)
#### getAttribute(name): Get the value of a specific attribute on an element.
### Example of getAttribute()
![image](https://github.com/user-attachments/assets/90de01f4-1dcd-46af-80ad-0b5acce76e2a)

### parentNode / parentElement
### Example of parentNode / parentElement
![image](https://github.com/user-attachments/assets/65a18f83-f0e1-4a19-879b-aca17b53abb9)

### childNodes / children
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"content="width=device-width,initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div>
        <ul>
            <li class="hero">Andrew Tale</li>
            <li class="hero">Keanu Reeves</li>
            <li id="hero1">Johnny Bravo</li>
            <li>Johnny Depp</li>
            <li>shinchan</li>
        </ul>
    </div>
    <script src="practise.js">
    ////children
var k=document.querySelector('div');
var l=k.children;
console.log(l);
console.log(l[0]);
///childNodes
var m=document.querySelector('ul');
var n=m.childNodes;
console.log(n);
console.log(n[0]);
console.log(n[1]);
console.log(n[2]);
//////childElementCount
var o=document.querySelector('ul');
var p=o.childElementCount;
console.log(p);
    </script>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/63eaab37-dfd6-4cee-9a18-9f2a69e7179e)

# DOM - CRUD (Create, Read, Update, Delete):

#### createElement(tagName): Create a new HTML element.

![image](https://github.com/user-attachments/assets/22412608-bf4f-4044-9af8-e54254b315f1)

# createTextNode()
- **The createTextNode() method creates a text node.**
- **Syntax:`document.createTextNode(text)`**
# createComment()
- **The createComment() method creates a comment and returns the comment node.**
- **Syntax:`document.createComment(text)`**
### Example of createTextNode() and createComment()
```
<!DOCTYPE html>
<html>
<head>
    <title>DOM Navigation</title>
    <style>
        h1{
            text-align: center;
            color:#ff0000;
        }
    </style>
</head>
<body>
    <h1>Yahoo Baba : DOM Create Methods</h1>
    <script>
// var newElement = document.createElement("p");
// var newElement = document.createElement("h2");
// console.log(newElement);
// var newText = document.createTextNode("This is just text");
// console.log(newText);
/* Dom Create  Comment*/
// var newComment = document.createComment("this is comment");
// console.log(newComment);
    </script>
</body>
</html>
```
### Combined Example of createTextNode() and createComment()
![image](https://github.com/user-attachments/assets/dc581623-254e-4a68-8616-f1efc691f7b9)



### addEventListener(event, function)

### removeEventListener(event, function)

#### removeChild(node): Remove a child node from its parent.

#### removeEventListener(event, function): Remove an event listener.






