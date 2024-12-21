# Ex.08 Design of Interactive Image Gallery
# Date:
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
```html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comic Image Gallery</title>
    
 <style>
  
    body {
        font-family: Arial, sans-serif;
        margin: 0;
        padding: 0;
        color: #333;
        text-align: center;
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        transition: background 0.5s ease;
        height: 100vh; /* Ensures the background covers the full height of the viewport */
    }

    h1 {
        color: #fff;
        padding: 20px;
        font-size: 2.5em;
        text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
        margin: 0; /* Removes extra space */
    }

    footer {
        padding: 10px;
        background-color: rgba(0, 0, 0, 0.7);
        color: white;
        font-size: 0.9em;
        text-align: center;
        position: absolute;
        bottom: 0;
        width: 100%;
    }

    .preview-box {
        width: 70%;
        margin: 20px auto;
        border: 2px solid #ddd;
        padding: 15px;
        background: rgba(255, 255, 255, 0.9);
        border-radius: 10px;
        box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        text-align: left;
    }

    .preview-box img {
        max-width: 100%;
        height: auto;
        border-radius: 8px;
        margin-bottom: 15px;
    }

    
    .gallery {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 15px;
        margin: 20px;
    }

    .gallery img {
        width: 120px;
        height: 120px;
        object-fit: cover;
        cursor: pointer;
        transition: transform 0.3s ease, border-color 0.3s ease;
        border-radius: 8px;
        border: 2px solid transparent;
        box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    }

    .gallery img:hover {
        transform: scale(1.1);
        border-color: #3498db;
    }

   
    body {
        background-size: 1500%;
        background-position: center;
    }
</style>

</head>
<body>
    <h1>Interactive Comic Image Gallery</h1>
    
    <div class="preview-box">
        <img id="preview-image" src="" alt="Preview Image">
        <p class="preview-title" id="preview-title">Click on an image to view</p>
        <p class="preview-description" id="preview-description">Description of the selected image will appear here.</p>
    </div>

    <div class="gallery">
        <img 
            src="image_gallery/gallery/static/images/berlin.jpeg" 
            data-bg="image_gallery/gallery/static/images/berlin.jpeg"
            data-description="BERLIN" 
            data-title="NETFLIX" 
            alt="Berlin Image">
        <img 
            src="image_gallery/gallery/static/images/bp.jpg" 
            data-bg="image_gallery/gallery/static/images/bp.jpg"
            data-description="BLACK PANTHER" 
            data-title="MARVEL" 
            alt="Black Panther Image">
        <img 
            src="image_gallery/gallery/static/images/dark.jpeg" 
            data-bg="image_gallery/gallery/static/images/dark.jpeg"
            data-description="DARK" 
            data-title="PRIME" 
            alt="Dark Image">
        <img 
            src="image_gallery/gallery/static/images/ironman.jpeg" 
            data-bg="image_gallery/gallery/static/images/ironman.jpeg"
            data-description="IRON MAN" 
            data-title="MARVEL" 
            alt="Iron Man Image">
        <img 
            src="image_gallery/gallery/static/images/loki.jpeg" 
            data-bg="image_gallery/gallery/static/images/loki.jpeg"
            data-description="LOKI" 
            data-title="DISNEY" 
            alt="Loki Image">
        <img 
            src="image_gallery/gallery/static/images/spidey.jpeg"
            data-bg="image_gallery/gallery/static/images/spidey.jpeg"
            data-description="SPIDER MAN" 
            data-title="MARVEL" 
            alt="Spider Man Image">
        <img 
            src="image_gallery/gallery/static/images/wed.jpeg" 
            data-bg="image_gallery/gallery/static/images/wed.jpeg"
            data-description="WEDNESDAY" 
            data-title="NETFLIX"
            alt="Wednesday Image">
    </div>

    <script>
        const previewImage = document.getElementById('preview-image');
        const previewTitle = document.getElementById('preview-title');
        const previewDescription = document.getElementById('preview-description');

        document.querySelectorAll('.gallery img').forEach(img => {
            img.addEventListener('click', () => {
                const bgImage = img.dataset.bg;
                document.body.style.backgroundImage = `url(${bgImage})`;
                previewImage.src = img.src;
                previewTitle.textContent = img.dataset.title || "No Title";
                previewDescription.textContent = img.dataset.description || "No Description";
            });
        });
    </script>
    
    <footer>
        <p>Designed by KELVIN</p>
    </footer>
</body>
</html>

```
# OUTPUT:
![Screenshot 2024-12-21 162437](https://github.com/user-attachments/assets/872202a4-fc82-404a-a984-e6556da680f1)
![Screenshot 2024-12-21 162949](https://github.com/user-attachments/assets/d23460fb-6007-4021-a9b0-b2339687dd25)

![Screenshot 2024-12-21 162937](https://github.com/user-attachments/assets/3c481595-9400-4617-b856-a685fc00cb6e)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
