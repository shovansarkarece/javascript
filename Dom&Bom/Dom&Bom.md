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



