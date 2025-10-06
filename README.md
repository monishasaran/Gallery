# Ex.08 Design of Interactive Image Gallery
# Date:06.10.2025
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>gallery</title>
</head>
<style>
    .gallery{
        display: flex;
        flex-direction: row;
        height:auto;
        width:200px;
        gap:20px;
        margin-bottom: 20px;
        background-color: #585858;
    }
    .gallery-image{
        width:200px;
        height: 500px;
        align-items: center;
    }
    .gallery1{
        display: flex;
        flex-direction: column;
        height:auto;
        width:200px;
        gap:10px;
        margin-bottom: 10px;

    }
    .zoom{
        transition : transform 1.8s;
    }
    .zoom:hover{
        transform: scale(1.1);

    }
    #photomodel {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }
    #photomodel img {
            max-width: 80%;
            max-height: 80%;
        }
    .close-btn {
      position: absolute;
      top: 8px;
      right:6px;
      background-color: red;
      color:black solid;
      border: 3px;
      border-radius: 20%;
      width: 70px;
      height: 30px;
      font-weight: bold;
      cursor: pointer;
      text-align: center;
      line-height: 25px;
      font-size: 18px;
    }

</style>
<body bgcolor="grey">
    <div class="gallery">
     <div class="gallery-img">
        <img src="{% static 'thanjavur.png' %}" onclick="openModal(this)" class="zoom">
     </div>
     <div class="gallery-img">
        <img src="{% static 'photo4.png' %}" onclick="openModal(this)" class="zoom">
     </div>
     <div class="gallery-img">
        <img src="{% static 'photo6.png' %}" onclick="openModal(this)" class="zoom">
    </div>
</div>

<div class="gallery">
    <div class="gallery-img">
        <img src="{% static 'photo1.png' %}" onclick="openModal(this)" class="zoom">
    </div>
    <div class="gallery-img">
        <img src="{% static 'photo5.png' %}" onclick="openModal(this)" class="zoom">
    </div>
    <div class="gallery-img">
        <img src="{% static 'photo2.png' %}" onclick="openModal(this)" class="zoom">
    </div>
</div>

<div id="photomodel">
    <span class="close-btn" onclick="closeModal()">&times;</span>
    <img id="modelimage" src="">
</div>

<script>
function openModal(img) {
    const model = document.getElementById("photomodel");
    const modelimg = document.getElementById("modelimage");
    model.style.display = 'flex';
    modelimg.src = img.src;
}

function closeModal() {
    document.getElementById("photomodel").style.display = 'none';
}
</script> 


    
</body>
</html>
```
# OUTPUT:
![alt text](<Screenshot 2025-10-06 172657.png>)
![alt text](<Screenshot 2025-10-06 172759.png>)
# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
