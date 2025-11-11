# Ex.08 Design of Interactive Image Gallery
# Name: Adharsh vidyardh U
# Reg no:212224230007
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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Marvel Image Gallery</title>

    <style>
        body {
            margin: 0;
            background: url("wp9152334.jpg") no-repeat center center fixed;
            background-size: cover;
            font-family: Arial;
        }

        .gallery-container {
            text-align: center;
            padding: 20px;
            background: rgba(0, 0, 0, 0.6);
            color: white;
        }

        /* Horizontal layout */
        .gallery {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
            flex-wrap: nowrap;
            overflow-x: auto;
            padding: 20px;
        }

        /* Big images */
        .gallery img {
            width: 350px;
            height: 240px;
            object-fit: cover;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.3s;
            flex-shrink: 0;
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.85);
            justify-content: center;
            align-items: center;
        }

        .lightbox img {
            width: 80%;
            max-width: 900px;
            border-radius: 8px;
        }
    </style>
</head>

<body>

    <div class="gallery-container">
        <h1>Marvel Image Gallery</h1>

        <div class="gallery">
            <img src="img-1.jpg" alt="">
            <img src="img.2.webp" alt="">
            <img src="OIP.jpeg" alt="">
            <img src="OI.jpeg" alt="">
        </div>
    </div>

    <div id="lightbox" class="lightbox">
        <img id="lightbox-img">
    </div>

    <script>
        const galleryImages = document.querySelectorAll(".gallery img");
        const lightbox = document.getElementById("lightbox");
        const lightboxImg = document.getElementById("lightbox-img");

        galleryImages.forEach(img => {
            img.addEventListener("click", () => {
                lightbox.style.display = "flex";
                lightboxImg.src = img.src;
            });
        });

        lightbox.addEventListener("click", () => {
            lightbox.style.display = "none";
        });
    </script>

</body>
</html>
```

## OUTPUT
![alt text](<Screenshot 2025-11-11 105332.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
