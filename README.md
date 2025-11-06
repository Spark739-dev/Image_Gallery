# Ex.08 Design of Interactive Image Gallery
## DATE: 06-11-2025
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
    <html>
        <head>
            <title>GALLERY APP</title>
            <style>
                body {
            text-align: center;
            font-family: Arial, sans-serif;
            background: #fff;
            }

            .image-gallery {
            display: flex;
            justify-content: center;     
            align-items: center;         
            gap: 20px;                   
            flex-wrap: wrap;             
            padding: 20px;
            }

            .image-gallery img {
            width: 250px;                
            height: 180px;              
            border-radius: 12px;         
            object-fit: cover;           
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);  
            transition: transform 0.25s ease, box-shadow 0.25s ease;
            }

            .image-gallery img:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 18px rgba(0,0,0,0.3);
            }
            .lightbox {
            display: none; 
            position: fixed;
            z-index: 999;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.85);
            justify-content: center;
            align-items: center;
            }

        
        .lightbox img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(255,255,255,0.2);
            }

        .close-btn {
            position: absolute;
            top: 20px;
            right: 35px;
            color: white;
            font-size: 40px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
            }

        .close-btn:hover {
          color: #ff5555;
        }

            </style>
        </head>
        <body>
            <h1><bold>LIST OF PHOTOS IN GALLERY</bold></h1><br><br>
            <div= class="image-gallery">
            <img src="1.jpg" alt="IMAGE1">
            <img src="2.jpg" alt="IMAGE1">
            <img src="3.jpg" alt="IMAGE1">
            <img src="4.jpg" alt="IMAGE1">
            <img src="5.jpg" alt="IMAGE1">
            <img src="6.jpg" alt="IMAGE1">
            <img src="7.jpg" alt="IMAGE1">
            </div>
        <div class="lightbox" id="lightbox">
        <span class="close-btn" onclick="closeLightbox()">&times;</span>
        <img id="lightbox-img" src="2.jpg" alt="Enlarged image">
      </div>
      <script>
        
        const galleryImages = document.querySelectorAll('.image-gallery img');
        const lightbox = document.getElementById('lightbox');
        const lightboxImg = document.getElementById('lightbox-img');

      
        galleryImages.forEach(img => {
          img.addEventListener('click', () => {
            lightboxImg.src = img.src;
            lightbox.style.display = 'flex';
          });
        });

        
        function closeLightbox() {
          lightbox.style.display = 'none';
        }

      
        lightbox.addEventListener('click', (e) => {
          if (e.target === lightbox) {
            lightbox.style.display = 'none';
          }
        });
      </script>
        </body>
    </html>

## OUTPUT

![1](../../1output.png)
![2](<../../2 output.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
