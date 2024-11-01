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

