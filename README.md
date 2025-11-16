# Ex.07 Design of Interactive Image Gallery
## Date:08\11\25

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

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

## PROGRAM:
```
<html>
<head>
    <title>INTERACTIVE IMAGE GALLERY</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: lightsalmon;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
        }
        .gallery-container {
            max-width: 800px;
            margin: 20px auto;
            overflow: hidden;
            position: relative;
        }
        .gallery-slider {
            display: flex;
            transition: transform 0.5s ease;
        }
        .gallery-item {
            min-width: 100%;
            box-sizing: border-box;
        }
        .gallery-item img {
            width: 100%;
            display: block;
            border-radius: 10px;
        }
        .navigation {
            position: absolute;
            top: 50%;
            width: 100%;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
        }
        .navigation button {
            background-color: rgba(0, 0, 0, 0.5);
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            border-radius: 50%;
            font-size: 18px;
        }
        .navigation button:hover {
            background-color: rgba(0, 0, 0, 0.8);
        }
        h1 {
            text-align: center;
            margin-bottom: 20px;
        }
        footer {
            margin-top: 20px;
            font-size: 16px;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>SUDHARSAN IMAGE GALLERY</h1>
    <div class="gallery-container">
        <div class="gallery-slider" id="slider">
            <div class="gallery-item">
                <img src="vijay.jpg" alt="VIJAY">
            </div>
            <div class="gallery-item">
                <img src="sec.jpg" alt="SAVEETHA ENGINEERING COLLEGE">
            </div>
            <div class="gallery-item">
                <img src="zuck.jpg" alt="MARK ZUCKERBURG">
            </div>
            <div class="gallery-item">
                <img src="tata.jpg" alt="RATAN TATA">
            </div>
            <div class="gallery-item">
                <img src="nakamoto.jpg" alt="SATOSHI NAKAMOTO">
            </div>
            <div class="gallery-item">
                <img src="musk.jpg" alt="ELON MUSK">
            </div>
            <div class="gallery-item">
                <img src="kalam.jpg" alt="DR. APJ ABDUL KALAM">
            </div>
        </div>
        <div class="navigation">
            <button id="prev">&#10094;</button>
            <button id="next">&#10095;</button>
        </div>
    </div>

    <footer>
        NANDA KISHOR 24011485
    </footer>

    <script>
        var slider = document.getElementById('slider');
        var prev = document.getElementById('prev');
        var next = document.getElementById('next');

        var currentIndex = 0;
        var totalItems = slider.children.length;

        function updateSlider() {
            slider.style.transform = 'translateX(-' + (currentIndex * 100) + '%)';
        }

        prev.onclick = function() {
            if (currentIndex > 0) {
                currentIndex--;
            } else {
                currentIndex = totalItems - 1;
            }
            updateSlider();
        };

        next.onclick = function() {
            if (currentIndex < totalItems - 1) {
                currentIndex++;
            } else {
                currentIndex = 0;
            }
            updateSlider();
        };
    </script>
</body>
</html>
```
## OUTPUT:
<img width="644" height="367" alt="image" src="https://github.com/user-attachments/assets/6bb725fc-ff80-4cb1-920f-d5c5a089d349" />
<img width="645" height="365" alt="image" src="https://github.com/user-attachments/assets/292c4b4c-2d4b-405b-9821-7a9fff183ab7" />
<img width="640" height="365" alt="image" src="https://github.com/user-attachments/assets/bfcd5233-0f36-4890-9b4b-b45f4029f9b1" />


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
