# Ex.08 Design of Interactive Image Gallery
## Name : ESHWER M
## Reg No : 212224040086
## Date : 15.05.2025

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
```
<html>
    <head>
    <title style="font-family: 'Times New Roman', Times, serif;">BIKE GALLARY</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background:rgb(225, 255, 0) ;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }

        .header {
            text-align: center;
            padding: 10px;
            background-color: #000000;
            width: 100%;
            height:100px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        
        }

        .header h1 {
            font-size: 2.5rem;
            color: #f2ff00;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            padding: 20px;
            margin: 20px 0 10px 0;
            width: 90%;
            max-width: 1200px;
        }

        .gallery-item {
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
            border: 10px solid #000000;
            margin-right: 40px;
            border-radius: 20px;
        }

        .gallery-item img {
            width: 100%;
            height:100%;
            object-fit: cover;
            display: block;
        }


        .gallery-item::after {
            content: '';
            position:fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom right, rgba(157, 149, 149, 0.2), rgba(0, 0, 0, 0.2));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover::after {
            opacity: 1;
        }

        footer {
            text-align: center;
            margin-top: 20px;
            padding: 10px;
            width: 100%;
            height:40px;
            background-color: #000000;
            color: rgb(255, 242, 0) ;
        }

        #lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
            border-radius: 25px;
        }

        #lightbox img {
            max-width: 90%;
            max-height: 80%;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
        }

        #lightbox:target {
            display: flex;
        }

        #lightbox .close {
            position: absolute;
            top: 10px;
            right: 10px;
            background: #d9d0d0;
            border: none;
            font-size: 2rem;
            cursor: pointer;
        }
    </style>

</head>
<body>

<div class="header">
    <h1 style="font-family: 'Times New Roman', Times, serif;">IMAGE GALLERY</h1>
   
</div>

<div class="gallery">
    <div class="gallery-item" onclick="showAlert('Image 1!')">
        <img src="cls350.jpeg" alt="Image 1">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 2!')">
        <img src="st765.jpeg" alt="Image 2" >
    </div>
    <div class="gallery-item" onclick="showAlert('Image 3!')">
        <img src="daytona.jpeg"alt="Image 3">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 4!')">
        <img src="zx.jpeg" alt="Image 4">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 5!')">
        <img src="gt.jpeg" alt="Image 5">
    </div>
</div>

<div id="lightbox">
    <button class="close" onclick="closeLightbox()">X</button>
    <img src="" id="lbox-img" alt="Full Image">
</div>

<footer>
    <p><b>@ Designed by ESHWER M (212224040086)</b></p>
</footer>
<script>
    function showAlert(message) {
        alert(message);
    }

    function openLightbox(imageSrc) {
        document.getElementById('lbox-img').src = imageSrc;
        document.getElementById('lightbox').style.display = 'flex';
    }

    function closeLightbox() {
        document.getElementById('lightbox').style.display = 'none';
    }

    const galleryItems = document.querySelectorAll('.gallery-item');
    galleryItems.forEach(item => {
        item.addEventListener('click', () => {
            const imgSrc = item.querySelector('img').src;
            openLightbox(imgSrc);
        });
    });
</script>

</body>
</html>
```

## OUTPUT
![alt text](<djproject8/imageapp/static/Screenshot 2025-05-15 203116.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
