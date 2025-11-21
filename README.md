# Ex.08 Design of Interactive Image Gallery
## Date: 18.05.25

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Image Gallery</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background-image: url('bg.png');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      font-family: Arial, sans-serif;
      color: white;
    }

    .tit h1 {
      font-size: 46px;
      padding: 30px;
      text-align: center;
      color: rgb(7, 7, 7);
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
      padding: 30px;
      justify-items: center;
    }

    .gallery img {
      width: 250px;
      height: 250px;
      object-fit: cover;
      cursor: pointer;
      transition: transform 0.3s ease;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
    }

    .gallery img:hover {
      transform: scale(1.05);
    }

    .popup {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-color: rgba(0, 0, 0, 0.8);
      display: none;
      justify-content: center;
      align-items: center;
      z-index: 999;
    }

    .popup img {
      width: 70%;
      max-width: 700px;
      border-radius: 20px;
      box-shadow: 0 0 30px rgba(255, 255, 255, 0.3);
    }

    .close-btn {
      position: absolute;
      top: 20px;
      right: 40px;
      font-size: 40px;
      color: white;
      cursor: pointer;
      font-weight: bold;
      transition: color 0.3s;
    }

    .close-btn:hover {
      color: red;
    }
  </style>
</head>
<body>

  <div class="tit">
    <h1>IMAGE GALLERY</h1>
  </div>

  <div class="gallery">
    <img src="1.jpg" alt="Image 1" onclick="showPopup(this.src)" />
    <img src="2.jpg" alt="Image 2" onclick="showPopup(this.src)" />
    <img src="3.jpg" alt="Image 3" onclick="showPopup(this.src)" />
    <img src="4.jpg" alt="Image 4" onclick="showPopup(this.src)" />
    <img src="5.jpg" alt="Image 5" onclick="showPopup(this.src)" />
    <img src="6.jpg" alt="Image 6" onclick="showPopup(this.src)" />
  </div>

  <!-- Popup Container -->
  <div class="popup" id="popup">
    <span class="close-btn" onclick="hidePopup()">&times;</span>
    <img id="popupImage" src="" alt="Popup Image" />
  </div>

  <script>
    function showPopup(src) {
      const popup = document.getElementById("popup");
      const popupImg = document.getElementById("popupImage");
      popupImg.src = src;
      popup.style.display = "flex";
    }

    function hidePopup() {
      document.getElementById("popup").style.display = "none";
    }

    // Optional: Close popup with ESC key
    document.addEventListener("keydown", function (e) {
      if (e.key === "Escape") {
        hidePopup();
      }
    });
  </script>

</body>
</html>
```

## OUTPUT:
<img width="1383" height="792" alt="image" src="https://github.com/user-attachments/assets/445de56c-6874-4ab6-8bd0-04b5e3fd0149" />
<img width="1397" height="756" alt="image" src="https://github.com/user-attachments/assets/58f13024-fcd5-48ff-98c4-2fff1d7b2b7d" />
<img width="1390" height="742" alt="image" src="https://github.com/user-attachments/assets/f21f5ced-dd2e-4252-9497-faab080b1146" />
<img width="1385" height="747" alt="image" src="https://github.com/user-attachments/assets/014c1428-c76e-4b05-9bf1-cd4b6625c7fe" />
<img width="1388" height="745" alt="image" src="https://github.com/user-attachments/assets/c9b2b0ce-41a6-4ba2-8cd3-ab3ffa7e5c93" />
<img width="1382" height="745" alt="image" src="https://github.com/user-attachments/assets/bf87120f-a5c6-4173-90f1-f7543efac959" />
<img width="1385" height="742" alt="image" src="https://github.com/user-attachments/assets/e0b88e08-c716-4e4f-80db-b3c41be6efad" />



## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
