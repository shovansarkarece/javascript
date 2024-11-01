# EVENTS
![image](https://github.com/user-attachments/assets/aa4900ff-6418-4ab0-94ef-aeb0943b90de)
# Mouse Events
![image](https://github.com/user-attachments/assets/b8167244-a45a-419a-9003-e78a904c77ef)

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
