# Prodigy_WD_01
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
        }

        /* Navigation menu styles */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: #333;
            color: white;
            display: flex;
            justify-content: space-around;
            align-items: center;
            padding: 10px 0;
            transition: background-color 0.3s ease;
            z-index: 1000;
        }

        .navbar.scrolled {
            background-color: #555;
        }

        .navbar a {
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            transition: color 0.3s ease, background-color 0.3s ease;
        }

        .navbar a:hover {
            background-color: #fff;
            color: #333;
            border-radius: 5px;
        }

        /* Page content */
        .content {
            margin-top: 60px;
            padding: 20px;
        }

        .section {
            height: 100vh;
            padding: 20px;
            border-bottom: 1px solid #ccc;
        }
    </style>
</head>
<body>

<div class="navbar" id="navbar">
    <a href="#section1">Home</a>
    <a href="#section2">About</a>
    <a href="#section3">Services</a>
    <a href="#section4">Contact</a>
</div>

<div class="content">
    <div class="section" id="section1">Home Section</div>
    <div class="section" id="section2">About Section</div>
    <div class="section" id="section3">Services Section</div>
    <div class="section" id="section4">Contact Section</div>
</div>

<script>
    const navbar = document.getElementById('navbar');

    // Add a scroll event listener to change navbar style on scroll
    window.addEventListener('scroll', () => {
        if (window.scrollY > 50) {
            navbar.classList.add('scrolled');
        } else {
            navbar.classList.remove('scrolled');
        }
    });
</script>

</body>
</html>
