# Ex.08 Design of Interactive Image Gallery
# DATE:06.11.25
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
gallery.html

<!DOCTYPE html>


<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
 
  <title>Image Gallery</title>
  

  <link rel="stylesheet" href="styles.css">

</head>
<style>
 
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f0f0f0;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  padding: 20px;
}

.image-container {
  position: relative;
  overflow: hidden;
  width: 500px;
  height: 550px;
}

.gallery-item {
  width: 100%;
  height: auto;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.gallery-item:hover {
  transform: scale(1.1);
}


.modal {
  display: none; 
  position: fixed;
  z-index: 1;
  padding-top: 100px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
  overflow: auto;
}

.modal-content {
  display: block;
  margin: auto;
  max-width: 80%;
  max-height: 80%;
}

.close {
  color: #fff;
  font-size: 40px;
  font-weight: bold;
  position: absolute;
  top: 10px;
  right: 25px;
  transition: 0.3s;
  cursor: pointer;
}

.close:hover,
.close:focus {
  color: #ddd;
  text-decoration: none;
  cursor: pointer;
}

#caption {
  text-align: center;
  color: #fff;
  font-size: 20px;
  padding: 10px;
}

</style>
<body>

  <div class="gallery">
    <div class="image-container">
      <img src="1.jpeg"  alt="Flower" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="2.jpeg"  alt="Flower" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="3.jpeg"  alt="Flower" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="4.jpeg" alt="Flower" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="5.jpeg"  alt="Flower" class="gallery-item">
    </div>
    <div class="image-container">
        <img src="6.jpg"  alt="Flower" class="gallery-item">
      </div>
      
    
  </div>

  
  <div id="myModal" class="modal">
    <span class="close">&times;</span>
    <img class="modal-content" id="img01">
    <div id="caption"></div>
  </div>

  <script>
  
const modal = document.getElementById("myModal");
const modalImg = document.getElementById("img01");
const captionText = document.getElementById("caption");
const closeBtn = document.getElementsByClassName("close")[0];


const images = document.querySelectorAll(".gallery-item");


images.forEach(img => {
  img.onclick = function() {
    modal.style.display = "block";
    modalImg.src = this.src;
    captionText.innerHTML = this.alt;
  };
});


closeBtn.onclick = function() {
  modal.style.display = "none";
};


window.onclick = function(event) {
  if (event.target === modal) {
    modal.style.display = "none";
  }
};

  </script>
  <footer>
    <h3>Designed and developed by TEJASWINI</h3>
  </footer>
</body>
</html>
```
## OUTPUT
![alt text](<Screenshot 2025-11-06 053958.png>)
![alt text](<Screenshot 2025-11-06 054034.png>)

![alt text](<Screenshot 2025-11-06 054700.png>)
![alt text](<Screenshot 2025-11-06 055019.png>)

![alt text](<Screenshot 2025-11-06 055033.png>)

![alt text](<Screenshot 2025-11-06 055052.png>)


## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
