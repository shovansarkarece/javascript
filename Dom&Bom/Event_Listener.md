# EVENTS
![image](https://github.com/user-attachments/assets/aa4900ff-6418-4ab0-94ef-aeb0943b90de)
# Mouse Events
![image](https://github.com/user-attachments/assets/b8167244-a45a-419a-9003-e78a904c77ef)
# Types of Events
![image](https://github.com/user-attachments/assets/adf48e65-fe45-483a-94d5-92d8215c5899)
![image](https://github.com/user-attachments/assets/804f70dc-50f5-4f89-ac58-d6df2f5bc33d)
# Ways to Assign EventHandeler
![image](https://github.com/user-attachments/assets/095d32cb-9b24-42fe-b2b2-b117cad9d141)

# Event Listener
![image](https://github.com/user-attachments/assets/6f646939-175e-489c-b818-2e2fa0bd6a9d)
# Another Example
![image](https://github.com/user-attachments/assets/e50a3430-01ac-4604-a59d-a95adf523d54)


#### addEventListener(event, function): Create an event listener to handle events.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <section id="content">
        <h1 id="heading">Hello From Interactive Cares...</h1>
        <p class="text">Welcome to our DOM Class</p>
        <p class="text">Today we are going to learn about DOM</p>
        <p class="text">DOM stands for Document Object Model</p>
    </section>
    <p id="footer">Copyright</p>
    <div>Hello Hello</div>
    <button style="margin-top:10px;" id="click">Make Bold</button>
    <script>
        const button = document.getElementById('click')
        button.addEventListener('click', function () {
            const paragraphs = document.getElementsByTagName('p')
            for(let i=0 ; i < paragraphs.length; i++){
                paragraphs[i].innerHTML = "<strong>"+paragraphs[i].innerHTML+"</strong>";
//////Using Template literal we also write the above code like below
                //     paragraphs[i].innerHTML = `<strong>${paragraphs[i].innerHTML}</strong>`;
            }
        })
    </script>
</body>

</html>
```
#### Output
![image](https://github.com/user-attachments/assets/c472e5e0-aecd-4046-a8ec-e2e115df64d5)
# Using For of loop
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <section id="content">
        <h1 id="heading">Hello From Interactive Cares...</h1>
        <p class="text">Welcome to our DOM Class</p>
        <p class="text">Today we are going to learn about DOM</p>
        <p class="text">DOM stands for Document Object Model</p>
    </section>
    <p id="footer">Copyright</p>
    <div>Hello Hello</div>
    <button style="margin-top:10px;" id="click">Make Bold</button>
    <script>
        const button = document.getElementById('click')
        button.addEventListener('click', function () {
            const paragraphs = document.getElementsByTagName('p')
   for(let paragraph of paragraphs){
                paragraph.innerHTML = `<strong>${paragraph.innerHTML}</strong>`;
            }
            }
        })
    </script>
</body>
</html>
```
#### Output
![image](https://github.com/user-attachments/assets/c472e5e0-aecd-4046-a8ec-e2e115df64d5)
## getElementsByClassName(className): Find elements with a specific class name.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <section id="content">
        <h1 id="heading">Hello From Interactive Cares...</h1>
        <p class="bold">Welcome to our DOM Class</p>
        <p class="bold">Today we are going to learn about DOM</p>
        <p class="bold">DOM stands for Document Object Model</p>
        <p>This is a normal Paragraph</p>
    </section>
    <p id="footer">Copyright</p>
    <div>Hello Hello</div>
    <button style="margin-top:10px;" id="click">Make Bold</button>
    <script>
        const button = document.getElementById('click')
        button.addEventListener('click', function () {
            const paragraphs = document.getElementsByClassName('bold')
            // console.log(paragraphs)
            for(let i=0 ; i < paragraphs.length; i++){
                // paragraphs[i].innerHTML = "<strong>"+paragraphs[i].innerHTML+"</strong>";
                paragraphs[i].innerHTML = `<strong>${paragraphs[i].innerHTML}</strong>`;
            }
            button.innerText = "Make Normal"
        })
    </script>
</body>
</html>
```
#### Output
![image](https://github.com/user-attachments/assets/87232e09-2c0c-4e7a-8bd8-3038332b6c0c)
## querySelector(selector):Find the first element that matches the specified CSS selector.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <section id="content">
        <h1 id="heading">Hello From Interactive Cares...</h1>
        <h2 class="bold">This is a heading</h2>
        <p class="bold">Welcome to our DOM Class</p>
        <p class="bold">Today we are going to learn about DOM</p>
        <p class="bold">DOM stands for Document Object Model</p>
        <p>This is a normal Paragraph</p>
    </section>
    <p id="footer">Copyright</p>
    <div>Hello Hello</div>
    <button style="margin-top:10px;" id="click">Make Bold</button>
    <script>
        const button = document.getElementById('click')
        button.addEventListener('click', function () {
            // const elements = document.querySelector("p.bold")
            const elements = document.querySelectorAll("p.bold")
            elements.forEach(element => {
                element.innerHTML = `<em>${element.innerHTML}</em>`
            })
        })
    </script>
</body>
</html>
```
#### Output
![image](https://github.com/user-attachments/assets/9d712ee5-56bb-4957-b12a-6eb75f00f65b)
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

# Event Object
![image](https://github.com/user-attachments/assets/57358684-779d-4f09-aca1-d6fb57a46c09)
# Example
![image](https://github.com/user-attachments/assets/ede8c6a8-e895-49fc-9223-9c8ef1ad972b)
# Another Example
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Event</title>
    <style>
        body {
            background-color: black;
            color: white;
        }
        div {
            background-color: blue;
            height: 100px;
            width: 100px;
            margin: 100px;
        }
    </style>
</head>
<body>
    <h1>We are learning event right now</h1>
    <button id="bt1">change to dark</button>
    <button id="bt2">change to light</button>
    <div onmouseover="bgChange()" onmouseleave="bgChange2()">
        div
    </div>
    <script>
        let bt1 = document.querySelector('#bt1');
        let bt2 = document.querySelector('#bt2');
        bt1.addEventListener('click', (e)=>{
            document.body.style.backgroundColor = 'black'
            document.body.style.color = 'white'
            console.log(e.type);
            console.log(e.target)
        })
        bt2.addEventListener('mouseover', ()=>{
            document.body.style.backgroundColor = 'white'
            document.body.style.color = 'black'
        })
        let bgChange = () => {
            let div = document.querySelector('div')
            div.style.backgroundColor = 'yellow'
        }
        let bgChange2 = () => {
            let div = document.querySelector('div')
            div.style.backgroundColor = 'blue'
        }
    </script>
</body>
</html>
```
# Example of Keydown and input
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="https://matcha.mizu.sh/matcha.css">
</head>
<body>
    <h1>Input Events</h1>

    Type Something:
    <input type="text" id="name" placeholder="Enter your name">
    
    <script>
        const name = document.getElementById('name');
        // name.addEventListener('input', function() {
        //     console.log(this.value);
        // })

        //keydown
        name.addEventListener('keydown', function(event) {
            const keyCode = event.keyCode;
            console.log(keyCode);
            console.log(event)
        })
    </script>
</body>
</html>
```
# Example of submit
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="https://matcha.mizu.sh/matcha.css">
</head>
<body>
    <h1>Contact Form</h1>
    <form id="contact" method="POST">
        <label for="name">Name:</label>
        <input type="text" id="name" placeholder="Enter your name">
        <br>
        <label for="email">Email:</label>
        <input type="email" id="email" placeholder="Enter your email">
        <br>
        <label for="message">Message:</label>
        <textarea name="message" id="message" cols="30" rows="10" placeholder="Enter your message"></textarea>
        <br>
        <button type="submit">Submit</button>
    </form>

    <script>
        const contact = document.getElementById('contact');
        contact.addEventListener('submit',function(event){
            const email = document.getElementById('email').value
            console.log(email)
            event.preventDefault()
        })
    </script>
</body>
</html>
```

# this Exception
- **this will not work for arrow function**
- **with an event listener like the below example it will not work properly.**
![image](https://github.com/user-attachments/assets/e8e00d05-3b10-4ec9-9021-d031995030c9)
### this will work on below EventListener properly.
![image](https://github.com/user-attachments/assets/56112fc1-cefa-41e6-bc02-47a3c73900f7)

