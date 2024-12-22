# Ex.08 Design of Interactive Image Gallery
# Date:23/11/2024
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

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Showcase</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: lightpink;
            font-family: 'Roboto', sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            min-height: 100vh;
        }

        header {
            font-size: 2.5rem;
            margin-top: 30px;
            color: #222;
        }

        .photo-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 16px;
            padding: 20px;
            max-width: 1300px;
            width: 100%;
        }

        .photo-item {
            position: relative;
            border-radius: 12px;
            overflow: hidden;
            cursor: pointer;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.25);
        }

        .photo-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease-in-out, filter 0.3s ease;
        }

        .photo-item:hover img {
            transform: scale(1.1);
            filter: brightness(0.7);
        }

        .photo-item .label {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            background-color: rgba(0, 0, 0, 0.6);
            color: white;
            text-align: center;
            padding: 12px;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .photo-item:hover .label {
            opacity: 1;
        }

        .viewer {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background-color: rgba(0, 0, 0, 0.85);
            justify-content: center;
            align-items: center;
            z-index: 10000;
        }

        .viewer img {
            max-width: 95%;
            max-height: 95%;
        }

        .close-btn {
            position: absolute;
            top: 30px;
            right: 30px;
            font-size: 35px;
            color: white;
            cursor: pointer;
        }

        footer {
            background-color: #444;
            color: #fff;
            padding: 12px 30px;
            text-align: center;
            width: 100%;
            position: fixed;
            bottom: 0;
        }
    </style>
</head>
<body>

<header>Image Gallery</header>
<h2>Ben 10 Aliens</h2>

<div class="photo-grid">
    <div class="photo-item">
        <img src="Flamethrower.png" alt="SwampFire">
        <div class="label">SwampFire</div>
    </div>
    <div class="photo-item">
        <img src="Alien X.webp" alt="Alien X">
        <div class="label">Alien Xs</div>
    </div>
    <div class="photo-item">
        <img src="Echo Echo.jpg" alt="Echo Echo">
        <div class="label">Echo Echo</div>
    </div>
    <div class="photo-item">
        <img src="Way Big.jpg" alt="Way Big">
        <div class="label">Way Big</div>
    </div>
    <div class="photo-item">
        <img src="Graymatter.jpg" alt="Diamondhead">
        <div class="label">Diamondhead</div>
    </div>
</div>

<div class="viewer">
    <span class="close-btn">&times;</span>
    <img src="" alt="Large View">
</div>

<footer>
    <p>Designed and Developed by KARTHIKRAJ C</p>
</footer>

<script>
    const allPhotos = document.querySelectorAll('.photo-item img');
    const viewer = document.querySelector('.viewer');
    const viewerImage = viewer.querySelector('img');
    const closeBtn = viewer.querySelector('.close-btn');

    allPhotos.forEach((img) => {
        img.addEventListener('click', function() {
            viewer.style.display = 'flex';
            viewerImage.src = this.src;
        });
    });

    closeBtn.addEventListener('click', () => {
        viewer.style.display = 'none';
    });

    viewer.addEventListener('click', (e) => {
        if (e.target === viewer) {
            viewer.style.display = 'none';
        }
    });
</script>

</body>
</html>



```
# OUTPUT:
![Screenshot 2024-12-22 185506](https://github.com/user-attachments/assets/d2aac28c-bff6-4582-a750-17398e67bf13)
![Screenshot 2024-12-22 185523](https://github.com/user-attachments/assets/99dbb122-f7af-4794-9a17-2df72266802f)
![Screenshot 2024-12-22 185558](https://github.com/user-attachments/assets/c4c60f9b-baac-4051-8dc9-6e18eb5d3b00)
![Screenshot 2024-12-22 185612](https://github.com/user-attachments/assets/f0933c93-5f37-4b3f-941f-395e2c8433b1)
![Screenshot 2024-12-22 185624](https://github.com/user-attachments/assets/ed110d0f-3181-45fb-9904-7cdfcbaca83e)
![Screenshot 2024-12-22 185637](https://github.com/user-attachments/assets/47b98602-af01-4920-8301-fd6891e2c4f3)
![Screenshot 2024-12-22 185255](https://github.com/user-attachments/assets/2bbe37ef-abd5-4c54-b31a-7a79a3c66000)


# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
